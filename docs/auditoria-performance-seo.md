# Auditoria de Performance e SEO — Azimute Educatur

> Executada em 2026-07-14. Performance medida com Lighthouse (Chrome headless) contra o site rodando localmente. SEO auditado manualmente nos arquivos HTML. Relatórios brutos do Lighthouse ficam fora do repositório (scratchpad da sessão) — os números abaixo são o que importa.

## Resposta direta: não está excelente

Performance medida: **63/100 no catálogo, 64/100 numa página de roteiro**. SEO técnico raso (o score do Lighthouse) deu 100, mas isso não significa "pronto para rankear" — faltam praticamente todos os elementos que fazem o Google decidir mostrar o site pra buscas de turismo genéricas, que é o objetivo que você descreveu.

---

## 1. Performance — números reais

| Página | Performance | LCP (maior elemento visível) | Payload total |
|---|---|---|---|
| `catalogo.html` | 63/100 | **12,1 s** | 5,9 MB |
| `roteiro-areia.html` | 64/100 | **7,8 s** | 1,05 MB |

Referência: Google considera "bom" um LCP até 2,5 s. Estamos 3 a 5x acima disso.

### Causa raiz (única, e é sempre a mesma)

**Imagens não otimizadas.** Não é o HTML, não é a arquitetura estática — é peso de arquivo:

- `catalogo-cajueiro-barreira-card.jpg` — 728 KB, exibida como card de ~260 px de largura.
- `catalogo-serra-sao-bento-card.jpg` — 628 KB.
- `catalogo-janelas-serido-card.jpg` — 603 KB.
- `catalogo-areia-hero.jpg` — 450 KB, é o próprio LCP da página de Areia.

Nenhuma tem `srcset`/tamanho responsivo, nenhuma está em WebP/AVIF (apesar de já existir `.webp`/`.avif` gerado para os heróis do index — as imagens de card e das páginas de roteiro não usam essas variantes), e o catálogo carrega ~15-20 dessas fotos de uma vez na mesma tela.

**Segunda causa, menor:** Font Awesome inteiro carregado via CDN (154 KB de fonte + 19 KB de CSS) só para uns 15 ícones usados — 99,3% do CSS do Font Awesome não é usado na página.

### Correção (prioridade, sem mudar arquitetura)

1. Redimensionar e comprimir toda imagem de card para o tamanho real de exibição (~500-600px de largura) e converter para WebP — isso sozinho deve cortar os 5,9 MB do catálogo para menos de 1 MB.
2. Trocar o CDN do Font Awesome por um subset com só os ícones usados (ou SVG inline).
3. Isso é *ortogonal* à migração pra template/SSG que conversamos — pode e deve ser feito já, independente de trocar a stack.

---

## 2. SEO — o que falta para aparecer no Google

O Lighthouse SEO deu 100 porque ele só checa o básico (viewport, título existe, meta description existe, links têm texto). Isso não é "pronto pra rankear" — é "não tem erro grosseiro". Para o objetivo que você descreveu (aparecer em buscas de turismo no RN, não só pedagógicas), faltam as peças que realmente pesam:

### Ausências confirmadas (auditoria manual, 37 páginas HTML)

| Item | Status | Por que importa |
|---|---|---|
| `sitemap.xml` | **Não existe** | Google descobre e prioriza indexação das 37 páginas muito mais rápido com um sitemap. Sem ele, depende de rastrear link por link. |
| `robots.txt` | **Não existe** | Não bloqueia nada por padrão, mas também não referencia o sitemap — é um sinal básico ausente. |
| Dados estruturados (JSON-LD / schema.org) | **Zero páginas têm** | Este é o maior buraco para o objetivo de turismo. Sem marcar os roteiros como `TouristAttraction`, `Place` ou `EducationEvent`, o Google não tem como oferecer rich results (estrelas, imagem, preço "sob consulta", localização) nem entender que "Galinhos" no seu site é o mesmo lugar que aparece em buscas de turismo genéricas. |
| Open Graph / Twitter Card | **Zero páginas têm** | Sem isso, compartilhar um link no WhatsApp/Instagram/Facebook não mostra imagem nem título formatado — link aparece pelado. Também é sinal que motores de busca usam. |
| Canonical tags | **Zero páginas têm** | Risco baixo agora, mas é prática ausente. |
| Google Search Console / Analytics | **Não encontrado nas páginas** | **Este é o problema mais sério de todos.** Sem Search Console, vocês não sabem se o Google já indexou o site, por quais termos ele aparece, se há erro de rastreamento. É estar cego para o próprio objetivo. |
| `<h1>` único por página | index.html tem **5 H1s** | Cada H1 é um "isso aqui é o assunto principal desta página" para o Google. Ter 5 dilui o sinal — deveria haver 1 H1 e os outros virarem H2 ou texto sem hierarquia semântica de título. |
| `alt` em imagens | **259 imagens com `alt=""`** no site inteiro | Busca de imagem no Google (que é tráfego real para turismo/viagem) depende de alt text descritivo. Vazio = invisível para esse canal. |

