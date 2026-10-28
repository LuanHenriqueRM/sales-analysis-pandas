# 📊 Análise de Vendas de uma Loja de Eletrônicos

Análise exploratória de dados de vendas de uma rede de lojas de eletrônicos dos EUA, com centenas de milhares de pedidos ao longo de 12 meses. 
O objetivo é transformar dados brutos em respostas para perguntas de negócio, usando Python, Pandas e Matplotlib.

## 🎯 Perguntas de negócio

1. Qual foi o melhor mês de vendas?
2. Qual cidade teve o maior faturamento?
3. Em qual horário do dia há mais pedidos?
4. Quais produtos costumam ser comprados juntos?
5. Quais produtos são mais vendidos?

## 🗂️ Sobre os dados

Os dados vêm do dataset [Electronics Store Sales Dataset for EDA](https://www.kaggle.com/datasets/sinjoysaha/sales-analysis-dataset/data), publicado no Kaggle. 
Estão divididos em 12 arquivos CSV, um por mês, e cada linha representa um item de um pedido.

## 🧹 Tratamento dos dados      

- Mesclagem dos 12 arquivos mensais em um único DataFrame
- Remoção de linhas de cabeçalho repetidas e de valores nulos
- Conversão de tipos: `Order Date` para data/hora e `Quantity Ordered` e `Price Each` para numérico
- Criação de novas colunas:
  - `Mes`: número do mês, extraído da data
  - `Hora`: hora do pedido
  - `Sales`: faturamento da linha (`Quantity Ordered × Price Each`)
  - `City`: cidade e estado, extraídos do endereço (ex.: `Portland (OR)`), para não misturar cidades homônimas

## 🔍 Principais resultados

- **Melhor mês:** Dezembro, com mais de US$ 4.000.000 em faturamento
- **Cidade com mais vendas:** São Francisco (CA) com mais de US$ 8.000.000 de vendas
- **Horário de pico:** 12h e 19h, com destaque para 19h com o maior número de pedidos
- **Pares de produtos mais comprados juntos:** Lightning Charging Cable e iPhone, com 1015 registros de pedidos juntos
- **Produto mais vendido:** O produto campeão de vendas foi AAA Batteries (4-pack), com 31017 pedidos.

## 🛠️ Tecnologias

- Python 
- Pandas
- Matplotlib
- Jupyter Notebook

## ▶️ Como executar

```bash
# 1. Clone o repositório
git clone <url-do-repositorio>
cd <nome-da-pasta>

# 2. Crie e ative um ambiente virtual
python -m venv .venv

# 3. Instale as dependências
pip install -r requirements.txt

# 4. Abra o notebook e execute de cima para baixo
jupyter notebook analise.ipynb
```

> Os arquivos CSV devem estar na pasta `dados/`. Se ela não vier com o repositório, baixe o dataset no [Kaggle](https://www.kaggle.com/datasets/sinjoysaha/sales-analysis-dataset/data) e coloque os 12 arquivos mensais nela.
