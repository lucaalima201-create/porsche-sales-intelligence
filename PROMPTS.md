# Prompts e decisões — Porsche Sales Intelligence

## Pedido inicial (briefing da DIO)

> Transformar uma base sanitizada de 100 registros de vendas de veículos Porsche em uma dashboard interativa, em um único arquivo HTML, com três perguntas de negócio, gráficos, indicadores de topo, filtros e visual coerente; preparar o conteúdo para publicação no GitHub Pages.

## Prompt estruturado para geração

> Crie uma dashboard em **um único arquivo `index.html`**, com HTML, CSS e JavaScript puro, sem CDNs, sem requisições externas e sem dependências. Use apenas os 100 registros sanitizados: ID, data, modelo, ano do modelo, preço (USD), método de pagamento, cidade e estado. Incorpore os registros no próprio HTML em formato JavaScript, como valores — nunca fórmulas do Excel.
>
> A página deve responder claramente a estas três perguntas de negócio, cada qual com uma visualização: **(1) quais modelos geram mais receita?** — barras horizontais com receita (USD); **(2) quais estados concentram mais vendas?** — ranking de número de vendas por estado; **(3) quais métodos de pagamento são mais utilizados?** — rosca com participação percentual por número de registros.
>
> Inclua filtros combináveis por modelo, estado, cidade, ano do modelo, ano da venda e método de pagamento; indicadores de quantidade de vendas, receita, ticket médio e estados atendidos; texto de interpretação dinâmica; botão limpar; exportação dos dados filtrados em CSV; e tabela de auditoria paginada.
>
> Use um design original, premium, responsivo, com fundo grafite/preto, contraste alto e destaque vermelho, inspirado no universo automotivo sem copiar páginas oficiais ou logotipos. Formate a moeda explicitamente em USD.
>
> Preserve registros com data inválida nos totais e ofereça o filtro "Sem data". Trate filtros sem resultados sem quebrar os gráficos. Inclua aviso de que o conjunto é educacional e de que existem datas futuras na base. Teste cálculos, filtros, CSV e responsividade antes de entregar.

## Evolução do pedido até a versão final

| Etapa | Decisão | Motivo |
| --- | --- | --- |
| 1 — perguntas | Receita por modelo, volume por estado e mix de pagamentos | Produz três respostas de negócio distintas e complementares. |
| 2 — dados | Manter campos essenciais e descartar identificadores pessoais | Reduz dados incorporados e evita exposição desnecessária. |
| 3 — tempo | Separar ano do modelo de ano da venda | Evita confundir o veículo com a data da transação. |
| 4 — inconsistências | Manter datas `INVALID` como ausentes e expô-las no recorte | Evita excluir vendas silenciosamente. |
| 5 — navegação | Acrescentar seis filtros, limpar, CSV e paginação | Permite investigar e auditar os resultados. |
| 6 — robustez | HTML autônomo + testes no Chromium | Funciona no Pages e offline, inclusive no celular. |

## Caminho de IA empregado

Foi usado o **ChatGPT para desenvolver o HTML diretamente**, com validação automatizada do comportamento. Não foi utilizado Canvas e não foi criado um agente com skill personalizada. A opção pelo HTML direto preservou a exigência de arquivo único e simplificou a execução.

## Limitação declarada

A planilha `.xlsx` fornecida pela DIO não pôde ser obtida diretamente neste ambiente. A base numérica foi reconstruída dos 100 registros sanitizados presentes em uma dashboard pública derivada do mesmo exercício. Para fins de rastreabilidade, o README identifica a origem utilizada e recomenda uma comparação com a planilha original antes da submissão definitiva.