# 🤖 PROYECTOS DE AUTOMATIZACIÓN CON ARDUINO

## 📚 Introducción

En este trabajo se presentan diferentes proyectos de automatización desarrollados utilizando **Arduino UNO** como controlador principal. La finalidad es aplicar conocimientos de programación y electrónica mediante el uso de sensores, actuadores y diferentes componentes electrónicos.

Los proyectos buscan solucionar situaciones cotidianas de manera automática, utilizando Arduino para recibir información de los sensores, procesarla y posteriormente controlar distintos dispositivos.

Los proyectos desarrollados son:

1. 🌡️ Ventilador automático.
2. 🪰 Detector de moscas.
3. 🌸 Aromatizador automático.
4. 🚨 Alarma de movimiento.
5. 🧴 Dispensador automático de alcohol gel.

---

# 🌡️ 1. VENTILADOR AUTOMÁTICO

## Descripción del proyecto

El ventilador automático es un sistema diseñado para controlar la temperatura de una sala de manera automática.

El sistema utiliza un **sensor de temperatura**, que permite medir constantemente la temperatura del ambiente. Arduino recibe esta información y la compara con un límite previamente establecido.

Cuando la temperatura supera el límite, Arduino activa un ventilador para ayudar a disminuir la temperatura. Cuando la temperatura vuelve a bajar, el ventilador se apaga automáticamente.

La temperatura y el estado del sistema pueden visualizarse mediante una pantalla LCD 16x2.

## Objetivo

Crear un sistema capaz de controlar automáticamente un ventilador dependiendo de la temperatura del ambiente.

## Componentes

* Arduino UNO.
* Sensor de temperatura TMP36 o DHT11.
* Motor DC o ventilador pequeño.
* Transistor o módulo relé.
* Pantalla LCD 16x2.
* LED verde.
* LED rojo.
* Buzzer.
* Botón.
* Resistencias.
* Protoboard.
* Cables.

## Funcionamiento

El sensor mide la temperatura y envía la información a Arduino. Si la temperatura supera el valor establecido, Arduino activa el ventilador y enciende el LED rojo.

Cuando la temperatura está por debajo del límite, el ventilador permanece apagado y se enciende el LED verde.

Además, si la temperatura alcanza un nivel demasiado alto, el buzzer puede emitir una alerta.

---

# 🪰 2. DETECTOR DE MOSCAS

## Descripción del proyecto

Este proyecto consiste en un sistema experimental capaz de detectar el movimiento de una mosca utilizando sensores.

Arduino recibe la información proporcionada por los sensores y procesa la señal para determinar si existe movimiento en la zona de detección.

Cuando se detecta movimiento, el sistema puede activar indicadores como un LED, un buzzer y un actuador.

## Objetivo

Desarrollar un sistema de detección automática utilizando sensores y Arduino.

## Componentes

* Arduino UNO.
* Sensor infrarrojo.
* Sensor de movimiento.
* Láser de baja potencia como indicador.
* LED.
* Buzzer.
* Pantalla LCD.
* Botón.
* Resistencias.
* Protoboard.
* Cables.

## Funcionamiento

Los sensores permanecen monitoreando el área. Cuando detectan movimiento, envían una señal a Arduino.

Arduino procesa esta señal y activa los indicadores correspondientes. La pantalla LCD puede mostrar el estado del sistema y el buzzer puede emitir una alerta.

El láser se considera únicamente como un **indicador de detección de baja potencia**, evitando utilizarlo para causar daño a personas o animales.

---

# 🌸 3. AROMATIZADOR AUTOMÁTICO

## Descripción del proyecto

El aromatizador automático es un sistema que permite activar un dispensador de aromatizante automáticamente después de un determinado período de tiempo.

Para realizar el mecanismo se utiliza un **servomotor**, el cual se encarga de realizar un movimiento para presionar el dispensador.

Por ejemplo, el sistema puede configurarse para activar el aromatizador cada 30 segundos.

## Objetivo

Crear un sistema automático que permita controlar un aromatizador mediante un servomotor y Arduino.

## Componentes

* Arduino UNO.
* Servomotor.
* Botón.
* LED verde.
* LED rojo.
* Buzzer.
* Pantalla LCD 16x2.
* Resistencias.
* Protoboard.
* Cables.

## Funcionamiento

Arduino controla el tiempo mediante la función `millis()`.

Cuando transcurre el intervalo establecido, Arduino activa el servomotor. El servo se mueve hasta una posición determinada para presionar el aromatizador y luego vuelve a su posición inicial.

El LED rojo indica que el sistema está realizando la activación, mientras que el LED verde indica que se encuentra esperando.

---

# 🚨 4. ALARMA DE MOVIMIENTO

## Descripción del proyecto

