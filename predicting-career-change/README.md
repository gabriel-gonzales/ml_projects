# Predicting Career Change

Este notebook utiliza Python para analisar e prever mudanças de carreira, aplicando técnicas de análise de dados, preparação e modelagem. Ele emprega um classificador baseado em Random Forest para prever se um indivíduo está propenso a mudar de carreira com base em atributos fornecidos.

## Descrição

O notebook aborda um problema de classificação com o objetivo de prever a probabilidade de uma mudança de carreira. Ele utiliza dados do dataset `career_change_prediction_dataset.csv`, que contém informações sobre campos de estudo e ocupações.

## Estrutura do Notebook

### 1. **Exploração de Dados**
O dataset foi carregado e inspecionado para entender sua estrutura e características principais:
- **Carregamento e inspeção:** Foi utilizado `pd.read_csv` para carregar os dados, seguido de `info()` e `describe()` para explorar suas dimensões, tipos de dados e valores estatísticos.
- **Insights iniciais:** Identificação de colunas com dados ausentes e análise preliminar das distribuições dos atributos.

### 2. **Preparação de Dados**
As etapas de preparação incluem:
- **Preenchimento de valores ausentes:** Uso do `SimpleImputer` para lidar com valores faltantes.
- **Codificação de variáveis categóricas:** Aplicação do `LabelEncoder` para transformar categorias em valores numéricos.
- **Divisão dos dados:** Separação em conjuntos de treinamento (80%) e teste (20%) com `train_test_split`.

### 3. **Modelagem**
Um modelo de Random Forest foi treinado e avaliado:
- **Treinamento do modelo:** A classe `RandomForestClassifier` foi usada para treinar o modelo com 100 árvores e uma semente aleatória de 42 para consistência.
- **Predição:** O modelo gerou previsões para os dados de teste.
- **Avaliação:** Foram gerados relatórios de classificação e matrizes de confusão para medir o desempenho.

### 4. **Resultados**
Os resultados indicam:
- **Acurácia do modelo:** Foi alcançada uma acurácia geral elevada, com valores reportados pelo `classification_report`.
- **Validação cruzada:** O modelo passou por validação cruzada (`cross_val_score`), obtendo uma média de performance estável.
- **Visualizações:** A matriz de confusão foi plotada para ilustrar o desempenho do modelo, destacando os acertos e erros nas previsões.


## Insights Principais

1. O modelo é robusto em prever mudanças de carreira com base nos atributos fornecidos.
2. A validação cruzada revelou uma boa consistência entre os conjuntos de dados.
3. A matriz de confusão destacou áreas de melhoria, especialmente na redução de falsos positivos.
