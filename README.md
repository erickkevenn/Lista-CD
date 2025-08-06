# Análise de Dados de Vendas - Lista 1 (Ciência de Dados)

Este repositório contém a resolução da **Lista 1** da disciplina de Ciência de Dados da Universidade Federal de Alagoas (UFAL). O projeto abrange etapas do ciclo de vida da ciência de dados, desde a aquisição e pré-processamento até a modelagem e análise estatística.

---

**Aluno:** Erick Keven da Silva Alves  
**Curso:** Ciência de Dados

## Estrutura do Projeto

O projeto está organizado em um único notebook Jupyter (`lista.ipynb`), que executa as seguintes tarefas:

1. **Aquisição de Dados e Leitura:** Leitura de um arquivo CSV de dados de vendas.
2. **Pré-processamento de Dados:** Limpeza e normalização dos dados.
3. **Análise Estatística:** Cálculo de métricas descritivas.
4. **Visualização de Dados:** Geração de gráfico de barras.
5. **K-Vizinhos Mais Próximos (KNN):** Classificação de vendas e avaliação do modelo.
6. **Agrupamento K-means:** Clusterização de produtos.
7. **Análise de Clusters:** Descrição das características dos clusters.
8. **Visualização de Clusters:** Gráfico de dispersão dos clusters.
9. **Validação Cruzada:** Avaliação da estabilidade do modelo KNN.
10. **Tomada de Decisão:** Estratégias de marketing baseadas nos clusters e análise de impacto.

---

## Como Executar

1. **Clone este repositório:**
    ```bash
    git clone https://github.com/erickkevenn/Lista-CD.git
    cd Lista-CD
    ```

2. **Instale as dependências:**
    ```bash
    pip install pandas matplotlib seaborn scikit-learn numpy scipy
    ```

3. **Abra o notebook** `lista.ipynb` com Jupyter Notebook ou JupyterLab.

4. **Execute as células** em ordem. Certifique-se de ter o arquivo `dados.csv` na mesma pasta do notebook.

---

## Análise e Resultados

### 1. Aquisição de Dados e Leitura
- Leitura do arquivo `dados.csv`.
- Exibição das primeiras 5 linhas: colunas **Data**, **Produto**, **Quantidade** e **Preço**.

### 2. Pré-processamento de Dados
- Remoção de linhas com valores nulos.
- Conversão da coluna **Data** para o tipo `datetime`.
- Normalização da coluna **Quantidade** (valores entre 0 e 1).

### 3. Análise Estatística
- **Média:** 2.676
- **Mediana:** 2.5
- **Desvio Padrão:** 1.6269
- **Moda:** [1.2]

### 4. Visualização de Dados
- Gráfico de barras mostrando a quantidade total (normalizada) de cada produto vendido.

### 5. K-Vizinhos Mais Próximos (KNN)
- Criação da coluna binária **Alta_Venda** (1 se quantidade > média, 0 caso contrário).
- Treinamento do modelo KNN para prever **Alta_Venda**.
- **Resultados:** Matriz de confusão e relatório de classificação com 100% de precisão, recall e f1-score.

### 6. Agrupamento K-means
- Aplicação do método do cotovelo para determinar o número ideal de clusters.
- **Número ideal de clusters:** 3

### 7. Análise de Clusters
- Médias de **Quantidade** e **Preço** para cada cluster:
  - **Cluster 0:** Quantidade = 0.6623, Preço = 4.346
  - **Cluster 1:** Quantidade = 0.6961, Preço = 1.3625
  - **Cluster 2:** Quantidade = 0.1831, Preço = 2.4539

### 8. Visualização de Clusters
- Gráfico de dispersão dos produtos por quantidade e preço, coloridos por cluster.

### 9. Validação Cruzada
- Validação cruzada (5-fold) do modelo KNN.
- **Média dos scores:** 1.0 (modelo extremamente estável).

### 10. Tomada de Decisão com Base em Clustering
- **Cluster 0 (Alta Quantidade, Alto Preço):** Aumentar o preço e lançar promoções.
- **Cluster 1 (Alta Quantidade, Baixo Preço):** Manter o preço e focar em marketing direcionado.
- **Cluster 2 (Baixa Quantidade, Preço Médio):** Diminuir o preço e lançar promoções.

- **Teste t:** Comparação dos preços antes e depois das estratégias sugeridas.
  - **p-valor:** 0.240 (maior que 0.05) → Mudanças de preço **não tiveram impacto estatisticamente significativo** nas vendas.

---

## Referências

- [Documentação do Pandas](https://pandas.pydata.org/)
- [Documentação do Scikit-learn](https://scikit-learn.org/)
- [Documentação do Matplotlib](https://matplotlib.org/)
- [Documentação do Seaborn](https://seaborn.pydata.org/)

---
