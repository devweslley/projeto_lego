# Análise de Dados LEGO com Big Data e Machine Learning

## 1. Sobre o projeto

Este projeto foi desenvolvido como trabalho final da pós-graduação em Inteligência Artificial, Big Data e Data Engineering da PUC-SP. Utiliza dados da plataforma Rebrickable para explorar características dos conjuntos LEGO com Apache Spark, Spark SQL, RDDs, Pandas, NumPy e visualizações em Python.

O projeto percorre as etapas de obtenção e preparação dos dados, análise exploratória, engenharia de atributos, construção de modelos de Machine Learning e comunicação dos resultados.

## Integrantes do grupo

- Anderson Almeida Costa
- Rafael de Sousa Camelo
- Roberto Freires Batista
- Wesley Rodrigues Silva
  
## 2. Objetivo

Investigar padrões nos conjuntos LEGO e avaliar se características disponíveis no lançamento ajudam a estimar a recorrência dos produtos no catálogo.

A recorrência é definida pela quantidade de anos distintos em que um produto aparece durante uma janela de observação de oito anos. Essa variável é uma aproximação da permanência no catálogo, não uma medida direta de vendas, receita ou sucesso comercial.

## 3. Perguntas analisadas

- Quais são os maiores conjuntos LEGO em quantidade de peças?
- Quais temas apresentam maior quantidade de conjuntos?
- Como os conjuntos se distribuem ao longo dos anos?
- Quais materiais aparecem em maior quantidade nos inventários?
- Quais cores e peças são mais frequentes na base analisada?
- É possível identificar padrões que ajudem a estimar a recorrência dos produtos no catálogo?

## 4. Tecnologias utilizadas

- Python
- Apache Spark e Spark SQL
- RDDs
- Pandas e NumPy
- Seaborn e Matplotlib
- Spark MLlib
- Google Colab

## 5. Modelagem e resultados

Foram comparados três métodos: um baseline baseado na média do alvo no treino, uma Regressão Linear regularizada e uma Árvore de Decisão. A avaliação utilizou uma separação temporal entre treino e teste.

| Modelo | RMSE | MAE | R² | AUC |
|---|---:|---:|---:|---:|
| Baseline | 0,3213 | 0,1207 | -0,0020 | 0,5000 |
| Regressão Linear | 0,3177 | 0,1022 | 0,0202 | 0,7730 |
| Árvore de Decisão | 0,3192 | 0,1058 | 0,0114 | 0,7232 |

A Regressão Linear apresentou os melhores resultados entre os modelos avaliados. Apesar disso, os valores de R² indicam capacidade limitada de explicar a variação da recorrência. Os resultados devem ser interpretados considerando a forte concentração de produtos que aparecem em apenas um ano e o caráter aproximado da variável-alvo.

## 6. Principais conclusões

A análise exploratória permitiu identificar padrões de distribuição de conjuntos, temas e características dos produtos LEGO. Na etapa de Machine Learning, a Regressão Linear superou a Árvore de Decisão e o baseline nas métricas apresentadas.

A recorrência no catálogo não deve ser interpretada diretamente como sucesso comercial. Os resultados representam uma análise exploratória e podem ser aprofundados com novas variáveis e estratégias de modelagem.

## 7. Como reproduzir

1. Abra o notebook do projeto no Google Colab.
2. Disponibilize os arquivos de dados da Rebrickable utilizados na análise.
3. Execute as células na ordem apresentada, desde a preparação dos dados até a avaliação dos modelos.
4. Consulte as tabelas, visualizações e interpretações registradas em cada etapa.

**Notebook no Google Colab:** [Abrir notebook do projeto](https://colab.research.google.com/drive/15SPnILMrp0J4J9tCG7paveWrZaFkfSfP)

**Repositório GitHub:** https://github.com/devweslley/projeto_lego

## 8. Fonte dos dados

Os dados utilizados são provenientes da plataforma Rebrickable: https://rebrickable.com/downloads/

## 9. Contexto acadêmico

Projeto final da pós-graduação em Inteligência Artificial, Big Data e Data Engineering — PUC-SP.
