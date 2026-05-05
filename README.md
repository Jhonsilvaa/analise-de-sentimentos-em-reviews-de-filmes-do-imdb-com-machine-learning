# Análise de Sentimentos em Reviews do IMDb com Machine Learning

No ambiente digital atual, milhões de usuários compartilham suas opiniões sobre filmes em plataformas como o IMDb. Essas reviews fornecem uma rica fonte de dados textuais, mas seu grande volume torna a análise manual impraticável.

Saber rapidamente se uma crítica é positiva ou negativa é importante para estúdios de cinema, plataformas de streaming e espectadores que buscam recomendações. O objetivo deste projeto é desenvolver um modelo de classificação binária capaz de identificar o sentimento expresso em cada review.

<p align="center">
<img src="https://github.com/user-attachments/assets/690c4482-330e-4998-a389-2590bbd4dd15" width="50%">
</p>

---

## 📖 Visão Geral

| | |
|---|---|
| **Problema** | Classificação binária — review positiva ou negativa? |
| **Dataset** | 10.000 reviews do IMDb |
| **Melhor modelo** | LightGBM |
| **Melhor F1-score** | **0.85** |
| **Abordagem NLP** | Pipeline completo com lematização por POS tag + TF-IDF |

---

## 🔍 Abordagem

### 1. Análise Exploratória
- Distribuição de sentimentos positivos e negativos
- Análise de frequência de palavras por classe
- WordCloud

### 2. Pré-processamento de Texto
Pipeline NLP completo aplicado a cada review:
- Conversão para minúsculas
- Remoção de tags HTML e URLs
- Expansão de **chatwords**
- Conversão de **emojis** para texto
- Expansão de **contrações**
- Remoção de pontuação e números
- Tokenização
- Remoção de **stopwords**
- **Lematização com POS tag**
- **TF-IDF**

### 4. Modelagem
- Comparação de classificadores: AdaBoost, XGBoost, LightGBM, MultinomialNB
- Otimização de hiperparâmetros com **Busca Bayesiana (skopt)**


---

## 📈 Resultados

| Métrica | Valor |
|---|---|
| F1 | **85%** |
| Melhor modelo | LightGBM |

---

## 📓 Notebook

🔗 [Ver projeto completo no Colab](http://bit.ly/4enfed4)

---

## 📝 Artigo

Documentação completa com pipeline NLP, decisões técnicas e avaliação dos modelos:

🔗 [Ler no Medium](https://medium.com/@jhonatasassumpcao/an%C3%A1lise-de-sentimentos-em-reviews-de-filmes-do-imdb-com-machine-learning-d05defc50c6a)

---

## ⚡️ Tecnologias

`Python` `Scikit-learn` `XGBoost` `LightGBM` `NLTK` `Scikit-optimize` `Pandas` `Seaborn` `WordCloud`

---

## 👨‍💻 Autor

**Jhonatas Assumpção**

[![GitHub](https://img.shields.io/badge/GitHub-Jhonsilvaa-181717?style=flat&logo=github)](https://github.com/Jhonsilvaa)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Jhonatas-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/jhonatas-assumpção-da-silva-62a7931b3)
[![Medium](https://img.shields.io/badge/Medium-@jhonatasassumpcao-000000?style=flat&logo=medium)](https://medium.com/@jhonatasassumpcao)

---

## 📄 Licença

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

Este projeto está licenciado sob a **[GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0)** — consulte o arquivo [LICENSE](https://github.com/Jhonsilvaa/analise-de-sentimentos-em-reviews-de-filmes-do-imdb-com-machine-learning/blob/main/LICENSE) para mais detalhes.
