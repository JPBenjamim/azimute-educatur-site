# Checklist de Entrega do Site Azimute Educatur

Use a coluna `Status` na planilha com: `Pendente`, `Em andamento`, `Revisar`, `Aprovado`.

| ID | Prioridade | Area | Tarefa | Criterio de aceite |
|---|---|---|---|---|
| BUG-01 | Alta | Roteiros | Padronizar rodape das paginas de roteiro com a home | Home, catalogo e roteiros exibem a mesma estrutura de marca, links, contato e creditos |
| BUG-02 | Alta | Mobile | Corrigir textos que estouram a largura da tela | Nenhum texto gera scroll horizontal em 320px, 375px, 390px e 430px |
| BUG-03 | Alta | Mobile | Corrigir estouros internos em cards e carrosseis | Listas, chips BNCC, CTA, depoimentos e cards quebram linha dentro do container |
| BUG-04 | Alta | Rodape | Compactar rodape no mobile | Rodape nao ocupa uma tela inteira e nao briga com a barra fixa inferior |
| BUG-05 | Alta | Cards | Corrigir cards de roteiro aparecendo brancos | Todo card tem imagem visivel, altura proporcional, titulo, local, etapa e CTA |
| QA-01 | Alta | Responsivo | Auditar todas as paginas principais no mobile real | Home, catalogo e roteiro modelo aprovados em celular |
| QA-02 | Alta | Responsivo | Auditar larguras 320, 375, 390, 430, tablet e desktop | Nenhuma largura apresenta corte lateral ou texto sobreposto |
| QA-03 | Alta | Navegacao | Testar menu mobile aberto e fechado | Menu abre, fecha, links funcionam e nao deixa a pagina presa |
| QA-04 | Alta | Barra fixa | Testar barra inferior dos roteiros | Botoes nao cobrem titulos, cards, rodape ou CTA final |
| QA-05 | Alta | Links | Verificar links quebrados em todos os HTMLs | Todos os links internos abrem pagina existente |
| HOME-01 | Alta | Home | Revisar hero principal | Texto cabe no mobile, transicao suave, CTA visivel e sem piscada branca |
| HOME-02 | Alta | Home | Revisar bloco Roteiros de Descoberta | Cards sem area branca, imagem consistente e CTA clicavel |
| HOME-03 | Media | Home | Revisar contagem de roteiros | Numero exibido bate com catalogo publicado |
| HOME-04 | Media | Home | Revisar Diario de Campo | Posts escolhidos, capas e textos coerentes com Instagram |
| HOME-05 | Media | Home | Revisar CTA final | Texto curto, botao claro e responsivo |
| CAT-01 | Alta | Catalogo | Confirmar total final de roteiros | Quantidade do catalogo bate com paginas disponiveis |
| CAT-02 | Alta | Catalogo | Revisar rotas tematicas como subtitulos | Cada roteiro fica dentro de uma rota coerente |
| CAT-03 | Alta | Catalogo | Revisar filtros de rota | Usuario alterna rotas sem precisar voltar manualmente ao topo |
| CAT-04 | Media | Catalogo | Destacados sobem na rota selecionada | Roteiros em destaque aparecem primeiro dentro do grupo ativo |
| CAT-05 | Alta | Catalogo | Revisar todos os cards | Todos tem imagem, titulo, local, segmento, selo e link |
| CAT-06 | Media | Catalogo | Revisar cards em desenvolvimento | Dev badge claro e sem parecer erro visual |
| ROT-00 | Alta | Roteiros | Finalizar pagina piloto O Chao Vivo de Natal | Pagina aprovada em desktop e mobile, com conteudo completo, fotos individuais, BNCC, jornada, incluso, depoimentos, CTA e footer |
| ROT-01 | Alta | Roteiros | Replicar a estrutura aprovada para todos os roteiros | Todas as paginas roteiro-*.html usam a mesma estrutura visual e as mesmas secoes da pagina piloto |
| ROT-01A | Alta | Roteiros | Comparar cada roteiro com a pagina piloto | Nenhum roteiro fica sem secao obrigatoria, sem CTA, sem card O roteiro ou com footer antigo |
| ROT-02 | Alta | Roteiros | Cada roteiro responde onde e | Pagina informa cidade, pontos visitados e paradas principais |
| ROT-03 | Alta | Roteiros | Revisar card O roteiro | Destino, duracao, saida/retorno, minimo de alunos e formato presentes |
| ROT-04 | Alta | Roteiros | Revisar prologo local | Mini resumo historico, cultural ou geografico sem texto generico |
| ROT-05 | Alta | Roteiros | Revisar Aprendizagem | Cards alinhados, textos objetivos e sem estouro |
| ROT-06 | Alta | Roteiros | Revisar A jornada do aluno | Cada parada usa foto individual, texto concreto e ordem clara |
| ROT-07 | Alta | Roteiros | Revisar Tudo que a escola recebe | Incluso, operacao e BNCC cabem no mobile |
| ROT-08 | Alta | Roteiros | Revisar BNCC | Formato codigo + disciplina entre parenteses + descricao |
| ROT-09 | Media | Roteiros | Revisar depoimentos | Professores e responsaveis aparecem com hierarquia clara |
| ROT-10 | Media | Roteiros | Revisar CTA final | Nao ocupa tela demais e leva ao WhatsApp correto |
| IMG-01 | Alta | Imagens | Remover fotos repetidas indevidas | Imagens repetidas so ficam quando houver intencao visual |
| IMG-02 | Alta | Imagens | Trocar colagens dentro de cards | Cards de jornada usam fotos individuais, nao mosaicos |
| IMG-03 | Media | Imagens | Padronizar proporcao das imagens | Cards, hero, carrosseis e jornada mantem proporcoes consistentes |
| IMG-04 | Media | Imagens | Substituir imagens provisiorias por fotos finais | Fotos finais entram sem credito Wikimedia no rodape; creditos/licencas ficam controlados em documento interno se necessario |
| COPY-01 | Alta | Conteudo | Revisar tom Azimute | Texto pedagogico, concreto e seguro, sem cara de turismo generico |
| COPY-02 | Alta | Conteudo | Remover textos de legenda/mockup | Nenhum trecho parece comentario interno ou placeholder |
| COPY-03 | Media | Conteudo | Evitar promessas vagas | Cada roteiro mostra paradas, temas e resultado esperado |
| COPY-04 | Media | Conteudo | Revisar nomes oficiais | Cidades, atrativos, instituicoes e locais sem erro |
| PUB-01 | Alta | Publicacao | Commitar por grupo de ajuste | Cada push tem escopo claro para rastrear regressao |
| PUB-02 | Alta | Publicacao | Conferir GitHub Pages apos push | Paginas publicadas refletem o commit esperado |
| PUB-03 | Alta | Publicacao | Fazer revisao final em celular real | Prints finais aprovados antes de enviar para socia |
