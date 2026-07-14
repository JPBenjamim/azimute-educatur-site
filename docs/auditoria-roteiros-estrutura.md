# Auditoria Estrutural das Paginas de Roteiro

Atualizado em: 2026-07-14

Escopo: arquivos `roteiro-*.html`. Esta auditoria evita a frente de SEO em andamento pelo Claude.

## Resultado geral

- 29 paginas de roteiro auditadas.
- Todas possuem hero, card "O roteiro", prologo, aprendizagem, jornada, bloco de incluso/BNCC, CTA final, footer, menu mobile e barra mobile.
- A diferenca estrutural encontrada nao e ausencia da secao de depoimentos, e sim ausencia do `id="depoimentos"` em algumas paginas.

## Ajustes encontrados

### ROT-09 — Depoimentos sem ancora

As paginas abaixo possuem estilos/conteudo de depoimentos, mas a secao nao tem `id="depoimentos"`. Isso pode quebrar links internos ou impedir navegacao direta para depoimentos.

- `roteiro-baia-da-traicao.html`
- `roteiro-barreira-do-inferno.html`
- `roteiro-cerro-cora.html`
- `roteiro-galinhos.html`
- `roteiro-lajedo-soledade.html`
- `roteiro-martires-cunhau-uruacu.html`
- `roteiro-pedra-do-inga.html`
- `roteiro-pipa-falesias.html`
- `roteiro-portalegre.html`

Acao recomendada: adicionar `id="depoimentos"` na secao `.testimonials`.

### COPY-02 / COPY-03 — Titulos de aprendizagem com gramatica quebrada

Padrao encontrado:

- `O que muda no aluno depois de da Aldeia`
- `O que muda no aluno depois de da Base`
- `O que muda no aluno depois de da Nascente`
- `O que muda no aluno depois de de Galinhos`
- `O que muda no aluno depois de de Soledade`
- `O que muda no aluno depois de do Inga`
- `O que muda no aluno depois de da Serra`

Acao recomendada: trocar para uma formula sem preposicao duplicada, por exemplo:

`O que muda no aluno depois desta expedicao`

ou usar nome completo do roteiro, quando a frase ficar natural.

## Proximos passos

1. Corrigir as ancoras de depoimentos.
2. Corrigir titulos de aprendizagem quebrados.
3. Rodar nova busca por `de da`, `de do`, `de de` e `de Pipa`.
4. Depois partir para auditoria de imagens (`IMG-01`, `IMG-02`, `IMG-03`).
