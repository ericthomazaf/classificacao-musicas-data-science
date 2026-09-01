# Classificação Preditiva de Músicas

Projeto de Ciência de Dados desenvolvido como parte do MVP da Pós-Graduação em Ciência de Dados e Analytics da PUC-Rio.

## Objetivo

Desenvolver um modelo de classificação binária capaz de categorizar músicas como **lentas** ou **agitadas**, utilizando atributos musicais e a métrica `valence` como referência para definição da variável alvo.

A proposta busca explorar a aplicação de Machine Learning na segmentação de músicas e na criação de playlists personalizadas.

## Dataset

O projeto utiliza o **Spotify Tracks Dataset**, disponibilizado pelo Kaggle.

O conjunto de dados possui **114.000 registros e 21 variáveis**, contendo informações sobre características musicais, popularidade e gênero das faixas.

Principais atributos utilizados no modelo:

- `popularity`
- `duration_ms`
- `danceability`
- `energy`
- `loudness`
- `acousticness`
- `instrumentalness`
- `liveness`
- `track_genre`

## Metodologia

O projeto foi desenvolvido seguindo as seguintes etapas:

1. Carregamento e exploração dos dados
2. Análise exploratória (EDA)
3. Criação da variável target a partir de `valence`
4. Engenharia e transformação de variáveis
5. Análise de correlação
6. Separação dos dados em treino e teste
7. Normalização das variáveis
8. Treinamento dos modelos
9. Avaliação dos modelos
10. Otimização de hiperparâmetros com Grid Search

## Modelos utilizados

Foram comparados três algoritmos de classificação:

- Regressão Logística
- K-Nearest Neighbors (KNN)
- Random Forest

Também foi realizada otimização do Random Forest utilizando `GridSearchCV`.

## Resultados

| Modelo | AUC | Acurácia |
|---|---:|---:|
| Regressão Logística | 0,80 | 72% |
| KNN | 0,81 | 75% |
| Random Forest | 0,83 | 74% |
| Random Forest + Grid Search | **0,91** | **82%** |

O melhor resultado foi obtido pelo **Random Forest otimizado**, utilizando:

- `max_depth = 15`
- `n_estimators = 300`

O modelo alcançou **AUC de 0,91 e acurácia de 82%**.

## Tecnologias

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## Arquivos

- `classificacao_musicas.ipynb` — notebook contendo toda a análise e desenvolvimento do modelo.

## Autor

Eric Thomaz Altines Figueiredo

Pós-Graduação em Ciência de Dados e Analytics — PUC-Rio
