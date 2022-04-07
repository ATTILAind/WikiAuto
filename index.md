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
Para el prototipad final se realizo un montaje como el que se ve a continuación:
![Plano A](https://raw.githubusercontent.com/ATTILAind/WikiAuto/gh-pages/Plan%20B.jpg)
![Plano B](https://raw.githubusercontent.com/ATTILAind/WikiAuto/gh-pages/Plano%20A.jpg)
![Otra](https://raw.githubusercontent.com/ATTILAind/WikiAuto/gh-pages/OtraARD.jpeg)

Y de esta manera se consiguió el resultado final 
![Prototipo](https://raw.githubusercontent.com/ATTILAind/WikiAuto/gh-pages/Proto%20final.jpeg)
El prototipo usa leds para representar elementos mecánicos del sistema hipotético e imita el esquema general sugerido en el documento original 


#### Diagramas relevantes
Diagrama de secuencia y tabla de variables 
[Diagrama de secuencia en PDF](https://viewscreen.githubusercontent.com/view/pdf?browser=firefox&color_mode=auto&commit=b4d3d911a7f460bddd34b58f31cf40fe955df23f&device=unknown_device&enc_url=68747470733a2f2f7261772e67697468756275736572636f6e74656e742e636f6d2f415454494c41696e642f57696b694175746f2f623464336439313161376634363062646464333462353866333163663430666539353564663233662f6469616772616d615f64655f73656375656e6369612e706466&logged_in=true&nwo=ATTILAind%2FWikiAuto&path=diagrama_de_secuencia.pdf&platform=windows&repository_id=478793554&repository_type=Repository&version=98#fa6d76c1-864b-43f6-8ed8-6b4d19684f6c)

![Diagrama de proceso](https://cdn.discordapp.com/attachments/786050339643195447/961505999473242142/diagrama_secuencia.png)

![Tabla de variables](https://cdn.discordapp.com/attachments/786050339643195447/961484131357818930/tabla_1.png)


## Referencias
-“OPENPLC ON WINDOWS” [ Internet ]
Disponible en: https://www.openplcproject.com/runtime/windows/
-"Codigo de Codesys", apuntes de clase de INFORM 275902, Facultad de ingeniería,
Universidad de la Sabana, Abril, 2022.


