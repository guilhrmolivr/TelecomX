# Análise de Churn de Clientes - Telecom X

## Introdução

Este projeto tem como objetivo analisar o problema de "Churn de Clientes" (cancelamento) na empresa Telecom X. A empresa enfrenta um alto índice de cancelamentos e precisa entender os fatores que levam a essa perda de clientes ao longo do tempo para desenvolver estratégias de retenção eficazes.

## Dados

Os dados utilizados nesta análise foram obtidos do seguinte URL: `https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/main/TelecomX_Data.json`.

## Limpeza e Tratamento dos Dados

As seguintes etapas de limpeza e tratamento foram realizadas:

- Importação das bibliotecas necessárias (pandas, requests, json, matplotlib, seaborn, numpy, plotly).
- Carregamento dos dados a partir do arquivo JSON.
- Normalização dos dados aninhados utilizando `pd.json_normalize`.
- Tradução dos nomes das colunas para português para facilitar a compreensão.
- Conversão da coluna `gasto_total` para o tipo numérico (`float64`), tratando erros com `errors='coerce'`.
- Conversão da coluna `idoso` para o tipo booleano.
- Remoção de linhas duplicadas com base no `id_Cliente`.
- Identificação e remoção de valores nulos na coluna `gasto_total`.
- Identificação e remoção de valores em branco na coluna `cancelamento`.
- Cálculo e adição da coluna `gasto_diario`, estimando o gasto diário do cliente.

## Análise Exploratória dos Dados

Foram realizadas diversas análises exploratórias para entender os padrões de churn e identificar fatores relevantes:

- **Visão Geral de Churn:** Gráfico de pizza mostrando a proporção de clientes que cancelaram e não cancelaram.
- **Taxa de Cancelamento por Gênero:** Análise da taxa de cancelamento entre homens e mulheres.
- **Taxa de Cancelamento em Idosos:** Comparação da taxa de cancelamento entre clientes idosos e não idosos.
- **Relação entre Meses de Contrato e Cancelamento:** Análise da taxa de cancelamento em relação ao tempo de contrato do cliente, visualizada em um histograma e um gráfico de linha da taxa de cancelamento por meses de contrato.
- **Taxa de Cancelamento por Meio de Pagamento:** Análise da taxa de cancelamento para diferentes formas de pagamento.
- **Quantidade de Clientes por Forma de Pagamento:** Gráfico de barras mostrando a distribuição de clientes por forma de pagamento.
- **Meses de Contrato vs Gastos Totais e Cancelamento:** Gráficos de dispersão explorando a relação entre meses de contrato, gastos totais e mensais, e o status de cancelamento.
- **Tipo de Contrato e Cancelamento:** Análise da relação entre o tipo de contrato e a taxa de cancelamento.
- **Taxa de Cancelamento por Tipo de Internet:** Análise da taxa de cancelamento com base no tipo de serviço de internet.

## Conclusões e Insights

Baseado na análise exploratória, os principais insights incluem:

- A taxa de cancelamento é ligeiramente maior entre mulheres.
- Clientes com mais de 65 anos apresentam uma taxa de cancelamento significativamente maior.
- Clientes com baixo tempo de contrato e alto gasto mensal representam um alto risco de churn.
- A forma de pagamento "Cheque Eletrônico" tem a maior taxa de cancelamento.
- Clientes com contratos de menor duração têm maior probabilidade de cancelar.
- O serviço de internet por fibra óptica está associado a uma alta taxa de cancelamento, indicando uma possível insatisfação com o custo-benefício.

## Recomendações

Com base nas conclusões, são propostas as seguintes recomendações para reduzir o churn:

- **Blindar o Início da Jornada do Cliente:** Implementar um plano de retenção focado nos primeiros 3 meses, oferecendo descontos ou benefícios para incentivar a permanência e a migração para contratos de maior duração.
- **Aumentar o Valor Percebido da Fibra Ótica:** Agregar serviços adicionais aos pacotes de Fibra Ótica (streaming, TV a cabo, suporte técnico 24 horas, etc.) para justificar o preço e aumentar a fidelidade do cliente.
- **Modernizar e Simplificar o Pagamento:** Incentivar a migração do "Cheque Eletrônico" para formas de pagamento mais modernas e automáticas (Débito Automático ou Cartão de Crédito) oferecendo pequenos descontos como incentivo.

Este README fornece um resumo do projeto. Para detalhes completos sobre o código e os resultados, consulte o notebook Python.
