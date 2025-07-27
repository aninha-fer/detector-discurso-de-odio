<h1>Projeto de Deep Learning: Detecção de Discurso de Ódio</h1>
Este projeto visa desenvolver um modelo de Deep Learning para identificar discurso de ódio em comentários de redes sociais na língua inglesa, utilizando Processamento de Linguagem Natural (NLP). O objetivo é contribuir para a moderação de conteúdo online e promover ambientes mais seguros.

<br>📊 **Dataset**
<br>O projeto utilizou o dataset twitter-hate-speech-en-240ksamples da Hugging Face, contendo cerca de 240 mil comentários do Twitter categorizados como hate speech, Neutral or Ambiguous e non-hate speech.

✨ **Pré-processamento**
<br>As etapas de pré-processamento incluíram:
<br>-Remoção de menções de usuários, links, pontuações, emojis e símbolos.
<br>-Padronização para letras minúsculas e remoção de stopwords.
<br>-Classificação binária (0 para ausência de ódio, 1 para presença).
<br>-Tokenização e padronização das sequências para 50 tokens.
<br>-Divisão dos dados em 70% treino e 30% teste.

🧠 **Modelo de Deep Learning**
<br>O modelo é uma rede neural sequencial construída com Keras, composta por:
<br>-Camada de Embedding: Transforma palavras em vetores densos (32 dimensões).
<br>-Camada GlobalAveragePooling1D: Reduz a dimensionalidade.
<br>-Camadas Densa (Dense): Introduzem não linearidade (32 e 16 neurônios com ativação ReLU).
<br>-Camadas Dropout: Para regularização e prevenção de overfitting (taxas de 0.2 e 0.1).
<br>-Camada de Saída: Um neurônio com ativação sigmoid para classificação binária.
<br>O treinamento utilizou binary_crossentropy, otimizador adam e accuracy como métrica. Foi implementado Early Stopping para evitar overfitting.

📊 **Resultados**
<br>O modelo final obteve uma acurácia geral de 0.8158 (quase 82%).
<br>Acertos (Sem ódio): 33.066.
<br>Acertos (Com ódio): 26.346.
<br>Precisão (Classe 1): 83%.
<br>Recall (Classe 1): 77%.
<br>F1-score (Classe 1): 80%.