La alarma de movimiento es un sistema de seguridad que utiliza un **sensor PIR** para detectar movimiento dentro de una sala.

Cuando el sensor detecta movimiento, Arduino procesa la señal y activa una alarma mediante un buzzer y un LED rojo.

## Objetivo

Crear un sistema de seguridad capaz de detectar movimiento y generar una alerta automáticamente.

## Componentes

* Arduino UNO.
* Sensor PIR.
* Buzzer.
* LED rojo.
* LED verde.
* Botón.
* Pantalla LCD 16x2.
* Resistencias.
* Protoboard.
* Cables.

## Funcionamiento

El sensor PIR permanece detectando cambios de movimiento.

Cuando una persona entra o se mueve dentro del área de detección, el sensor envía una señal HIGH a Arduino.

Arduino interpreta la señal y activa el buzzer y el LED rojo. La pantalla LCD muestra un mensaje indicando que se ha detectado movimiento.

Cuando no existe movimiento, el sistema vuelve a su estado normal.

El botón permite activar o desactivar la alarma.

---

# 🧴 5. DISPENSADOR AUTOMÁTICO DE ALCOHOL GEL

## Descripción del proyecto

El dispensador automático de alcohol gel permite entregar una cantidad de producto sin necesidad de tocar el envase.

Para detectar la mano se utiliza un **sensor ultrasónico HC-SR04**. Cuando la mano se encuentra a una distancia determinada, Arduino activa un servomotor que presiona el dispensador.

## Objetivo

Crear un sistema higiénico y automático capaz de entregar alcohol gel mediante la detección de una mano.

## Componentes

* Arduino UNO.
* Sensor ultrasónico HC-SR04.
* Servomotor.
* LED verde.
* LED rojo.
* Buzzer.
* Botón.
* Pantalla LCD 16x2.
* Resistencias.
* Protoboard.
* Cables.
* Envase de alcohol gel.

## Funcionamiento

El sensor ultrasónico mide constantemente la distancia existente frente al dispensador.

Cuando detecta un objeto, como una mano, a una distancia menor al límite establecido, Arduino activa el servomotor.

El servomotor realiza un movimiento que presiona el dispensador y entrega una pequeña cantidad de alcohol gel.

Durante el proceso, el LED rojo se enciende y el buzzer puede emitir un sonido. La pantalla LCD muestra el mensaje **"Dispensando..."**.

Después de realizar la acción, el servomotor vuelve a su posición inicial y el sistema queda nuevamente preparado.

---

# 🔌 FUNCIONAMIENTO GENERAL

Todos los proyectos utilizan Arduino UNO como unidad principal de control.

El funcionamiento general puede dividirse en tres etapas:

### 1. Entrada

Los sensores reciben información del entorno.

Ejemplos:

* Sensor de temperatura → mide la temperatura.
* Sensor PIR → detecta movimiento.
* Sensor ultrasónico → detecta distancia.
* Sensor infrarrojo → detecta objetos o movimiento.

### 2. Procesamiento

Arduino recibe las señales de los sensores y ejecuta el programa correspondiente.

Dependiendo de la información recibida, Arduino toma una decisión.

### 3. Salida

Arduino controla diferentes dispositivos:

* LEDs.
* Buzzer.
* Servomotor.
* Ventilador.
* Pantalla LCD.
* Otros actuadores.

---

# 🎯 Objetivo General

Desarrollar diferentes sistemas automatizados utilizando Arduino UNO, aplicando conocimientos de programación, electrónica, sensores y actuadores para resolver situaciones prácticas de la vida cotidiana.

# 🎯 Objetivos Específicos

* Aprender a utilizar Arduino UNO.
* Comprender el funcionamiento de diferentes sensores.
* Utilizar actuadores controlados mediante Arduino.
* Implementar sistemas automáticos.
* Aprender a programar entradas y salidas digitales y analógicas.
* Mostrar información mediante una pantalla LCD.
* Aplicar conocimientos de electrónica en proyectos prácticos.
* Desarrollar soluciones tecnológicas simples y funcionales.

# 🧠 Conclusión

La realización de estos proyectos permite comprender cómo Arduino puede utilizarse para crear sistemas automáticos capaces de responder a diferentes situaciones.

Cada proyecto utiliza sensores para obtener información del entorno y Arduino se encarga de procesarla para controlar distintos dispositivos.

El ventilador automático permite controlar la temperatura, el detector de moscas demuestra el uso de sensores de detección, el aromatizador automatiza una acción repetitiva, la alarma de movimiento permite implementar un sistema básico de seguridad y el dispensador de alcohol gel demuestra una aplicación práctica de sensores y servomotores.

En conclusión, estos proyectos permiten aplicar de manera práctica conceptos de **programación, electrónica, automatización y control**, demostrando las posibilidades que ofrece Arduino para desarrollar soluciones tecnológicas.
