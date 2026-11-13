# Análise de Vendas em Power BI

Dashboard de desempenho comercial de uma distribuidora B2B de produtos de escritório e tecnologia (base fictícia): 1.000 vendas para 12 clientes corporativos, de janeiro a dezembro de 2025.

O objetivo é responder a quatro perguntas de negócio:

1. Quais produtos, categorias e regiões sustentam o faturamento?
2. A política de descontos traz volume ou apenas reduz a margem?
3. Qual é o grau de dependência dos principais clientes?
4. Como o resultado varia entre vendedores e ao longo do ano?

**[Abrir o dashboard publicado](https://app.powerbi.com/view?r=eyJrIjoiY2Q2Nzc2ZTQtNjA4NC00M2RmLWJhZDgtYWJmZTU3NGE5OTFmIiwidCI6IjUwMWRjZjJhLWI1ZWUtNGEyNC1hZjQzLTJiMWY1NTQ3ZTQxNSJ9)**

![Página de faturamento](imagens/faturamento.png)

## Resultados do período

| Faturamento | Lucro | Margem | Vendas | Ticket médio |
|---:|---:|---:|---:|---:|
| R$ 2,60 mi | R$ 878,5 mil | 33,7% | 1.000 | R$ 2.604,54 |

## O que os dados mostram

**Um único produto responde por 40% da receita e tem a menor margem do portfólio.**
O Notebook Pro 14 gerou R$ 1,03 milhão (39,7% do faturamento), com margem de 29,4%. Os acessórios têm a melhor margem (43,9%), mas representam apenas 11% da receita.

**O desconto reduz a margem sem aumentar o volume.**
Mais da metade das vendas (53,5%) teve algum desconto. A margem cai de 37,1% nas vendas sem desconto para 26,4% nas vendas com 15%, enquanto a quantidade média por pedido fica praticamente igual em todas as faixas (cerca de 2,6 itens).

**A receita está concentrada em poucos clientes.**
Os três maiores clientes somam 31,7% do faturamento. Na região Norte, toda a receita vem de um único cliente, o que torna o resultado da região vulnerável a uma eventual perda dessa conta.

**Os vendedores praticam políticas de desconto diferentes.**
Carla lidera em faturamento (18,8% do total). Felipe concede o menor desconto efetivo (3,4%) e tem a melhor margem da equipe (35,1%). Ana e Eduarda concedem os maiores descontos (6,4% e 6,2%), e Eduarda tem a menor margem (32,4%).

**A sazonalidade é leve.**
Março e setembro foram os meses mais fortes, com cerca de 10% da receita anual cada. Abril e junho foram os mais fracos.

## Recomendações

- Rever a política de descontos: definir limites por faixa e acompanhar a margem por vendedor, já que o desconto não está gerando aumento de volume.
- Estimular a venda de acessórios junto com notebooks e monitores, para elevar a margem média dos pedidos.
- Reduzir a dependência dos maiores clientes, com prospecção ativa principalmente na região Norte.

## Página de vendas

![Página de vendas](imagens/vendas.png)

## Como foi construído

- **Power Query:** a base em Excel é lida a partir de um parâmetro (`CaminhoBase`); as tabelas de vendedores e de calendário são derivadas da consulta de vendas, sem reler o arquivo.
- **Modelagem:** tabela fato `Venda` relacionada às dimensões `Data` e `Vendedores`, com uma tabela dedicada para as medidas. A tabela `Data` é um calendário contínuo, marcado como tabela de datas, e a data/hora automática do Power BI está desativada.
- **DAX:** medidas de faturamento, custo, lucro, margem, ticket médio, quantidade de vendas e clientes, percentual de vendas com desconto e desconto efetivo, com formatos de moeda e percentual definidos no próprio modelo.
- **Versionamento:** o relatório também está salvo no formato PBIP (TMDL), o que permite ler o modelo e as medidas diretamente pelo GitHub.

Exemplo de medida:

```dax
Desconto efetivo % =
DIVIDE ( [Desconto total], SUM ( Venda[Valor_Bruto] ) )
```

## Estrutura do repositório

```text
analise-vendas-power-bi/
├── dados/              base-vendas.xlsx
├── dashboard/          relatorio-vendas.pbix
├── imagens/            Capturas das páginas do dashboard
└── projeto-power-bi/   relatorio-vendas.pbip (relatório e modelo em formato PBIP)
```

## Como abrir

- **Versão publicada:** use o link no início desta página; não é preciso instalar nada.
- **Power BI Desktop:** baixe `dashboard/relatorio-vendas.pbix` e abra no Power BI Desktop (Windows).
- **Formato PBIP:** abra `projeto-power-bi/relatorio-vendas.pbip`.

Para atualizar os dados, ajuste o parâmetro `CaminhoBase` (Transformar dados > Gerenciar parâmetros) com o local onde você salvou `dados/base-vendas.xlsx`.

## Autora

**Isabela Medeiros** · [LinkedIn](https://www.linkedin.com/in/isabela-medeiros-de-araujo)
