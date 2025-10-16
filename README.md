# Módulo 30 - K-Means: Segmentação de Espécies de Pinguins

## 📖 Descrição do Projeto

Este projeto consiste na aplicação do algoritmo de *clustering* **K-Means** para segmentar diferentes espécies de pinguins com base em suas características físicas. Diferentemente de aplicações usuais em marketing ou finanças, este estudo foca em dados biológicos, demonstrando a versatilidade de K-Means para agrupar indivíduos em um contexto científico.

O objetivo principal é identificar agrupamentos naturais nos dados e compará-los com as espécies reais, validando a eficácia do K-Means na diferenciação das espécies.

---

## 💾 Dados

O projeto utiliza o famoso conjunto de dados **`penguins`**, disponível no pacote `seaborn`, que contém informações de pinguins coletadas na Antártica.

### Variáveis Utilizadas no Clustering

As variáveis quantitativas (numéricas) foram as selecionadas como *features* para o modelo K-Means:

| Variável | Descrição | Unidade |
| :--- | :--- | :--- |
| `bill_length_mm` | Comprimento do bico | Milímetros (mm) |
| `bill_depth_mm` | Profundidade do bico | Milímetros (mm) |
| `flipper_length_mm` | Comprimento da barbatana | Milímetros (mm) |
| `body_mass_g` | Massa corporal | Gramas (g) |

### Espécies Presentes

O conjunto de dados original inclui três espécies de pinguins:
* Adelie
* Chinstrap
* Gentoo

---

## 🛠️ Tecnologias e Bibliotecas

O projeto foi desenvolvido em Python, utilizando as seguintes bibliotecas:

* **`pandas`**: Manipulação e análise de dados.
* **`seaborn`**: Carregamento do dataset `penguins` e visualizações.
* **`plotly.express` / `plotly.graph_objects`**: Visualizações interativas (como gráficos de dispersão 3D).
* **`sklearn.cluster.KMeans`**: Implementação do algoritmo K-Means.
* **`sklearn.preprocessing.StandardScaler`**: Padronização dos dados.

---

## 🚀 Etapas da Análise

O processo de clustering seguiu as seguintes etapas:

1.  **Limpeza e Pré-processamento de Dados:**
    * Remoção de colunas categóricas que não seriam utilizadas no K-Means (`island` e `sex`).
    * Exclusão de linhas com valores nulos, devido à baixa representatividade de dados faltantes (menos de 4% em todas as colunas impactadas).
2.  **Análise Descritiva e Exploração (EDA):**
    * Utilização do `pairplot` para visualizar a distribuição e a relação entre as variáveis, buscando identificar visualmente a formação de possíveis agrupamentos.
3.  **Padronização dos Dados:**
    * As variáveis numéricas foram padronizadas utilizando `StandardScaler` para garantir que todas tivessem a mesma importância na criação dos clusters.
4.  **Definição do Número de Clusters (k):**
    * Aplicação do **Método do Cotovelo (Elbow Method)** para determinar o número ideal de clusters (`k`) para o modelo.
5.  **Modelagem K-Means:**
    * O algoritmo K-Means foi ajustado aos dados, e os rótulos de cluster foram adicionados ao DataFrame original.
6.  **Visualização dos Resultados:**
    * Gráficos de dispersão 3D e novos `pairplots` foram gerados, coloridos pelos rótulos de cluster, para visualizar a segmentação obtida pelo modelo.
7.  **Conclusão:**
    * Comparação dos clusters gerados com os rótulos de espécies originais para avaliar a performance do modelo em identificar as espécies existentes.

---
