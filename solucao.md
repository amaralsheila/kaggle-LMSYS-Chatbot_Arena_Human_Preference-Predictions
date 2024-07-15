```mermaid
graph TD
    A[Importação das bibliotecas]
    B[Carregamento dos dados]
    C[Preparação dos Dados] 
    D[Limpeza de textos]   
    E[Feature Engineering]
    E1a[Contagem de palavras]
    E2a[Contagem de caracteres]
    E3a[Diversidade lexical]
    E4a[Contagem de sílabas]
    E5a[Contagem de frases]
    E6a[Índice de facilidade de leitura Flesch]
    E7a[Análise de sentimento]
    E1b[Tokenização]
    E2b[Embedings]
    E3b[Similaridade entre textos]
    
    F[Separação de dados de treino e validação]
    G[Modelagem]
    H[Criação de modelos]
    H1[Random Forest]
    H3[Support Vector Machine]
    H4[Gradient Boosting]
    H5[Neural Network]
    H5a[Camada de entrada]
    H5b[Dense: 128, ReLU]
    H5c[Dropout: 0.2]
    H5d[Dense: 64, ReLU]
    H5e[Dense: 3, Softmax]
    H5f[Compilação do modelo: Adam, sparse_categorical_crossentropy, accuracy]
    I[Treinamento dos modelos]
    J[Avaliação com validação cruzada]
    K[Seleção do melhor modelo]

    L[Predição e Submissão]
    L1[Preparação dos dados de teste]
    L2[Predição nos dados de teste]
    L3[Criação do arquivo de submissão]

    A --> B
    B --> C
    C --> D
    D --> E

    E --> E1a --> F
    E --> E2a --> F
    E --> E3a --> F
    E --> E4a --> F
    E --> E5a --> F
    E --> E6a --> F
    E --> E7a --> F

    E --> E1b --> F
    E --> E2b --> F
    E --> E3b --> F

    F --> G --> I
    G --> H --> I
    H --> H1 --> I
    H --> H3 --> I
    H --> H4 --> I
    H --> H5 --> I
    H5 --> H5a --> H5f
    H5 --> H5b --> H5f
    H5 --> H5c --> H5f
    H5 --> H5d --> H5f
    H5 --> H5e --> H5f
    H5f --> I
    I --> J
    J --> K
    K --> L
    L --> L1
    L1 --> L2
    L2 --> L3
