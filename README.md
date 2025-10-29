# Arduino-Controle-de-Luz-com-Potenciômetro
Processo de montagem do circuito e simulação, tem-se o projeto envolvendo o controle de luz (led) por meio de um potenciômetro.

Dando início ao processo de montagem do circuito e simulação: Controle de Luz com Potenciômetro (Componente eletrônico que possui resistência elétrica ajustavél por meio de
um botão do tipo sintonizador).

Vamos precisar ter acesso ao TINKERCAD, acesse: 

https://www.tinkercad.com/


Antes de descrever o circuito, neste projeto é fundamental apontar as regiões e plataformas responsáveis por algumas funcionalidades:

# Circuit View ( Vizualização do Circuito) 
Região demarcada com a cor vermelha, esta funcionalidade retornar para o visual do circuito. 


# Components List ( Lista de Componentes) 
Região demarcada com a cor verde,quando acionada mostra a lista dos componentes utilizados no projeto, algo bem útile que orienta a compra dos elementos para um projeto
no mundo real. 


# CODE (Código)
Esta região, demarcada com a cor marrom, é fundamental para a interface entre o Arduino e os sensores e atuadores, e nela será inserido o código desenvolvido usando um conjunto
de funções C/ C ++ que podem ser utilizadas. 


# Start Simulation ( Iniciar a Simulação) 
Região demarcada com a cor amarela, é responsável pela simulação em tempo real do projeto, e quando acionada, apresenta dinamicamente os estados dos sensores e atuadoresm além de 
seus efeitos visuais. 


![Projeto Circuito com Poliômetro C](https://github.com/user-attachments/assets/1d752691-7fd6-4744-b6fd-c8d1fedef842)



Ainda, usando nossa figura acima é importante destacar:

- Cabo de Cor Preta = Representa o "terra" (gnd)
- Cabo de Cor Vermelha = Representa o VCC (5V)
- Cabo de Cor Verde = Representa o valor analógico de 0 a 1023 que é enviado para o Arduino ( A0)


O Resistor em led servirá para que eviatar sua sobreceraga, evitando que ele queime, e o led, por sua vez, está conectado na porta digital ~D10.
E o fato de ligar em uma porta digital com o símbolo ~acontece devido as portas digitais (GPI0) marcadas com um ~(til) possuírem a capacidade de servirem saída do tipo PWM.
Uma saída do tipo PWM automaticamente alterna os períodos em que ela está ligada (HIGH) e em que está desligada (LOW). A proporção do tempo em que a saída está ligada em relação ao tempo total do ciclo
é chamado de Duty Cycle, e varia de 0 a 100%, ou no caso de 0 até 255.


# Executando Código 

O próximo passo, após o desenho do circuito, é desenvolver o código responsável pelo envio e recebimento dos dados pelo Arduino e a atuação de acordo com a necessidade do projeto. 


É Importante descatarmos alguns pontos, antes da implementação do código, é importante mostrar a estrutura mínima para o funcionamento no caso do Arduino são essencias:

**Função Void(Setup)**: chamado no ínicio da execução do programa e deve configurar os dispositivos a serem usados. 

**Função void loop**:executada dentro do laço principal de execução e é chamada enquanto a placa estiver ligada. 

**Classe Serial**:representa a classe que se comunica com o computador hospedeiros através da porta USB\serial. 

**Função delay(milisegundos)**:pausa e execução por X milissegundos. 

Observe pelo código a seguir como está representada a estrutura básica para o funcionamento do Arduino:



![code arduino 01](https://github.com/user-attachments/assets/bf2f660c-99b6-4cb1-a2a1-73bf9c114e04)



# Conclusões Finais 

A função analogWrite() envia para a porta ~D10 o valor mapeado de 0 até 1023 para 0 até 255. O final do código efetua a exibição dos valores na sáida pela porta Serial
com o comando Serial.print(saída), seguindo de um intervalo de 1 segundo delay(1000), repetindo o processo enquanto o dispositivo estiver ligado. 

Chegando quase ao final da execução do Projeto, é preciso clicar em Start Simulation, em em Serial Monitor ( na parte inferior logo abaixodo código) para visualizar o resultado final, 
reprsentado pela figura, por meio de um corte especial mostrando somente o código-fonte e saída serial. 


Disponível no link abaixo: 

https://www.tinkercad.com/things/4sGHuITMBj1/editel?returnTo=%2Fdashboard%2Fdesigns%2Fcircuits&sharecode=jfLGnN1EJz9pRzGXOZVemIhuTvJ8_Jigv70cAhPG7aQ



<img width="1536" height="640" alt="Fantastic Kieran" src="https://github.com/user-attachments/assets/3cd600d0-4120-49ff-bbbe-4c504fd3caed" />






**Sarah Marcela** 
**Defesa Cibernética** 



