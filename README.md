Detecção de Pneumonia em Raios-X

Este é um repositório que contém código para detecção de pneumonia em imagens de raios-X do tórax usando Deep Learning com TensorFlow e Keras.

Descrição do Projeto

O objetivo deste projeto é criar um modelo de Deep Learning que possa identificar se uma imagem de raios-X do tórax pertence a um paciente com pneumonia ou não. Para isso, utilizamos uma arquitetura de rede neural convolucional (CNN) para aprender padrões discriminativos diretamente das imagens.

Conjunto de Dados

O conjunto de dados usado neste projeto é o Chest X-Ray Images (Pneumonia) disponível no Kaggle. Ele contém imagens de raio-X do tórax de pacientes divididas em conjuntos de treinamento, teste e produção.

Pré-processamento e Augmentação de Dados

As imagens foram pré-processadas redimensionando-as para o tamanho de entrada da rede (224x224) e normalizando os valores dos pixels para o intervalo [0, 1]. Além disso, foi aplicada uma técnica de aumento de dados durante o treinamento, incluindo cisalhamento, zoom aleatório e inversão horizontal, para melhorar a generalização do modelo.

Arquitetura do Modelo

A arquitetura da rede neural utilizada consiste em várias camadas convolucionais e de pooling, seguidas por camadas totalmente conectadas. Aqui está um resumo da arquitetura do modelo:

Camadas convolucionais com ativação ReLU e normalização em lote.
Camadas de pooling para redução da dimensionalidade.
Camadas totalmente conectadas com ativação ReLU e regularização L2.
Camada de saída com ativação sigmoid para previsão binária.
Treinamento e Avaliação
O modelo foi compilado com o otimizador RMSprop e a função de perda de entropia cruzada binária. Durante o treinamento, usamos callbacks para redução da taxa de aprendizado e parada antecipada para evitar overfitting.

Após o treinamento, o modelo foi avaliado no conjunto de teste, alcançando uma precisão de 93.75%.

Exemplo de Uso


Você pode usar o modelo treinado para fazer previsões em novas imagens de raios-X do tórax. Um exemplo de como fazer isso é fornecido no código, onde uma imagem de exemplo é carregada e passada pelo modelo para determinar se o paciente está com pneumonia ou não.

Requisitos de Instalação


Certifique-se de ter instalado o TensorFlow e as bibliotecas relacionadas. Você pode instalar essas dependências executando:
pip install tensorflow matplotlib pandas

Como Usar

Clone este repositório:
git clone (https://github.com/Mateusaraujo8/Projeto-Raiox)
Execute o script Python detecao_pneumonia.py para treinar o modelo e fazer previsões.


Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir um problema ou enviar uma solicitação de pull.