### O problema estratégico, não só técnico

Todo título e meta description do site fala a língua de venda B2B pedagógica:

> "Expedição Pedagógica em Galinhos/RN... alinhada à BNCC"

Ninguém pesquisando "o que fazer em Galinhos RN" ou "roteiro RN turismo" digita nada parecido com "BNCC" ou "expedição pedagógica". O conteúdo pode continuar vendendo pra escola primeiro — mas se a meta é também aparecer pra turismo geral, os títulos, H1 e primeiro parágrafo de cada página de destino precisam conter a linguagem que a pessoa comum busca (nome do lugar + "o que fazer", "roteiro", "passeio", "visitar"), com a proposta pedagógica entrando depois, não substituindo completamente a intenção de busca genérica.

Isso não significa abandonar o tom Azimute — significa que cada página de roteiro pode ter uma segunda camada de conteúdo (ou um roteiro "gêmeo" de turismo geral) que capture esse público antes de apresentar a oferta escolar.

---

## 2.1 Correções já aplicadas em 2026-07-14 (sem depender de fotos finais)

Executei a parte da lista de prioridade que não depende de imagem definitiva:

- **`sitemap.xml`** criado, com as 31 páginas reais do site (URL real: `jpbenjamim.github.io/azimute-educatur-site/`).
- **`robots.txt`** criado, referenciando o sitemap e bloqueando páginas de mockup/template/órfã (`roteiro-serra-sao-bento.html`, que ficou sem link no catálogo desde a remoção do duplicado).
- **`index.html`**: corrigido de 5 `<h1>` para 1 — os 4 slides seguintes do carrossel viraram `<p class="hero-h1" role="heading" aria-level="2">`, mantendo o visual idêntico (a classe CSS não mudou) mas parando de competir pelo sinal de "assunto principal da página".
- **Canonical, Open Graph, Twitter Card e JSON-LD (`schema.org`)** injetados nas 32 páginas reais do site:
  - Roteiros ganharam `TouristAttraction` com nome, descrição, endereço (cidade/UF) e `touristType` (Escolas, Famílias, Turismo educativo) — isso ajuda o Google a entender que a página é sobre um lugar visitável, não só conteúdo institucional.
  - `index.html` ganhou `Organization`, `catalogo.html` ganhou `CollectionPage`.
  - `og:image` usa a imagem que já está em cada página hoje — quando as fotos finais entrarem, a troca é automática (o script lê a primeira `<img>` do arquivo).

**O que isso não resolve:** nenhuma dessas mudanças toca no problema de performance (imagens pesadas) nem na estratégia de palavra-chave de turismo geral (títulos ainda falam a língua pedagógica) — aqueles continuam para quando o site estiver com as fotos finais, como você definiu.

**Pendência que só você resolve:** o Google Search Console precisa da sua conta/domínio para ser verificado — isso eu não posso fazer sozinho, é passo manual de vocês.

---

## 3. Prioridade de ação

**Alto impacto, baixo esforço (fazer primeiro):**
1. Comprimir/redimensionar as imagens de card e hero — resolve 90% do problema de performance.
2. Criar `sitemap.xml` e `robots.txt`.
3. Configurar Google Search Console (é grátis, só precisa verificar propriedade do domínio) — sem isso, vocês continuam cegos.
4. Corrigir os 5 H1 do index.html.

**Médio impacto, médio esforço:**
5. Adicionar Open Graph em todas as páginas (título, descrição, imagem) — melhora compartilhamento e é sinal de SEO.
6. Adicionar `alt` descritivo em todas as imagens.
7. Adicionar JSON-LD (`TouristAttraction`/`Place`) nas páginas de roteiro.

**Estratégico, precisa de decisão sua:**
8. Revisar títulos/H1/primeiro parágrafo de cada página de destino para capturar intenção de busca de turismo geral, não só pedagógica — isso é decisão de conteúdo, não só técnica.

## Ferramentas usadas nesta auditoria

- Lighthouse 13.4.0 via `npx lighthouse` contra Chrome headless local, servindo o site com `python -m http.server`.
- Grep manual nos 37 arquivos HTML para sitemap, robots.txt, JSON-LD, Open Graph, canonical, H1, alt text.
- Relatórios brutos (JSON/HTML do Lighthouse) não foram commitados no repositório — ficaram no scratchpad da sessão. Posso regerar a qualquer momento.
