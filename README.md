# 📊 Análise de Vendas | Power BI

Projeto desenvolvido para analisar o desempenho comercial de uma empresa
a partir de uma base de dados fictícia.

O projeto foi construído no Power BI, passando pelo tratamento dos dados,
modelagem, criação de medidas em DAX e desenvolvimento do dashboard.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-245373?style=for-the-badge)
![Power Query](https://img.shields.io/badge/Power%20Query-245373?style=for-the-badge)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)

---

## 📊 Dashboard

[**🔗 Acessar dashboard interativo no Power BI**](https://app.powerbi.com/view?r=eyJrIjoiODJmMmZlZWUtNDhlNi00MDBjLWI1ZTctYzA4ZjQ2ZGI1NTNmIiwidCI6IjUwMWRjZjJhLWI1ZWUtNGEyNC1hZjQzLTJiMWY1NTQ3ZTQxNSJ9)

### Faturamento

![Dashboard de faturamento](imagens/Página%201%20-%20Faturamento.png)

### Vendas

![Dashboard de vendas](imagens/Página%202%20-%20Vendas.png)

---

## 🔎 Principais análises

- Evolução do faturamento ao longo do ano
- Faturamento por categoria
- Faturamento por região
- Top 10 produtos
- Análise de descontos
- Desempenho dos vendedores
- Indicadores de vendas, custos e lucro

---

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

---

## 🧩 Tratamento e modelagem

Os dados foram tratados no Power Query e organizados em um modelo
relacional no Power BI.

Foram utilizadas medidas em DAX para criação dos principais indicadores
do dashboard, como faturamento, lucro, margem, ticket médio e quantidade
de vendas.

O projeto também está disponível em formato **PBIP**, permitindo visualizar
a estrutura do relatório e as definições do modelo diretamente no GitHub.

---

## 🛠️ Ferramentas

**Power BI** · **Power Query** · **DAX** · **Excel**

---

## 📁 Estrutura do projeto

```text
analise-vendas-power-bi/
│
├── dados/
│   └── Base_Vendas_Projeto_Power_BI.xlsx
│
├── dashboard/
│   └── T1_Relatório_Vendas.pbix
│
├── imagens/
│   ├── Página 1 - Faturamento.png
│   └── Página 2 - Vendas.png
│
├── projeto-power-bi/
│   ├── T1_Relatório_Vendas.Report
│   ├── T1_Relatório_Vendas.SemanticModel
│   └── T1_Relatório_Vendas.pbix
│
└── README.md
