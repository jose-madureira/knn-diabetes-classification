# Classificação de Diabetes com o Algoritmo KNN

Este repositório apresenta a aplicação de técnicas de Inteligência Artificial no contexto da saúde, com foco na construção de um modelo preditivo voltado à classificação de pacientes com ou sem diagnóstico de diabetes, utilizando o algoritmo supervisionado K-Nearest Neighbors (KNN). A proposta emerge da premissa de que a análise de dados médicos pode, quando bem estruturada, oferecer suporte relevante a processos diagnósticos e à tomada de decisão clínica.

## Delimitação do Problema

No cerne deste estudo, encontra-se a tarefa de classificar indivíduos em dois agrupamentos distintos:

- portadores de diabetes;
- não portadores.

Essa categorização é realizada a partir da análise de atributos coletados previamente, tais como níveis de glicose, pressão arterial, entre outros. A escolha do algoritmo KNN justifica-se por sua natureza baseada em instâncias e pela forma como explora a similaridade entre os dados históricos para prever novos casos.

## Objetivos Gerais e Específicos

- Desenvolver um modelo preditivo de classificação com base no algoritmo KNN.
- Realizar análise exploratória dos dados (EDA) a fim de identificar padrões, distribuições e outliers.
- Implementar validação cruzada como mecanismo de robustez da avaliação.
- Mensurar o desempenho do modelo a partir de métricas quantitativas: acurácia, precisão, recall e F1-score.
- Otimizar o parâmetro *K* por meio de busca sistemática.
- Confrontar os resultados do KNN com outros modelos clássicos de classificação, como Regressão Logística e Árvore de Decisão.
- Discutir, com base na literatura e na prática observada, as potencialidades e limitações da abordagem adotada.

## Fundamentos Metodológicos

O algoritmo KNN é caracterizado por ser não paramétrico, de natureza preguiçosa (*lazy learner*), o que implica dizer que não há, em sua essência, uma etapa de treinamento tradicional. A inferência ocorre no momento da predição, com base na análise da distância entre o novo exemplo e os exemplos do conjunto de dados rotulado.

### Definição e Escolha do Parâmetro K

A quantidade *K*, que define o número de vizinhos considerados no processo de decisão, é um hiperparâmetro de relevância crítica. Valores muito baixos podem levar a sobreajuste; valores excessivamente altos podem diluir a influência de observações relevantes. O notebook realiza uma varredura sobre diversos valores de *K*, observando seu impacto na acurácia do modelo.

## Etapas da Metodologia Adotada

1. Leitura e preparação do dataset original (`diabetes.csv`), com análise descritiva dos atributos.
2. Visualizações para detecção de padrões e correlações.
3. Normalização dos dados, essencial para algoritmos baseados em distância.
4. Separação entre conjuntos de treino e teste.
5. Implementação do KNN utilizando a biblioteca `scikit-learn`.
6. Avaliação do modelo com uso de métricas quantitativas.
7. Aplicação de validação cruzada para evitar avaliações enviesadas.
8. Comparação com modelos concorrentes, ressaltando vantagens e deficiências.
9. Ajuste do hiperparâmetro *K* com uso de `GridSearchCV`.

## Ferramentas e Bibliotecas Utilizadas

- Python 3.x
- `pandas`, `numpy` – manipulação e tratamento de dados;
- `matplotlib`, `seaborn` – geração de gráficos e visualizações para o EDA;
- `scikit-learn` – construção e avaliação dos modelos de aprendizado supervisionado.

## Organização do Repositório

```bash
├── data/
│   └── diabetes.csv                  # Conjunto de dados utilizado para a modelagem
├── knn-diabetes-classification.ipynb  # Notebook com todas as etapas do projeto
├── README.md                         # Documento técnico e descritivo do projeto


