## Classificação de Estilo de Jogo de Jogadores de Futebol
Este projeto utiliza aprendizado de máquina para classificar jogadores de futebol com base em suas estatísticas de desempenho. O algoritmo K-Nearest Neighbors (KNN) é treinado para prever o estilo de jogo de um jogador (Ataque ou Defesa) com base em dados como gols, assistências, dribles completos, interceptações, passes e distância percorrida.

## Descrição do Código
O código realiza as seguintes etapas:

- Criação e Expansão de Dados:

    O código começa com um conjunto de dados inicial com informações sobre seis jogadores de futebol e suas estatísticas de desempenho.
    Esses dados são expandidos para simular 30 dias de treinamento para cada jogador, variando as estatísticas de forma aleatória. Isso cria uma base de dados mais robusta para treinar o modelo.
  
- Pré-processamento dos Dados:

    O DataFrame expandido é separado em variáveis independentes (X) e rótulos (y).
    As variáveis independentes representam as estatísticas dos jogadores, enquanto os rótulos são o estilo de jogo (Ataque ou Defesa).
    Os dados são normalizados usando a técnica de StandardScaler para garantir que todos os recursos tenham a mesma escala, o que é importante para o algoritmo KNN.

- Divisão dos Dados:

    O conjunto de dados é dividido em dois grupos: treino e teste. Aproximadamente 33% dos dados são usados para testar a precisão do modelo, enquanto o restante é utilizado para treinar o modelo.
  
- Treinamento do Modelo KNN:

    O algoritmo KNN é treinado com os dados de treino, utilizando 3 vizinhos mais próximos (n_neighbors=3).
    O modelo é avaliado utilizando os dados de teste, e as previsões são comparadas com os rótulos reais.
  
- Geração de Relatório de Classificação:

    O código gera um relatório de classificação que avalia a performance do modelo, apresentando métricas como:
    Precisão (Precision): Proporção de previsões corretas positivas entre todas as previsões positivas feitas.
    Revocação (Recall): Proporção de verdadeiros positivos entre todas as instâncias positivas.
    F1-Score: Média harmônica entre a precisão e a revocação.
  
## Dependências
Este projeto requer as seguintes bibliotecas Python:

- pandas: Para manipulação e análise de dados.
- numpy: Para cálculos e operações matemáticas.
- scikit-learn: Para as ferramentas de aprendizado de máquina, como o KNN e a normalização dos dados.
