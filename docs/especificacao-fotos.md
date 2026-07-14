# Especificação de fotos — o que buscar, quantas, em que tamanho

> Gerado em 2026-07-14. Base: dimensões reais do CSS do site (não estimativa) + paradas já pesquisadas com fonte em `site/docs/conteudo-roteiros/`.
> Objetivo: você sair pesquisando/comprando/fotografando sabendo exatamente o assunto de cada foto, sem descobrir depois que faltou uma ou que o tamanho não serve.

## Como o site usa imagem (5 espaços diferentes, por página de roteiro)

Todo `roteiro-*.html` tem 5 lugares onde imagem entra. `object-fit: cover` está configurado em todos — ou seja, a foto pode ter qualquer proporção próxima da pedida que o CSS corta automaticamente; o que precisa ser respeitado é a **resolução mínima**, não o enquadramento exato.

| # | Onde | Proporção do slot (CSS real) | Resolução mínima recomendada | Quantas fotos |
|---|---|---|---|---|
| 1 | **Hero** (colagem grande no topo da página) | proporção geral 1,34:1; a primeira foto é vertical/alta (ocupa 2 linhas), as outras 4 são menores | Foto principal: **1600×1200px**. Fotos de apoio: **1000×1000px** | 1 principal + até 4 de apoio (mín. viável: 2 fotos distintas) |
| 2 | **Card do catálogo** (miniatura na grade) | quadrada (1:1), vira 4:3 quando destacada | **1000×1000px** (quadrada, funciona nos dois casos) | 1 |
| 3 | **Jornada do aluno** (uma foto por parada) | larga, ~1,6:1 (colunas de ~450px por ~260px de altura) | **1400×900px** | **1 por parada (3 a 4 por roteiro)** — a mais importante: cada parada precisa da SUA foto, não pode repetir |
| 4 | **Tira de fotos** (photo-strip, 5 quadradinhos no fim da seção jornada) | quadrada (1:1) | **700×700px** | 5 (pode reaproveitar as fotos das paradas, cortadas em quadrado) |
| 5 | **Compartilhamento (Open Graph)** — já configurado, mas hoje usa a foto errada como placeholder | fixa, 1,91:1 | **1200×630px** | 1 (pode ser um recorte da foto hero) |

### Tradução prática por destino

O mínimo pra tirar uma página do "mosaico repetido" (que é exatamente o problema que o checklist aponta em IMG-01/IMG-02) é:

**5 a 6 fotos distintas por destino:**
1. Uma foto "capa" (grande, a mais bonita/reconhecível do lugar) → serve pro Hero e pro Open Graph.
2. Uma foto "card" (pode ser outro ângulo do mesmo ponto, ou o segundo local mais icônico) → serve pro card do catálogo.
3. Uma foto por parada da jornada (3 a 4, dependendo do roteiro) → são as fotos mais específicas, de cada local exato que a pesquisa já nomeou.

Com **31 destinos ativos**, isso dá entre **155 e 186 fotos** no total do site.

---

## Lista por destino — o que fotografar em cada parada

Cruzando com a pesquisa já feita (fontes completas em `site/docs/conteudo-roteiros/`). Onde a pesquisa não achou nome de local específico, marco como pendência — aí a foto também depende de decidir o local antes.

### Rota do Litoral e do Mar
- **Aquário de Natal** (Redinha Nova): tanque do mergulho (peixes de recife); área de mini zoológico (pinguins/tartarugas/jacarés); grupo escolar com monitor.
- **Mata Estrela / Baía Formosa**: trecho sombreado da trilha no Parque Florestal Senador Antônio Farias; Lagoa da Coca-Cola/Araquara (água escura característica); dossel da mata sobre dunas.
- **No Alto da Falésia (Pipa)**: trilha na mata do Santuário Ecológico; mirante do Madeiro com a enseada; falésia vista da praia.
- **Cajueiro e Barreira**: copa do Cajueiro de Pirangi (de longe, pra mostrar escala); entrada do Centro de Cultura Espacial; instalação do CLBI.
- **Raízes e Muralhas (Forte + Ribeira)**: Forte dos Reis Magos visto da barra do Potengi; interior do Museu de Artes Populares; fachada de prédio histórico da Ribeira.
- **A Laguna que Trabalha (Guaraíras)** — pendência: depende de confirmar operador náutico antes.

### Rota do Sal e do Vento
- **Galinhos**: travessia de barco em Pratagil; salina com duna de sal; vila com charrete.
- **Sal, Sol e Liberdade (Mossoró)**: fachada do Memorial da Resistência (Av. Rio Branco); interior de um dos 4 módulos de exposição.
- **Dunas do Rosado** — pendência: sem contato/condutor confirmado ainda.
- **Do Sal ao Prato** — pendência: depende de qual empresa salineira autorizar visita.

### Rota das Serras
- **A Serra que Pinga (Portalegre)**: queda da Cachoeira do Pinga; vista do Mirante da Ponta da Serra (contraste serra x sertão); trilha com passarelas de madeira.
- **No Topo da Serra (Martins)**: vista do Mirante da Carranca; entrada/interior da Casa de Pedra.
- **Serra das Gameleiras (Araruna + Serra de São Bento)**: Pedra da Boca (a cavidade característica); Cânion de Macapá; Mirante das Serras.
- **Serra e Quilombo** — pendência: só fotografar com autorização explícita da comunidade quilombola envolvida.

