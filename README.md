# 🎬 Análise de Sentimentos em Larga Escala com PySpark e NLP



# 🎬 Análise de Sentimentos em Larga Escala com PySpark e NLP

![Nuvem de Palavras do Dataset](wordcloud_movies.jpg)

*Nuvem de palavras gerada a partir dos depoimentos processados, destacando os termos mais frequentes após a limpeza de StopWords.*


Este projeto implementa um pipeline completo de Processamento de Linguagem Natural (NLP) para classificar sentimentos em avaliações de filmes (IMDB). A solução utiliza a biblioteca MLlib do Apache Spark para garantir escalabilidade e processamento distribuído.

## 🛠️ Tecnologias Utilizadas
* **Python**
* **Apache Spark (PySpark)**
* **Spark MLlib** (Machine Learning)
* **NLP (Natural Language Processing)**

## 🚀 O Pipeline de Dados
Para transformar texto bruto em previsões precisas, estruturei uma esteira de processamento (Pipeline) composta por:

1.  **Limpeza (Regex):** Tratamento de caracteres especiais e ruídos textuais.
2.  **Tokenização:** Segmentação das frases em unidades de palavras.
3.  **StopWords:** Remoção de termos irrelevantes (artigos, conectivos) para focar no significado.
4.  **HashingTF:** Conversão de texto em vetores numéricos de frequência.
5.  **TF-IDF:** Ponderação estatística para destacar termos de maior relevância semântica.
6.  **Decision Tree Classifier:** Modelo de aprendizagem supervisionada para a classificação final.

## 📊 Performance e Validação
O modelo foi validado utilizando uma divisão de 70% para treino e 30% para teste, garantindo que a inteligência artificial fosse testada em dados inéditos. Atualmente, o modelo atinge uma **acurácia de ~67%**.

---

> **Nota de Estudo:** Este projeto faz parte do meu aprendizado contínuo em Engenharia de Dados e IA, focado em arquiteturas distribuídas.
>
> **🚀 Melhoria Implementada:** Para elevar a performance do modelo original, realizei uma otimização no estágio de vetorização (`HashingTF`), expandindo o vocabulário de 1.000 para **10.000 features**. Essa alteração reduziu a taxa de colisão de termos e permitiu que a Árvore de Decisão capturasse nuances mais finas nos textos, resultando em predições mais robustas para comentários inéditos.

---

## 📂 Como Executar
1. Certifique-se de ter o ambiente Spark configurado (ou use o Google Colab).
2. Carregue o dataset de reviews.
3. Execute as células do pipeline para treinar e testar o modelo.
