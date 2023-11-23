----

# Braço Robótico


SISTEMAS EMBARCADOS

4° Semestre - FATEC Jundiaí

Integrantes:


-Misael Fernandes Soares;


-Rafael Massayoshi Hamazaki;


----

# Sumário

1 - Introdução;

2 - Materiais;

3 - Código-Fonte;

4 - Conclusão do Projeto;




----


# 1 - Introdução


Com o advento da Industria 4.0 ou Quarta Revolução Industrial, que engloba as tecnologias de Inteligência Artificial, Internet das Coisas, Computação em Nuvem, Big Data entre outras. A partir da integração entre os sistemas (Computação, Mecânica, Eletrônica), deriva-se a robótica e a automação, que são técnicas destinadas a automatizar os processos industriais, substituindo o trabalho físico e mental do homem por equipamentos.
As tecnologias de Inteligência Artificial, Internet das Coisas, Computação em Nuvem, Big Data, e a integração com a robótica e automação com objetivo de promover a otimização dos processos industriais, com o consequente aumento da produtividade e lucratividade.
Neste sentido, o braço robótico vem sendo utilizado em diferentes nichos da indústria, pela sua versatilidade, pois pode ser empregado nas mais diversas atividades, produzir por dias a fio, repetindo a mesma atividade de forma incansável e substituindo a necessidade de um operador, evitando que seja afetado por um trabalho repetitivo ou fisicamente desgastante.


----

# 2 - Materiais


Para a montagem do Braço Robótico, foram adquiridos separadamente um Microcontrolador ATMEGA 328 (Arduino Uno), 4 servos motores (controlados por um conjunto de joysticks) que serão conectados a um Chassi Acrílico composto por articulações e juntas.

+ ATMEGA 328P (Arduino Uno)

  ![Arduino](https://github.com/RafaelHamazaki/Braco-Robotico/assets/106597490/3bb7b7a5-014b-4812-89ea-e05c1ad8e5fa)

+ Placa de Expansão

![Expansao](https://github.com/RafaelHamazaki/Braco-Robotico/assets/106597490/1cedfb5a-f993-48ee-ae46-578f30647a39)

+ Braço Robótico em Acrílico

![Braco](https://github.com/RafaelHamazaki/Braco-Robotico/assets/106597490/e2f94ec3-2537-4035-b3c3-410825baaa90)


+ Micro Servo Motor

  ![Servo](https://github.com/RafaelHamazaki/Braco-Robotico/assets/106597490/0b00882a-036b-47f5-8c51-687d838b780c)


+ Módulo Joystick

  ![Joystick](https://github.com/RafaelHamazaki/Braco-Robotico/assets/106597490/7a0cf3cb-a50a-4358-a87b-44515d2c282f)
  


Segue video do projeto:

https://github.com/RafaelHamazaki/Braco-Robotico/assets/106597490/9328e398-135d-4ba4-9b28-5d00fb690a73

  
# 3 - Código Fonte

```


// BLOG Eletrogate
// Kit Braço Robótico MDF com Arduino
// https://blog.eletrogate.com/kit-braco-robotico-mdf-com-arduino/
 
 
#define potpin1  2
#define potpin2  3
#define potpin3  4
#define potpin4  5
 
#include <Servo.h>
 
Servo myservoBase;  // Objeto servo para controlar a base
Servo myservoGarra;  //Objeto servo para controlar a garra
Servo myservoAltura; //Objeto servo para controlar a altura do braço
Servo myservoProfundidade; //Objeto servo para profundidade a altura do braço
 
 
int val;    // variable to read the value from the analog pin
 
void setup()
{
  //Associa cada objeto a um pino pwm
  myservoBase.attach(3);
  myservoGarra.attach(5);
  myservoAltura.attach(9);
  myservoProfundidade.attach(11);
}
 
void loop()
{
 
  val = map(analogRead(potpin1), 0, 1023, 0, 179);
  myservoBase.write(val);
 
  val = map(analogRead(potpin2), 0, 1023, 0, 179);
  myservoGarra.write(val);
 
  val = map(analogRead(potpin3), 0, 1023, 0, 179);
  myservoAltura.write(val);
 
  val = map(analogRead(potpin4), 0, 1023, 0, 179);
  myservoProfundidade.write(val);
}


```


----


# 4 - Conclusão do Projeto

Finalizadas as execuções das etapas presentes em cada tópico do documento do sistema, nota-se que o protótipo alcançado assemelha-se bastante ao ambiente de uma linha de produção industrial. Quase todos os possíveis problemas encontrados foram adequadamente encaminhados e tratados, dentre eles a montagem mecânica e a programação e a validação dos resultados, conforme configura o planejamento dos requisitos do projeto.


Todo o processo de planejamento e execução do projeto, respeitando e validando todo o fluxo do processo determinado, é possível avaliar em conjunto que o que temos como resultado se aproxima muito do que foi proposto no kick-off do projeto, existem sim algumas variáveis que por alguma razão não entendemos ser importante controlar no início (como os elementos de fixação dos sensores) e que de certa forma provocou alguns impactos em nosso tempo de realização assim como no resultado, mas com as ferramentas utilizadas, o apoio dos professores e a boa relação dos integrantes foi possível realizar a entrega, com qualidade.


Com foco especifico na execução do projeto, é possível analisar que do planejamento a execução é de extrema importância, o domínio sobre os ajustes mecânicos e toda a sua montagem, a complexidade de integrar os elementos em um escopo que permita extrair o máximo de qualidade e funcionamento de todos os elementos envolvidos nos faz pensar que o uso de uma ferramenta de CAD, com desenho assistido por computador seja um conhecimento que mitiga os riscos de execução no rascunho do projeto de desenho analisando com foco na realização, a funcionalidade do projeto do braço robótico integra de maneira satisfatória com o sistemas de movimentação do braço robótico, e que para nós elementos do grupo foi uma grande experiência poder realizar esse trabalho, em todos os aspectos, programação, processo de compras, montagem e as discussões do grupo, amadurecendo nosso relacionamento interpessoal e nossa comunicação profissional.
