# Validação técnica · Atelier 04

Testada no Chromium por meio do Playwright em 26/11/2026, com as conexões externas bloqueadas para comprovar que os dados e gráficos não dependem da internet.

- [x] Dados embutidos: 100 vendas, US$ 12.827.800,50 de receita, 79 cidades, 24 datas ausentes.
- [x] Total de vendas, receita compacta + receita exata, ticket médio e cidades atualizam com filtros.
- [x] Quatro filtros temáticos e intervalo de ano de venda (seis controles combináveis).
- [x] Filtros de data usam ano da VENDA; gráfico usa ano-MODELO; dados sem data não entram em períodos selecionados.
- [x] Gráficos de famílias/versões, ano-modelo e mix de famílias desenhados em HTML5 Canvas 2D, sem bibliotecas de gráficos.
- [x] Cidade Boston: 2 vendas e empate entre famílias 718 e 911; alerta de amostra pequena exibido.
- [x] Seleção vazia: 0 vendas sem exceções JavaScript.
- [x] Botões Famílias/Versões, Limpar filtros e reset verificados.
- [x] Exportação CSV gerou arquivo com cabeçalho e 100 registros.
- [x] Visual renderizado em desktop (1440 px) e celular (390 px); nenhuma rolagem horizontal no celular.
- [x] Nenhum erro de JavaScript observado durante os testes.
- [ ] Testar visual da fotografia remota no GitHub Pages com internet disponível.
- [ ] Publicar no repositório do usuário (não modificado durante esta atualização).

Observação: fotografias e fontes externas não foram carregadas no ambiente de teste. A interface possui estilos de fallback e ilustração vetorial própria.


## Atualização da capa (26/11/2026)

- Ilustração genérica SVG removida da capa.
- CSS utiliza fotografia externa do 718 Cayman GT4 RS vermelho/preto via Porsche Finder.
- Link da fonte da imagem incluído no rodapé; depende de rede e disponibilidade da origem.
- Ainda é necessário conferir o carregamento da imagem no GitHub Pages com acesso à rede.