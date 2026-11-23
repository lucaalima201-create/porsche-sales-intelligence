# Porsche Sales Intelligence — Dashboard Interativa

**Dashboard interativa em HTML único — consulte `index.html`.**

> Dashboard educacional e independente para analisar 100 registros de vendas de veículos Porsche. Desenvolvida em **HTML, CSS e JavaScript puro**, em um único `index.html`, com dados incorporados e sem bibliotecas externas.

## 🌐 Dashboard Publicada

**Status: Publicada via GitHub Pages ✅**

Acesse a dashboard interativa Porsche Sales Intelligence pelo link:

**[Porsche Sales Intelligence — Dashboard Interativa](https://lucaalima201-create.github.io/porsche-sales-intelligence/)**

A aplicação foi desenvolvida em HTML, CSS e JavaScript, com visual responsivo, indicadores de desempenho e filtros interativos para análise dos dados de vendas.

## 🎯 Perguntas de negócio

| Pergunta | Visualização | Por que importa? |
| --- | --- | --- |
| **1. Quais modelos geram mais receita?** | Barras horizontais: receita por modelo (USD) | Mostra quais veículos mais contribuem financeiramente para o mix de vendas. |
| **2. Quais estados concentram mais vendas?** | Ranking por estado: número de registros | Identifica os mercados mais presentes na amostra. |
| **3. Quais métodos de pagamento são mais usados?** | Gráfico de rosca com percentuais | Ajuda a entender os meios de pagamento predominantes. |

As três visualizações, os indicadores e a tabela são atualizados simultaneamente ao aplicar os filtros.

## ✨ Funcionalidades

- **6 filtros combináveis:** modelo, estado, cidade, ano do modelo, ano da venda e pagamento.
- **4 indicadores principais:** vendas, receita registrada, ticket médio e estados atendidos.
- **3 visualizações de negócio** com leitura automática do líder de cada ranking.
- **Tabela paginada** para conferir cada registro e os dados exibidos.
- **Exportação CSV** da seleção atual, sem depender de servidor.
- **Botão de limpar filtros**, tratamento de seleções sem resultados e destaque de datas inválidas.
- **Layout responsivo**, paleta grafite, preto, branco e vermelho, e tipografia de sistema.
- **Execução offline:** basta abrir `index.html` no navegador.

## 📊 Base e principais números

| Indicador | Total da base |
| --- | ---: |
| Registros de vendas | **100** |
| Receita registrada | **US$ 12.827.800,50** |
| Ticket médio por venda | **US$ 128.278,01** |
| Estados diferentes | **33** |
| Datas inválidas | **24** |

> Estes valores são derivados da **base de exercício** e não representam dados oficiais da Porsche. Receita é soma dos preços registrados, sem deduções, e não representa lucro ou faturamento efetivamente realizado.

### Proveniência e tratamento dos dados

- **Base do enunciado:** [planilha Porsche disponibilizada pela DIO](https://hermes.dio.me/files/assets/8683bed0-cc33-4e06-bca9-04db9c31f9e2.xlsx).
- **Fonte efetivamente processada nesta implementação:** os **100 registros sanitizados embutidos** no HTML público do projeto educacional [`michaelfellype/dashboard_porsche_sales`](https://github.com/michaelfellype/dashboard_porsche_sales/blob/main/index.html), que documenta uso da base do mesmo desafio. **O download direto da planilha da DIO não foi possível neste ambiente**; por isso, a equivalência registro a registro com o XLSX original ainda não foi verificada aqui.
- **Colunas mantidas:** `id`, `date`, `model`, `year`, `price`, `payment`, `city`, `state`.
- **Colunas descartadas:** quaisquer informações de clientes, vendedores ou outros campos brutos/sensíveis não necessários à análise.
- **Normalizações:** `price` em número decimal e USD, `year` em número inteiro; datas ISO `AAAA-MM-DD` ou ausentes para `INVALID`.
- **Datas inválidas:** 24 registros continuam nas métricas gerais; quando um ano da venda é escolhido, aparecem somente as datas correspondentes (inclusive a opção **Sem data**).
- **Datas futuras:** mantidas como aparecem no conjunto de exercício, inclusive em 2027; não significam vendas realizadas no mundo real.
- **Sem fórmulas do Excel:** o CSV usa valores simples; a página embute todos os 100 objetos JavaScript como valores.

Para comparação oficial, substitua a base do exercício pelos campos sanitizados diretamente no XLSX original antes de uma submissão que exija essa verificação.

## 🤖 IA utilizada, prompt e refinamentos

**Ferramenta:** ChatGPT, com geração de código e testes automatizados; **sem Canvas e sem agente personalizado**. O HTML foi produzido diretamente, sem copiar a implementação visual de terceiros.


## 🖼️ Evidências de funcionamento

### Evidências de funcionamento

As capturas de tela desktop, filtro CA e versão mobile já foram geradas, mas ainda precisam ser anexadas à pasta `assets/` do repositório. A validação funcional está registrada em [VALIDACAO.md](VALIDACAO.md).

**Testes executados:** renderização sem erros de JavaScript, conferência dos 100 registros, da receita total, dos seis controles, do gráfico por pagamento, seleção de `CA` (**16 vendas**), seleção de `Sem data` (**24 registros**), botão limpar, download de CSV e ausência de rolagem horizontal em tela de 390 px. Resultados detalhados em [VALIDACAO.md](VALIDACAO.md).

## 📁 Estrutura

```text
porsche-sales-intelligence/
├── index.html
├── README.md
├── PROMPTS.md
├── VALIDACAO.md
└── dados/
    └── porsche_vendas_sanitizadas.csv

```


## 🛠️ Tecnologias

HTML5 · CSS3 · JavaScript ES2020 · SVG · GitHub Pages (publicação)

**Aviso:** projeto educacional independente, sem vínculo com a Porsche AG.