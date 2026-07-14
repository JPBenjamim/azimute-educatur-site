# Fila de Pendencias do Site

Atualizado em: 2026-07-14

Esta fila organiza o que ainda falta executar sem conflitar com a frente de SEO em andamento pelo Claude.

## Em andamento com Claude

| ID | Frente | Observacao |
|---|---|---|
| SEO-01 | Performance/SEO | Claude esta trabalhando em `index.html`, `robots.txt`, `sitemap.xml` e `docs/auditoria-performance-seo.md`. Codex nao deve tocar nesses arquivos ate a frente fechar. |

## Pendencias que dependem de decisao

| ID | Tarefa | Decisao necessaria |
|---|---|---|
| NATAL-04 | Resolver `Da Terra a Celula` | Remover do catalogo ou reformular com outro recorte sem repetir Parque das Dunas + Museu de Minerios |
| NATAL-05 | Definir mini roteiros de Natal que viram cards | Escolher primeiro lote: sugestao inicial `NAT-01`, `NAT-06`, `NAT-07`, `NAT-03` |
| CAT-01 | Confirmar total final de roteiros | Total muda se `Da Terra a Celula` sair ou se novos mini roteiros de Natal entrarem |
| IMG-04 | Substituir imagens provisorias | Depende de fotos finais ou decisao de gerar/usar imagens temporarias licenciadas |
| PUB-03 | Revisao final em celular real | Precisa de validacao manual no aparelho antes de enviar para socia |

## Pendencias executaveis pelo Codex agora

| ID | Prioridade | Proximo passo |
|---|---|---|
| NATAL-06 | Alta | Atualizar catalogo depois da decisao sobre `Da Terra a Celula` e primeiro lote de Natal |
| NATAL-07 | Media | Desenvolver primeira pagina nova da Rota Chao Vivo depois da escolha do roteiro |
| ROT-01A | Alta | Rodar comparacao estrutural entre pagina piloto e todas as paginas `roteiro-*.html` |
| ROT-02 | Alta | Fazer pente fino de "onde e" e paradas reais nas paginas ja publicadas |
| ROT-03 | Alta | Conferir card "O roteiro" em todas as paginas |
| ROT-04 | Alta | Conferir prologo local em todas as paginas |
| ROT-05 | Alta | Conferir cards de aprendizagem em todas as paginas |
| ROT-06 | Alta | Conferir jornada do aluno em todas as paginas |
| ROT-07 | Alta | Conferir bloco "Tudo que a escola recebe" em todas as paginas |
| ROT-08 | Alta | Conferir formato BNCC em todas as paginas |
| ROT-09 | Media | Conferir depoimentos professores/responsaveis em todas as paginas |
| ROT-10 | Media | Conferir CTA final em todas as paginas |
| IMG-01 | Alta | Mapear fotos repetidas indevidas nas paginas |
| IMG-02 | Alta | Mapear onde cards de jornada ainda usam colagens |
| IMG-03 | Media | Auditar proporcao das imagens de cards, hero, carrosseis e jornada |
| COPY-01 | Alta | Auditar tom Azimute em paginas publicadas |
| COPY-02 | Alta | Buscar textos de mockup/placeholder |
| COPY-03 | Media | Buscar promessas vagas sem paradas concretas |
| COPY-04 | Media | Checar nomes oficiais de locais em paginas publicadas |
| QA-05 | Alta | Validar links externos principais: WhatsApp, Instagram e email |

## Pendencias tecnicas ja em revisao

| ID | Status atual | Falta |
|---|---|---|
| QA-02 | Revisar | Conferencia em celular real |
| QA-03 | Revisar | Conferencia de toque real no menu mobile |
| QA-04 | Revisar | Conferencia da barra fixa em celular real |
| HOME-01 | Revisar | Conferir transicao do hero em rede real |
| HOME-02 | Revisar | Conferir cards no celular real |
| HOME-05 | Revisar | Validar forca comercial da copy final |
| ROT-00 | Em andamento | Revisao visual em celular real e foto final do Museu de Minerios |

## Proxima execucao recomendada

1. Rodar auditoria estrutural das paginas de roteiro (`ROT-01A`, `ROT-03` a `ROT-10`).
2. Gerar relatorio de divergencias sem editar paginas ainda.
3. Corrigir em lote apenas o que for padrao/template, evitando arquivos SEO do Claude.
