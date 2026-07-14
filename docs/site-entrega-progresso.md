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
