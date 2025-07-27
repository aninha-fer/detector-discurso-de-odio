Projeto de Deep Learning: Detecção de Discurso de Ódio
Este projeto visa desenvolver um modelo de Deep Learning para identificar discurso de ódio em comentários de redes sociais na língua inglesa, utilizando Processamento de Linguagem Natural (NLP). O objetivo é contribuir para a moderação de conteúdo online e promover ambientes mais seguros.

📊 Dataset
O projeto utilizou o dataset twitter-hate-speech-en-240ksamples da Hugging Face, contendo cerca de 240 mil comentários do Twitter categorizados como hate speech, Neutral or Ambiguous e non-hate speech.

✨ Pré-processamento
As etapas de pré-processamento incluíram:
-Remoção de menções de usuários, links, pontuações, emojis e símbolos.
-Padronização para letras minúsculas e remoção de stopwords.
-Classificação binária (0 para ausência de ódio, 1 para presença).
-Tokenização e padronização das sequências para 50 tokens.
-Divisão dos dados em 70% treino e 30% teste.

🧠 Modelo de Deep Learning
O modelo é uma rede neural sequencial construída com Keras, composta por:
-Camada de Embedding: Transforma palavras em vetores densos (32 dimensões).
-Camada GlobalAveragePooling1D: Reduz a dimensionalidade.
-Camadas Densa (Dense): Introduzem não linearidade (32 e 16 neurônios com ativação ReLU).
-Camadas Dropout: Para regularização e prevenção de overfitting (taxas de 0.2 e 0.1).
-Camada de Saída: Um neurônio com ativação sigmoid para classificação binária.
O treinamento utilizou binary_crossentropy, otimizador adam e accuracy como métrica. Foi implementado Early Stopping para evitar overfitting.

📊 Resultados
O modelo final obteve uma acurácia geral de 0.8158 (quase 82%).
Acertos (Sem ódio): 33.066.
Acertos (Com ódio): 26.346.
Precisão (Classe 1): 83%.
Recall (Classe 1): 77%.
F1-score (Classe 1): 80%.
