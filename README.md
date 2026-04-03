# Guia pandas e matplotlib para Python
Olá, nesse Notebook será abordado assuntos baseados em duas bibliotecas muito utilizadas no python para Análise, Manipulação e Visualização de Dados. Optei por esse assunto pois são duas bibliotecas que estou aprendendo na faculdade e vi uma oportunidade de poder utilizar esse NotebookLm para auxiliar e potencializar meus estudos! Meu foco com esse guia é justamente poder aprimorar meus entendimentos baseados em fontes confiáveis e seguras de informação.

**Alguns links utilizados:**

https://pandas.pydata.org/docs/user_guide/index.html#user-guide

https://pandas.pydata.org/docs/user_guide/index.html#user-guide

https://www.kufunda.net/publicdocs/Pandas%20Python%20Data%20Wrangling%20Para%20Ciencia%20De%20Dados%20(Eduardo%20Corr%C3%AAa).pdf

https://ecs.wgtn.ac.nz/foswiki/pub/Support/ManualPagesAndDocumentation/numpybook.pdf


# Documentação de Prompts e Resultados:

## *1º Prompt*
- Ensine-me NumPy e Pandas assumindo que sou iniciante.

## *1ª Resultado*
**NumPy** e **Pandas** são as duas ferramentas mais fundamentais para qualquer pessoa que deseja trabalhar com ciência de dados e análise estatística usando Python. Enquanto o NumPy foca em cálculos matemáticos pesados e processamento eficiente de grandes volumes de dados numéricos, o Pandas é construído sobre o NumPy e funciona como uma "planilha de Excel superpotente" para manipular tabelas.

Aqui está um guia inicial para você começar do zero:

### 1. Instalação e Importação
O primeiro passo é garantir que as bibliotecas estejam instaladas em seu computador. Você pode instalá-las via terminal usando o gerenciador de pacotes `pip`:
*   `pip install numpy`
*   `pip install pandas`

No seu código Python, a convenção padrão de importação é usar apelidos (aliases) para facilitar a escrita:
```python
import numpy as np
import pandas as pd
```

### 2. Aprendendo NumPy (O Coração Numérico)
A estrutura principal do NumPy é o **ndarray** (array n-dimensional). Diferente das listas padrão do Python, os arrays do NumPy processam dados de forma muito mais rápida porque são otimizados computacionalmente e exigem que todos os elementos sejam do mesmo tipo.

*   **Criando Arrays:** Você pode criar um array a partir de uma lista comum.
    ```python
    a = np.array()
    ```
*   **Dimensões:** Arrays podem ser unidimensionais (vetores), bidimensionais (matrizes) ou ter múltiplas dimensões (tensores).
*   **Operações Vetorizadas:** Uma das maiores vantagens é poder fazer cálculos em todos os elementos de uma vez. Por exemplo, `a * 2` multiplicará cada número do array por dois instantaneamente.
*   **Funções Matemáticas:** O NumPy possui ferramentas integradas para calcular a soma (`sum`), o valor máximo (`max`), o mínimo (`min`) e a média (`mean`) de um conjunto de dados.

### 3. Aprendendo Pandas (A Ferramenta de Análise)
O Pandas introduz duas estruturas de dados principais que facilitam a manipulação de dados tabulares:

1.  **Series:** É como uma única coluna de uma planilha, onde cada valor possui um rótulo (índice).
2.  **DataFrame:** É a estrutura mais importante, representando uma tabela inteira com linhas e colunas (como uma planilha Excel ou tabela SQL).

#### Operações Essenciais com Pandas:
*   **Carregar Dados:** É muito comum ler arquivos externos para um DataFrame.
    ```python
    df = pd.read_csv("seu_arquivo.csv")
    df_excel = pd.read_excel("planilha.xlsx")
    ```
*   **Visualização Rápida:** Use `df.head()` para ver as primeiras 5 linhas ou `df.info()` para ver o resumo das colunas e tipos de dados.
*   **Filtragem:** Você pode selecionar apenas os dados que atendem a uma condição.
    ```python
    # Exemplo: Pegar apenas linhas onde a idade é maior que 30
    filtro = df[df['idade'] > 30]
    ```
*   **Tratamento de Dados:** Aproximadamente 75% do trabalho com Pandas envolve a limpeza de dados. Valores vazios ou nulos são representados como `NaN` (*Not a Number*) e podem ser removidos com `dropna()` ou preenchidos com `fillna()`.
*   **Agrupamento (Group By):** Permite consolidar informações. Por exemplo, você pode agrupar uma base de vendas por "loja" e somar o "faturamento" para saber qual unidade vendeu mais.

