# MobileNetV2-BiLSTM-para-analises-de-videos-de-violencia
Projeto que combina uma CNN **MobileNetV2** para extração de features espaciais com uma RNN **Bi-LSTM** para modelar dependências temporais em vídeos de vigilância, com o objetivo de detectar cenas com possível violência. O foco é em eficiência (rodar em edge/ambientes com GPU limitada) e em obter um pipeline pronto para treinar, avaliar e fazer inferência em arquivos de vídeo.

## Motivação:
Com o aumento do número de câmeras de vigilância em ambientes públicos e privados, torna-se inviável monitorar manualmente todos os vídeos em tempo real. Situações de violência podem passar despercebidas, atrasando a resposta de equipes de segurança e reduzindo a eficácia da prevenção.</br>

Este projeto busca enfrentar esse desafio utilizando inteligência artificial para análise automática de vídeos, com o objetivo de detectar comportamentos violentos de forma rápida e eficiente. A combinação entre MobileNetV2, responsável por extrair padrões visuais espaciais (como movimentos, posturas e interações), e uma Bi-LSTM, que modela a evolução temporal dessas ações, permite identificar sequências de violência com maior precisão e baixo custo computacional.</br>

A proposta é oferecer uma solução leve, escalável e aplicável em tempo real, adequada tanto para sistemas embarcados (edge devices) quanto para servidores de vigilância inteligentes. Dessa forma, o modelo pode atuar como um sistema de apoio à decisão, auxiliando equipes humanas a detectar incidentes precocemente e agir de maneira mais rápida e eficaz.</br>
## Tecnologias Utilizadas:

- python 3.11
- Numpy
- Tensorflow/Keras
- matplotlib
- sklearn

## Estrutura do Projeto:

o código foi desenvolvido com Jupiter, o dataset de treino esta disponivel no kaggle, apartir do link abaixo:</br>
https://www.kaggle.com/datasets/mohamedmustafa/real-life-violence-situations-dataset</br>
o dataset apresenta duas classes, violencia e sem violencia, cada classe apresenta 1000 videos de 5 segundos. para realizar o treinamento, cada classe utilizará 90% do dataset em treinamento e 10% em validação.</br>
o treinamento utilizou 50 epocas e para verificação do treino, utilizo 3 metricas, a matriz de confusão e a acuracia.

## Resultados:

o treinamento foi bem sastifatorio, talvez algumas mudanças em alguns paramentos e o aumento de epocas podem melhorar ainda mais os resultados. o treinamento obteve 82% de acuracia e o grafico abaixo demonstra a classificação de cada classe:
![modelo 1](matriz_MobileNetV2.png)

### futuramente colocarei as imagens dos resultado final do treinamento


## Como Executar o Projeto:

```bash
# 1️⃣ Clonar o repositório
git clone https://github.com/CiroKyushima/MobileNetV2-BiLSTM-para-analises-de-videos-de-violencia.git

# 2️⃣ Instalar as dependências
pip install -r requirements.txt

# 3️⃣ Abrir o Jupyter Notebook
jupyter notebook main.ipynb
