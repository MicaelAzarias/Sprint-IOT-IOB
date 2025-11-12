🧠 Classificação de Gênero e Faixa Etária com Visão Computacional

Projeto desenvolvido em Python para identificar o gênero e a faixa etária de uma pessoa em tempo real usando a webcam.
Utiliza técnicas de Visão Computacional e Deep Learning com modelos .h5 pré-treinados.

🎯 Objetivo

O sistema detecta rostos capturados pela webcam, processa a imagem e realiza duas previsões:

👨‍🦱 Gênero: Homem ou Mulher

🎂 Faixa etária: 6–20, 25–30, 42–48 ou 60–98 anos

Tudo acontece em tempo real, mostrando o resultado diretamente sobre o rosto detectado.

⚙️ Tecnologias Utilizadas
Tecnologia	Função
🐍 Python 3.10+	Linguagem principal
🎥 OpenCV	Captura e processamento de vídeo
👁️ MediaPipe	Detecção facial
🧠 TensorFlow / Keras	Carregamento e execução dos modelos de IA
🧩 NumPy	Manipulação de arrays e normalização
💬 cvzone	Exibição de textos e caixas na tela
🧩 Instalação e Execução
1️⃣ Instale as dependências
pip install numpy opencv-python tensorflow keras mediapipe cvzone

2️⃣ Estrutura do projeto
📁 gender_and_age_classification-main
│
├── model_gender.h5          # Modelo de gênero
├── model_age.h5             # Modelo de idade
├── testModel.py             # Script principal
├── redim.py                 # Script auxiliar
└── README.md

3️⃣ Execute o programa
python testModel.py

4️⃣ Resultado

A janela da webcam será aberta mostrando:

🟩 Um retângulo verde em volta do rosto

🧍 O gênero previsto

⏳ A faixa etária estimada

📊 A confiança (%) da previsão

➡️ Pressione q para encerrar o programa.

🔬 Como Funciona

O vídeo é capturado em tempo real pela webcam.

O MediaPipe detecta o rosto e extrai a região facial.

A imagem é redimensionada para 224x224 pixels e normalizada entre [-1, 1].

Os dois modelos (gender e age) processam a imagem.

O resultado é exibido visualmente com as previsões e confianças.

📊 Parâmetros dos Modelos
Modelo	Tipo	Saídas	Precisão mínima exibida
model_gender.h5	Classificação binária	Homem / Mulher	30%
model_age.h5	Classificação por faixa	6–20, 25–30, 42–48, 60–98	40%


⚖️ Nota Ética sobre o Uso de Dados Faciais

⚠️ Este projeto é educacional e não deve ser usado para fins comerciais sem consentimento dos usuários.

Nenhum dado facial é salvo ou transmitido.

O reconhecimento facial deve respeitar:

A LGPD (Lei Geral de Proteção de Dados) no Brasil

O GDPR na Europa

Em aplicações reais, é fundamental obter consentimento informado e reduzir vieses de gênero, idade ou etnia.

🚧 Limitações

Pode falhar com pouca iluminação ou ângulos extremos.

As faixas etárias são amplas e podem gerar confusão.

O modelo foi treinado em um dataset genérico, podendo apresentar viés em rostos de diferentes origens.

🔮 Próximos Passos

🧠 Treinar modelos personalizados e mais precisos

📱 Adaptar o sistema para rodar em dispositivos móveis

😊 Adicionar reconhecimento de emoções e expressões faciais

⚡ Melhorar desempenho em tempo real
