# Wiki Automatizacion
## Introduccion

Esta wiki creada para la clase de automatización 2022-1 será utilizada para exponer la creación y otra documentación de la creación del parcial correspondiente al segundo corte

## Etapas de diseño
#### Planeación 
Usando los conocimientos adquiridos en la clase, la primera consideración son los elementos del sistema, el sistema consiste esencialmente de 3 motores y 3 válvulas, se planea el uso de leds y una placa ARDUINO MEGA para la elaboración del elemento práctico propuesto. 

#### Diseño preliminar
Se planea la creación de un sistema simple utilizando una placa Arduino como controlador principal y luces led para simular los actuadores hipotéticos a utilizar, además se usa otro juego de luces para simbolizar los estados de ejecución. 

## Desarrollo
#### Simulación

![Imagen de la simulacion](https://cdn.discordapp.com/attachments/786050339643195447/961482481981333514/visualizacion.png)

El diseño del prototipo se realiza en la plataforma CODESYS, la cual nos facilita una visión hipotética del sistema a través de la creación de animaciones simples que están vinculadas a una lógica de diseño Ladder que se usara mas adelante en el propio dispositivo PLC, pro lo tanto CODESYS nos permite tener un entorno en el que podemos organizar y crear un sistema sin la necesidad de saltar directamente a la implementación física, esto a su vez ayuda a la mitigación de errores futuros.

#### Uso de OpenPLC

![Runtime](https://cdn.discordapp.com/attachments/786050339643195447/961484586787962930/unknown.png)

La plataforma OpenPLC nos permite la implementación de la lógica Ladder generada previamente, en primer lugar, se usara como dispositivo maestro un computador portátil con el sistema operativo Windows y el dispositivo esclavo será una placa de desarrollo Arduino MEGA, esta configuración se usa debido a su flexibilidad y accesibilidad económica. Primero se configura el run time en el dispositivo maestro para que genere el Host necesario en el que se pueda añadir el dispositivo esclavo a utilizar, una vez hecho esto se puede empezar a trabajar en la lógica Ladder en el editor de OpenPLC, se realizan ajustes menores a la lógica original y se añaden las conexiones a los pines correspondientes.

## Implementación 
#### Materiales 
Como se mencionó anteriormente se utilizarán luces LED para simular los elementos del sistema y también para permitir retroalimentación referente a los estados del sistema, además se usara una placa Arduino MEGA, claves jumper y un protoboard para facilitar las conexiones de manera rápida.

#### Prototipado 

#### Diagramas relevantes
Diagramas relevantes 

![Diagrama de proceso](https://cdn.discordapp.com/attachments/786050339643195447/961505999473242142/diagrama_secuencia.png)

![Tabla de variables](https://cdn.discordapp.com/attachments/786050339643195447/961484131357818930/tabla_1.png)

![Tabla de variables](https://cdn.discordapp.com/attachments/786050339643195447/961484131357818930/tabla_1.png)

## Referencias
