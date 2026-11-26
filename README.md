# Porsche Sales Intelligence · Midnight GT4 RS

Dashboard com identidade visual **dark premium** em **HTML único** com **HTML5 Canvas 2D**, filtros e análises exploratórias de 100 registros. Projeto educacional independente, sem vínculo com Porsche AG. O código foi refeito com referência conceitual e visual do [site Porsche Brasil](https://www.porsche.com/brazil/pt/) e dos [tokens de cor do Porsche Design System](https://designsystem.porsche.com/v4/tokens/color/), usando tipografia de sistema/Google Fonts (sem arquivos de fontes proprietárias).

## Funcionalidades

- Filtros: **modelo Porsche, ano-modelo, cidade, pagamento, ano inicial e ano final da venda**.
- **KPIs:** quantidade de vendas, receita em USD, ticket médio em USD e cidades ativas.
- **Pergunta 1:** quais modelos mais são vendidos por cidade? Gráfico em Canvas com opção de agrupar por família ou versão exata.
- **Pergunta 2:** qual ano-modelo mais saiu no período selecionado? Canvas vertical com ano-modelo e seletores independentes para ano da venda.
- **Pergunta 3:** quais veículos aparecem mais em cada cidade? Card com empates e avisos de amostra pequena; lista clicável de cidades.
- Gráfico de rosca do mix de famílias em Canvas, tabela de registros paginada e exportação CSV.
- Os gráficos são desenhados em HTML5 Canvas. Dependências de JavaScript: **nenhuma**. A foto real do Porsche 718 Cayman GT4 RS vermelho/preto e as fontes web dependem de conexão com a internet, mas gráficos/dados/filtros não.

## Dados e limites

- Base sanitizada utilizada nas versões anteriores do projeto; **100 registros**, com datas entre 2024–2027 e **24 datas não informadas**.
- Algumas vendas têm datas posteriores a novembro de 2026; portanto, a base é de **estudo** e não deve ser anunciada como relatório real de vendas históricas.
- Todos os valores são **USD** e as cidades são dos **Estados Unidos**, não do Brasil.
- Sem filtro de período, as 24 vendas sem data entram no total; ao aplicar filtros pelo *ano da venda*, são excluídas porque não há ano verificável.
- Ano-modelo e ano da venda são dimensões diferentes.
- Muitas cidades têm uma ou duas vendas: os insights representam a frequência *dentro da amostra*, não preferência comprovada de mercado.

## Como abrir e publicar

1. Abra `index.html` no navegador (os filtros e gráficos funcionam mesmo offline; imagem hero e fontes podem não carregar sem internet).
2. Para publicar, substitua somente o `index.html` na raiz da branch `main` do [repositório do projeto](https://github.com/lucaalima201-create/porsche-sales-intelligence). Confira o arquivo antigo antes de substituir.
3. O GitHub Pages seguirá usando o mesmo URL: https://lucaalima201-create.github.io/porsche-sales-intelligence/

## Crédito e fontes de referência

- Referência estética: https://www.porsche.com/brazil/pt/
- Tokens e diretrizes públicas: https://designsystem.porsche.com/v4/
- Fotografia real do **Porsche 718 Cayman GT4 RS vermelho e preto**: [Porsche Finder](https://finder.porsche.com/de/de-DE/details/porsche-718-cayman-gt4-rs-gebraucht-9XPP2W), imagem exibida diretamente da hospedagem externa da Porsche (`images.finder.porsche.com`), sem copiar os bytes da fotografia para o repositório. O uso da imagem no portfólio deve respeitar os direitos do fotógrafo/titular. Se a URL externa ficar indisponível, o fundo gráfico em CSS permanece legível. A imagem não implica patrocínio ou vínculo oficial.
- Marcas nominativas citadas somente como referência ao conjunto de dados e projeto de estudo.

## Conteúdo

- `index.html` — versão final para GitHub Pages
- `porsche_vendas_sanitizadas.csv` — base auditável
- `README.md` — funcionalidades e metodologia
- `VALIDACAO.md` — checklist de testes
- `preview-desktop.png`, `preview-mobile.png` — capturas de tela da versão quando disponíveis

## Atualização visual · Midnight Edition (26/11/2026)

- Tema escuro aplicado **a todo o site**: navegação, seções, painéis, KPIs, filtros, tabela, ranking, rodapé e cores internas dos três gráficos Canvas.
- Cores dominantes: preto profundo (`#080a0e`), grafite (`#171b22`) e vermelho esportivo (`#ec2948`) em pequenos destaques.
- Capa: tentativa progressiva de carregar imagem de alta resolução do Porsche 718 Cayman GT4 RS vermelho/preto via Porsche Finder (`3840`, `2560`, `1920`), evitando aceitar miniaturas inferiores a 1600 px como se fossem HD.
- Quando a Porsche Finder não serve fotos maiores, o sistema tenta uma imagem real alternativa de resolução alta de [Collecting Cars](https://collectingcars.com/for-sale/2023-porsche-718-cayman-gt4-rs-2) e [Porsche Newsroom](https://newsroom.porsche.com/en_AU/2023/products/porsche-718-cayman-gt4-rs-product-highlights-30846.html). A miniatura Porsche Finder de 960 px é recurso de emergência. Todas as fotos são externas e sujeitos a licenças/direitos dos respectivos titulares.
- A imagem externa não pôde ser carregada no navegador de teste local (restrição de rede), então é importante conferir a nitidez na versão publicada.

### Publicação

- GitHub Pages: https://lucaalima201-create.github.io/porsche-sales-intelligence/
- Repositório: https://github.com/lucaalima201-create/porsche-sales-intelligence

Projeto educacional independente, não afiliado à Porsche.