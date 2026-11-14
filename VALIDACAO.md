# Verificação funcional

Testes feitos em Chromium headless sobre o HTML completo, incluindo execução do script e inspeção dos elementos renderizados.

| Cenário | Resultado |
| --- | --- |
| HTML inicia sem erro de JavaScript | **Passou** |
| Total inicial de vendas | **100** |
| Receita total inicial | **US$ 12.827.800,50** |
| Ticket médio inicial | **US$ 128.278,01** |
| Estados atendidos | **33** |
| Datas inválidas sinalizadas | **24** |
| Gráfico de modelos | **8 barras visíveis (40 modelos)** |
| Ranking de estados | **8 barras visíveis (33 estados)** |
| Gráfico de pagamentos | **9 segmentos/legendas** |
| Filtros disponíveis | **Modelo, estado, cidade, ano do modelo, ano da venda, pagamento** |
| Selecionar estado CA | **16 vendas; US$ 1.973.350,00** |
| Combinar CA e 911 Dakar | **1 venda** |
| Limpar filtros | **Retorno às 100 vendas** |
| Selecionar ano da venda = Sem data | **24 vendas** |
| Exportar CSV filtrado | **Download de `porsche-vendas-filtradas.csv` disparado** |
| Renderização mobile 390 px | **Sem overflow horizontal** |

## Pontos para conferir após a publicação

1. Abrir a URL gerada pelo Pages sem erro 404.
2. Confirmar que o botão de limpar restaura 100 registros.
3. Aplicar o filtro `Estado = CA` e conferir 16 vendas.
4. Clicar em `EXPORTAR CSV` e abrir o download.
5. Conferir se as imagens e arquivos documentados no README existem no repositório.

Os screenshots em `assets/` são evidências das versões desktop, com filtro `CA` e mobile. O uso de uma cópia pública sanitizada da base, em vez de leitura direta do XLSX da DIO, está declarado no README.