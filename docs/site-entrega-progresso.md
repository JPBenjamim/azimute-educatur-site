# Progresso de Entrega

Atualizado em: 2026-07-13

| ID | Status | Evidencia | Pendencia |
|---|---|---|---|
| QA-05 | Revisar | Auditoria local encontrou 0 links/imagens locais quebrados em 36 arquivos HTML. Links externos foram ignorados na auditoria automatica. | Validar manualmente links externos principais: WhatsApp, Instagram e email. |
| CAT-01 | Revisar | Catalogo reformulado pelo pacote de conteudo: 36 cards de roteiro, sendo paginas HTML + cards de solicitacao por WhatsApp. Home/catalogo atualizados para 36 roteiros catalogados. | Decidir destino de `Da Terra a Celula` e concluir pesquisa de Fortaleza antes de chamar todos de paginas completas. |
| ROT-00 | Em andamento | Pagina `roteiro-chao-vivo-natal.html` possui resumo do roteiro, prologo, aprendizagem, jornada, incluso, BNCC, depoimentos, CTA e footer padronizado. Jornada nao usa mais foto falsa para Museu de Minerios. | Revisao visual em celular real e substituicao por foto final do Museu de Minerios/IFRN quando disponivel. |
| QA-02 | Revisar | Playwright validou home, catalogo e Chao Vivo em 320, 375, 390, 430, 768 e 1280px: 18 combinacoes, 0 overflow e 0 erro de console. | Conferir visual final em celular real. |
| QA-03 | Revisar | Menu mobile testado por Playwright em home, catalogo e Chao Vivo; `aria-expanded`, classe `open` e `body.menu-open` funcionando. | Conferir toque real no celular. |
| QA-04 | Revisar | Barra fixa dos roteiros testada em 320, 375, 390 e 430px; CTA e footer nao ficam cobertos. Barra recolhe quando o footer entra na tela. | Conferir sensacao de uso no celular real. |
| HOME-01 | Revisar | Hero principal passou no QA responsivo sem overflow ou erro de console. Menu mobile da home corrigido com estado acessivel. | Conferir no celular se a troca de imagens permanece suave em rede real. |
| HOME-02 | Revisar | Bloco Roteiros de Descoberta passou no QA responsivo; cards com imagem proporcional e sem area branca colapsada. | Conferir visual final no celular real. |
| HOME-05 | Revisar | CTA final da home passou no QA responsivo e texto foi ajustado para 36 roteiros catalogados. | Conferir se a copy final esta comercialmente forte. |
| CONTEUDO-01 | Revisar | Pacote `docs/conteudo-roteiros/` recebido: 10 arquivos por rota, com 35/36 roteiros ativos pesquisados segundo o indice do Claude. | Integrar conteudo nas paginas sem quebrar layout; pesquisar Fortaleza antes de finalizar o roteiro. |
| CONTEUDO-02 | Revisar | `O Chao Vivo de Natal` registrado como rota local/linha tematica, capaz de abrigar mini roteiros combinaveis em Natal sem duplicar o mesmo par Parque das Dunas + Museu de Minerios. | Decidir se `Da Terra a Celula` sai do catalogo ou ganha outro recorte real. |
| CONTEUDO-03 | Revisar | Roteiro de Fortaleza renomeado visualmente para `Da Fortaleza as Ondas`, com pesquisa de Fortaleza de Nossa Senhora da Assuncao, Dragao do Mar e Beach Park integrada a pagina e ao catalogo. | Confirmar viabilidade operacional da visita interna a Fortaleza de Nossa Senhora da Assuncao; URL antiga mantida para nao quebrar links. |
| NATAL-00 | Revisar | Bloco de tarefas `NATAL-01` a `NATAL-07` criado na checklist para organizar Natal e Grande Natal antes de mexer em novos cards. | Executar levantamento e classificacao dos mini roteiros. |
| NATAL-02 | Revisar | Criado `docs/natal-grande-natal-mini-roteiros.md` com 12 mini roteiros possiveis de Natal e Grande Natal, paradas, segmento, disciplinas, status e pendencias. | Validar com Jonas/Ivana quais entram no primeiro lote comercial. |
| NATAL-03 | Revisar | Mini roteiros classificados em `Pronto para card`, `Combinavel`, `Precisa pesquisa` e `Nao publicar ainda`. | Confirmar operacao de grupos nos locais marcados como combinaveis/pesquisa. |
| NATAL-04 | Em andamento | Duplicidade de `Da Terra a Celula` documentada: nao publicar como card separado enquanto repetir Parque das Dunas + Museu de Minerios. | Decisao final: remover do catalogo ou reformular com outro recorte. |
