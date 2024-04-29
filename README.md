Nesta parte do projeto foi preciso atendermos outros requisitos que seriam a medição de temperatura e umidade do ambiente, para isso seria preciso utilizar um sensor integrado DHT11. As informações precisam aparecer no display para que seja possível a melhor visualização, além disso continuamos com o sinal de alerta e os LED'S que indicam a luminosidade do ambiente.

Explicação do código passo a passo: 

1- Inclusão de Bibliotecas: 

   - As bibliotecas `LiquidCrystal.h` e `DHT.h` são incluídas para utilizar as funções relacionadas ao LCD e ao sensor DHT22, respectivamente. 

  

2- Definição de Constantes e Pinagem: 

   - São definidos os pinos para os LEDs, o buzzer, o sensor DHT22, o LDR (fotocélula), e os pinos do LCD. 

   - São definidas constantes para os limites de luminosidade, temperatura e umidade. 

  

3- Inicialização: 

   - O método `setup()` é chamado uma vez, onde são configurados os pinos como entrada ou saída, inicia-se a comunicação serial, o sensor DHT22, e o LCD. Também são criados os caracteres personalizados para o LCD. 

  

4- Loop Principal: 

   - O método `loop()` é executado continuamente. 

   - A cada 5 segundos (definido por `millis() - lastUpdateTime >= 5000`), as leituras do sensor DHT22 e do LDR são atualizadas e os LEDs são controlados com base nesses valores. 

   - Se a leitura do sensor DHT22 falhar, uma mensagem de erro é impressa e o loop continua. 

  

5- Funções Auxiliares: 

   - `desligarLEDs()`: Desliga todos os LEDs. 

   - `atualizarStatus()`: Atualiza o status dos LEDs com base nos valores lidos do sensor DHT22 e do LDR. Também chama `atualizarLCD()` para atualizar as informações no LCD. 

   - `atualizarLCD()`: Atualiza as informações no LCD com base nos valores lidos do sensor DHT22 e do LDR. 

  

6- Exibição no LCD: 

   - No LCD, são exibidos ícones para temperatura, umidade e luminosidade, juntamente com os respectivos valores. 

   - Além disso, são exibidas mensagens relacionadas às condições de temperatura, umidade e luminosidade, com possíveis avisos sonoros. 

  

7- Controle dos LEDs: 

   - Os LEDs são controlados de acordo com as condições de luminosidade, temperatura e umidade, sendo verde para condições ideais, amarelo para condições intermediárias e vermelho para condições críticas. 

  

Esse código tem como intuito monitorar o ambiente (luminosidade, temperatura e umidade) e fornece feedback visual e sonoro sobre as condições encontradas, além de exibir as informações em um LCD. 




Materiais Utilizados: 

1 Arduino UNO 

1 Placa de ensaio 

5 Resistores 

1 LED verde 

1 LED vermelho 

1 LED amarelo 

1 DHT22 

1 BUZZER 

1 LCD com 2 linhas e 16 caracteres por linha 

29 fios  

1 LDR 

