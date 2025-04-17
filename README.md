📊 Este dashboard foi desenvolvido em Power BI para análise financeira de empresas listadas na B3, utilizando como fonte os dados públicos disponibilizados pela CVM. O objetivo é oferecer uma visão gerencial e estratégica com base nas Demonstrações Financeiras Padronizadas (DFP), com foco especial na DFC (Demonstração do Fluxo de Caixa).

🔍 Principais Indicadores Disponíveis:
Receita Líquida
Lucro / Prejuízo Líquido
Custos e Despesas Operacionais
EBITDA
Margem Líquida e Margem Operacional
Variação YoY (Year over Year) de Receita e Lucro
Ranking de empresas com maior lucratividade
Evolução temporal de desempenho financeiro
Análise setorial com filtros dinâmicos por ano, setor e empresa

⚙️ Estrutura Técnica e Pipeline de Dados
Para garantir escalabilidade e dados atualizados, foi construído um pipeline automatizado com as seguintes etapas:

1. Coleta Automatizada (Python):
Script desenvolvido em Python para download automático dos arquivos DFP da CVM (2019 a 2023).
Extração e leitura dos arquivos em CSV utilizando pandas.
Unificação e limpeza dos dados em um DataFrame consolidado.

2. Carga no Data Warehouse (Google BigQuery):
Utilização de autenticação via google.oauth2 e integração com pandas_gbq para envio dos dados.
Dados brutos foram armazenados em uma tabela raw_dfc.
Pré-processamento com SQL para normalização e estruturação dos dados, facilitando o uso no Power BI.

3. Visualização e Análise (Power BI):
Conexão direta com o BigQuery para acesso em tempo real aos dados tratados.
Criação de medidas DAX para cálculo de margens, comparativos YoY, e métricas de desempenho.
Interface interativa, com filtros por ano, setor e empresa, além de gráficos comparativos e indicadores-chave.

📌 Tecnologias Utilizadas: Python · Pandas · Google BigQuery · SQL · Looker Studio
📂 Objetivo: Criar um ambiente de análise robusto, dinâmico e automatizado para tomada de decisões baseada em dados financeiros oficiais.