### Resumo para o Iniciante
*   Use **NumPy** quando precisar de performance matemática e trabalhar com arrays numéricos puros.
*   Use **Pandas** para organizar, limpar, filtrar e analisar tabelas de dados provenientes de fontes como CSV ou Excel.
*   Pratique carregando um conjunto de dados pequeno e tente responder perguntas como "qual a média desta coluna?" ou "quantas vezes este item aparece?" usando as funções `mean()`, `value_counts()` e `groupby()`.


## *2º Prompt*
- Estou iniciando na faculdade de Data Science, qual roadmap você estruturaria para minha jornada de conhecimento, tomando como partida que eu estou iniciando meus estudos?

## *2ª Resultado*
Para estruturar sua jornada na faculdade de Data Science, é fundamental compreender que esta área une técnicas estatísticas e computacionais para extrair conhecimento valioso de grandes bases de dados. Como você está iniciando, o roadmap abaixo foca na progressão lógica das ferramentas e conceitos apresentados nas fontes:

### 1. Base em Python e Bibliotecas Numéricas
O ponto de partida deve ser o domínio da linguagem Python. Logo em seguida, você deve focar no **NumPy**, que é a "pedra fundamental" da computação científica em Python.
*   **Por que aprender:** O NumPy é muito superior às listas padrão do Python em termos de processamento e velocidade. Ele permite realizar **operações vetorizadas** (cálculos em massa sem precisar de laços `for`) e manipular **arrays n-dimensionais** (vetores e matrizes).
*   **Conceitos-chave:** Criação de arrays, *slicing* (fatiamento), funções matemáticas integradas (`sum`, `mean`, `sqrt`) e o conceito de *broadcasting* (operações entre arrays de formas diferentes).

### 2. Manipulação de Dados com Pandas (Data Wrangling)
A biblioteca **Pandas** é construída sobre o NumPy e é a ferramenta mais utilizada para análise de dados. Ela será essencial para o que se chama de **Data Wrangling** ou **Data Preparation**, que ocupa cerca de **80% do tempo** de um projeto de ciência de dados.
*   **Estruturas principais:** Aprenda a diferenciar as **Series** (unidimensionais) dos **DataFrames** (bidimensionais, como planilhas de Excel).
*   **Habilidades essenciais:**
    *   **Importação e Exportação:** Ler arquivos CSV, Excel e JSON.
    *   **Limpeza de Dados:** Tratar valores nulos (**NaN**), remover duplicatas e corrigir tipos de dados.
    *   **Transformação:** Criar novas colunas (*feature engineering*), filtrar linhas e agrupar dados com o método **groupby**.

### 3. Estatística Descritiva e Análise Exploratória (EDA)
Antes de criar modelos, você deve "ouvir" o que os dados dizem.
*   **Medidas de Tendência Central:** Entender o uso de média, mediana e moda para diferentes tipos de atributos.
*   **Medidas de Variabilidade:** Aprender amplitude, variância e desvio padrão para entender o quão espalhados os dados estão.
*   **Tipos de Atributos:** Identificar se seus dados são numéricos (contínuos/discretos) ou categóricos (nominais/ordinais).

### 4. Visualização de Dados
A visualização transforma números em imagens compreensíveis. Use o Pandas para visualizações rápidas, mas especialize-se no **Matplotlib** para gráficos profissionais.
*   **Gráficos fundamentais:** Gráficos de linha (tendências), barras (comparações), histogramas (distribuição) e **boxplots** (excelentes para detectar **outliers** e visualizar quartis).
*   **Habilidades técnicas:** Customizar eixos, legendas, títulos e utilizar **subplots** para colocar vários gráficos em uma mesma figura.

### 5. Fundamentos de Machine Learning
Com os dados limpos e explorados, você entra na etapa de criação de modelos.
*   **Introdução à Classificação:** Treinar o computador para atribuir classes a objetos (ex: classificar um e-mail como spam ou normal).
*   **Algoritmos e Ferramentas:** Comece com algoritmos intuitivos como o **k-NN (k-Nearest Neighbors)** utilizando a biblioteca **Scikit-learn**.
*   **Avaliação do Modelo:** Entender métricas como **Acurácia** e ferramentas como a **Matriz de Confusão** para verificar se o seu modelo é realmente eficaz.

**Dica Prática:** A Ciência de Dados é um processo **cíclico**. Muitas vezes, ao interpretar os resultados finais, você precisará voltar para a etapa de limpeza ou seleção de dados para aprimorar seu modelo.