### Rota do Seridó · Geoparque UNESCO
- **Onde Nasce o Potengi (Cerro Corá)**: a nascente do Potengi (o filete de água real); Mirante Serra Verde/Cruzeiro; afloramento de rocha no Vale Vulcânico.
- **Coração de Metal do Seridó (Currais Novos)**: entrada das galerias adaptadas da Mina Brejuí; acervo do Museu Mineral Mário Moacyr Porto; Mirante das Dunas (dentro do complexo).
- **Janelas do Seridó (Acari)**: vista do Açude Gargalheiras; fachada da Basílica de N. Sra. da Guia; fachada da Igreja de N. Sra. do Rosário.
- **Pedra, Tinta e Fé (Carnaúba dos Dantas)** — pendência: fotografar painel de gravura só com autorização/regras confirmadas do sítio.

### Rota das Cavernas e da Pré-História
- **O Sertão Já Foi Mar (Lajedo de Soledade)**: um painel de pintura rupestre (Araras, Urubu ou Olho d'Água); interior do Museu do Lajedo; mini-cânion de calcário.
- **O Enigma da Pedra do Ingá**: painel de gravuras; Museu de História Natural do sítio; grupo em atividade de registro/desenho.
- **Subterrâneos da Caatinga (Furna Feia)** — pendência: precisa autorização do ICMBio pra fotos comerciais do interior.
- **Capital das Cavernas (Felipe Guerra)** — pendência: sem condutor confirmado ainda.

### Rota dos Engenhos e da História
- **Civilização e Engenhos (Areia)**: já tem fotos reais no site — conferir se são suficientes ou reforçar.
- **Entre Trilhos, Engenhos e Saberes (Bananeiras)**: fachada da Estação Ferroviária (hoje pousada); processo de produção no Engenho Goiamunduba; trecho do centro histórico.
- **Terra do Açúcar e do Rio (Ceará-Mirim)**: torres da Igreja Matriz de N. Sra. da Conceição; fachada do Museu Nilo Pereira/antiga Casa Grande do Guaporé.
- **Roliude (Cabaceiras/PB — correção de estado feita)**: paisagem árida característica; cenário de filmagem, se identificado — pendência de pesquisa adicional.

### Rota da Fé e da Memória
- **Primeiros Santos do Brasil (Cunhaú + Uruaçu)**: fachada/interior da Capela das Candeias em Cunhaú; monumento/capela de Uruaçu; detalhe das pedras coloniais preservadas.
- **A Cidade da Estátua (Santa Cruz)** — pendência: depende de agendamento no complexo.

### Rota da Ciência e do Espaço
- **Rumo ao Espaço (Barreira do Inferno)** — pendência: precisa autorização do CLBI pra foto de interior/alunos.
- **O Chão Vivo de Natal**: já tem 2 fotos próprias; falta 1 foto real do Museu de Minérios do RN (hoje usa ícone) e 1 do fechamento.
- **Do Rio ao Mar**: acervo do Museu de Minérios; barco do "Auto do Potengi" na Praia da Redinha.

### Rota dos Povos Originários
- **Potiguara (Baía da Traição)** — pendência: só fotografar trilha/Rio do Gozo/Casa do Bejú com autorização explícita da comunidade; nunca retrato de pessoa sem consentimento.

### Rota das Capitais
- **Arrebol Paraibano (João Pessoa)**: fachada da Igreja de São Francisco/Capela Dourada; torre-mirante da Estação Cabo Branco; marco da Ponta do Seixas.
- **Pernambuco Imortal (Recife + Olinda)**: Marco Zero; Rua do Bom Jesus/Sinagoga; Alto da Sé com a Caixa D'Água.
- **Do Marco Zero às Ondas (Fortaleza)** — pendência: componente urbano ainda não confirmado (ver `10-rota-capitais.md`); Beach Park já é fotografável.

---

## Resumo rápido pra organizar a busca

| Prioridade | Motivo |
|---|---|
| **Fazer primeiro**: destinos sem pendência (Aquário, Mata Estrela, Pipa, Forte+Ribeira, Galinhos, Mossoró, Portalegre, Martins, Serra das Gameleiras, Cerro Corá, Currais Novos, Acari, Soledade, Ingá, Bananeiras, Ceará-Mirim, Cunhaú+Uruaçu, Chão Vivo de Natal, Rio ao Mar, João Pessoa, Recife+Olinda) | Já sabemos exatamente o que fotografar — 21 destinos, ~110-125 fotos |
| **Depende de autorização de terceiro antes de fotografar**: Guaraíras, Dunas do Rosado, Do Sal ao Prato, Serra e Quilombo, Carnaúba dos Dantas, Furna Feia, Felipe Guerra, Santa Cruz, Barreira do Inferno, Potiguara | 10 destinos — resolver contato primeiro, fotografar depois |
| **Falta decidir o local exato antes**: Roliude (qual cenário?), Fortaleza (qual marco urbano?) | 2 destinos |

## Fontes gráficas de apoio (se quiser começar com banco de imagens antes das fotos próprias)

Como alternativa temporária (não definitiva — o checklist COPY/IMG pede fotos finais, não stock), Wikimedia Commons já é usado no rodapé do site como fonte de crédito para outras imagens do projeto — pode ser onde procurar primeiro para os locais públicos/naturais (parques, sítios, igrejas tombadas). Locais privados (engenhos, museus, CLBI) provavelmente exigem contato direto ou fotografia própria, já que dificilmente têm banco de imagem livre de direitos.
