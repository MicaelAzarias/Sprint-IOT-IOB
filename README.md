🧠 Classificação de Gênero e Faixa Etária com Visão Computacional
🎯 Objetivo

Este projeto tem como objetivo reconhecer o gênero (Homem ou Mulher) e estimar a faixa etária de uma pessoa em tempo real usando a webcam do computador.
A aplicação combina técnicas de Visão Computacional e Deep Learning para detectar rostos, extrair a região facial e realizar previsões utilizando modelos de redes neurais previamente treinados.

⚙️ Tecnologias e Dependências
🧩 Bibliotecas Principais

Python 3.10+

OpenCV → captura e processamento de vídeo

MediaPipe → detecção de rostos

TensorFlow / Keras → carregamento dos modelos .h5

NumPy → manipulação de matrizes

cvzone → exibição de textos e caixas na tela

📦 Instalação das dependências

No terminal, execute:

pip install numpy opencv-python tensorflow keras mediapipe cvzone

🚀 Execução do Projeto

Clone o repositório

git clone https://github.com/seu-usuario/classificacao-genero-idade.git
cd classificacao-genero-idade


Garanta que os modelos estão no diretório principal:

├── model_gender.h5
├── model_age.h5
├── testModel.py
└── redim.py


Execute o script principal

python testModel.py


O sistema abrirá uma janela da webcam exibindo:

Um retângulo verde ao redor do rosto detectado.

O gênero previsto e a faixa etária estimada.

A confiança (%) do modelo para cada predição.

Para encerrar o programa, pressione a tecla q.

🧾 Parâmetros e Funcionamento

A imagem capturada é redimensionada para 224x224 pixels.

Os valores de pixel são normalizados entre [-1, 1].

Dois modelos são usados:

model_gender.h5 → classifica Homem ou Mulher.

model_age.h5 → classifica em uma das faixas:

6–20 anos

25–30 anos

42–48 anos

60–98 anos

🧩 Organização do Código
📁 gender_and_age_classification-main
│
├── model_age.h5              # Modelo de faixa etária pré-treinado
├── model_gender.h5           # Modelo de gênero pré-treinado
├── testModel.py              # Script principal (execução com webcam)
├── redim.py                  # Script auxiliar para redimensionar imagens
└── README.md                 # Documentação do projeto

⚖️ Nota Ética sobre o Uso de Dados Faciais

O reconhecimento facial é uma tecnologia poderosa, mas requer uso ético e responsável.
Este projeto é estritamente educacional, desenvolvido para fins de estudo de técnicas de Visão Computacional e Machine Learning.

Nenhuma imagem ou dado facial de usuários é armazenado ou compartilhado.
Em aplicações reais, o uso de reconhecimento facial deve seguir:

Leis de proteção de dados (como a LGPD no Brasil e o GDPR na Europa);

Consentimento explícito dos usuários;

Evitar vieses discriminatórios nos modelos treinados.

🔮 Próximos Passos

Treinar modelos próprios com datasets diversificados.

Aprimorar a acurácia em diferentes condições de iluminação.

Adicionar detecção de emoções ou expressões faciais.

Portar a aplicação para dispositivos móveis.
