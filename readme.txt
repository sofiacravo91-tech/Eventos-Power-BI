# Análise de Vendas de Evento — Power BI

## Objetivo
Este projeto tem como objetivo analisar os padrões de vendas de um evento, incluindo informações sobre pedidos, canais, locais de venda, itens e horários. O objetivo principal é criar visualizações que permitam entender:
- Quantidade total de vendas
- Distribuição de vendas por hora
- Performance de canais e locais de venda
- Itens e categorias mais vendidos

## Estrutura do Projeto

- `datasets/` → Contém os dados de entrada (CSV de exemplo)
- `pbix/` → Arquivo Power BI com todos os dashboards e medidas
- `medidas_dax/` → Lista de medidas DAX usadas no Power BI
- `images/` → Prints dos gráficos e visualizações
- `README.md` → Este arquivo explicativo

## Principais Métricas e Medidas

Exemplos de medidas DAX criadas:

- **Total Quantidade**
```DAX
Total Quantidade = SUM(Fato_Vendas[quantidade])

Pedidos Únicos

Pedidos Únicos = DISTINCTCOUNT(Fato_Vendas[pedido_id])


Qtd Média por Pedido

Qtd Média por Pedido = DIVIDE([Total Quantidade], [Pedidos Únicos])


Itens Distintos

Itens Distintos = DISTINCTCOUNT(Fato_Vendas[item])

Visualizações principais

Heatmap de Vendas por Hora
Mostra os horários de pico de vendas ao longo do evento.

Top Itens e Categorias
Gráficos de barras/colunas mostrando quais produtos venderam mais.

Análise de Canal e Local de Venda
Matrizes ou mapas destacando onde e por qual canal as vendas ocorreram.

KPIs Executivos
Cards com Total de Vendas, Pedidos Únicos, Qtd Média por Pedido e Itens Distintos.

Observações

Os dados usados são fictícios, preservando confidencialidade.

Estrutura pensada para crescimento futuro: permite incluir múltiplos eventos, mais datas e mais locais sem alterar o modelo.
