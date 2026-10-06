# 📊 Análise de Vendas - Power BI

## 📌 Sobre o projeto

Projeto desenvolvido em Power BI para analisar o desempenho de vendas de uma empresa utilizando uma base de dados fictícia.

O dashboard permite analisar faturamento, custos, lucro, descontos, produtos, regiões, clientes e vendedores, apoiando a identificação de indicadores e padrões de desempenho.

## 🖼️ Dashboard

### 📊 Dashboard interativo

[🔗 Visualizar Dashboard no Power BI](https://app.powerbi.com/view?r=eyJrIjoiODJmMmZlZWUtNDhlNi00MDBjLWI1ZTctYzA4ZjQ2ZGI1NTNmIiwidCI6IjUwMWRjZjJhLWI1ZWUtNGEyNC1hZjQzLTJiMWY1NTQ3ZTQxNSJ9)

### Visão Geral

![Visão Geral](imagens/Página%201%20-%20Faturamento.png)

### Análise de Vendas

![Análise de Vendas](imagens/Página%202%20-%20Vendas.png)

## 🛠️ Ferramentas utilizadas

- Power BI
- Power Query
- DAX
- Excel

## 🧩 Modelagem e desenvolvimento

O projeto foi desenvolvido utilizando:

- Tratamento e transformação dos dados no Power Query
- Modelagem de dados e criação de relacionamentos
- Criação de medidas e indicadores utilizando DAX
- Desenvolvimento de tabela calendário
- Criação de KPIs e visualizações interativas
- Organização do projeto em formato PBIP para versionamento no GitHub

## 📊 Análises realizadas

- Faturamento por mês
- Faturamento por categoria
- Faturamento por região
- Top 10 produtos
- Análise de descontos
- Vendas por região
- Análise de vendedores

## 📈 Principais indicadores

| Indicador | Resultado |
|---|---:|
| Faturamento | R$ 2.604.542,59 |
| Custo | R$ 1.726.017,35 |
| Lucro | R$ 878.525,24 |
| Margem | 33,73% |
| Vendas realizadas | 1.000 |
| Produtos vendidos | 2.614 |
| Clientes | 12 |
| Ticket médio | R$ 2.604,54 |

## 📁 Estrutura do projeto

```text
analise-vendas-power-bi/
├── dashboard/
│   └── T1_Relatório_Vendas.pbix
├── imagens/
│   ├── Página 1 - Faturamento.png
│   └── Página 2 - Vendas.png
├── dados/
│   └── Base_Vendas_Projeto_Power_BI.xlsx
├── projeto-power-bi/
│   ├── T1_Relatório_Vendas.Report/
│   └── T1_Relatório_Vendas.SemanticModel/
└── README.md
