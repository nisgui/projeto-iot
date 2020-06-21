# Objetos Inteligentes Conectados 2 sem. 2020
# Turma 5H11
# Projeto: Arduino com sensor de temperatura e ativação automática de ventilação
## Integrantes do grupo:
### - Nicole Francani Godinho
### - Augusto Vasques Vasconcelos

**Descrição do hardware utilizado:**

Lista de Peças
* 01 - Arduino Uno R3 com Cabo USB;
* 01 - Protoboard 400 Pontos;
* 07 - Jumpers Fêmea / Fêmea
* 01 - Resistor de 10KΩ
* 01 - Sensor de Temperatura LM35
* 01 - Micro Cooler 5V

**Descrição do funcionamento e uso para quem quiser reproduzir:**

Primeiro de tudo, é preciso realizar a conexão de todos componentes na protoboard, sendo estes componentes: fios, resistores, jumpers, sensor de temperatura e o cooler (sendo representado como um motor no tinkercad). Conforme ilustrado na figura abaixo:
![GitHub Logo](/tinkercad.png)

Depois disso, para este projeto utilizamos o protocolo firmata, que é um protocolo para comunicação com microcontroladores a partir de software em um computador. Para utiliza-lo, na IDE do Arduino temos na barra de exemplos o sketch ja pronto, chamado StandardFirmata. A partir disso, apenas colocar para rodar o código.

 Após isso iniciamos a aplicação no Node Red que vai trabalhar como servidor, na figura a seguir temos a montagem dos nodes da aplicação começando pelo LM35 e terminando com o acionamento do cooler: 

![GitHub Logo](/nodered.png)

Para este projeto utilizamos a comunicação via MQTT utilizando um broker (Mosquitto), no qual possibilitou o envio e recebimento de mensagens referentes aos resultados obtidos ao simplesmente acessar o IP onde se encontra o dashboard de monitoramento.

Após isso, colocando o DEPLOY e indo na Dashboard do Node-red, podemos ver o funcionamento do projeto conforme a temperatura atinge 22 graus, é ativado o micro cooler.


