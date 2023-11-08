# ESCUELA TÉCNICA N°1 “Otto Krause”
## TALLER DE ELECTRÓNICA

# Informe: Estacion metereologica | Martin Sanchez || Thomas Acosta 

## Indice
---
## Descripcion del proyecto

### *Descripcion de la problematica:

- Una pequeña estación meteorológica podría solucionar diversas problemáticas relacionadas con la recopilación de datos climáticos y el monitoreo de las condiciones atmosféricas en una ubicación específica. Algunas de las problemáticas que podría abordar son:

  - Predicción del clima local

  - Alertas tempranas de fenómenos meteorológicos extremos

  - Monitoreo de la calidad del aire

  - Investigación científica local

  - Agricultura y gestión del agua

  - Eficiencia energética

  - Seguridad en el transporte

En resumen, una pequeña estación meteorológica puede solucionar problemáticas relacionadas con la falta de datos climáticos precisos y en tiempo real, y puede tener una amplia gama de aplicaciones en diversas áreas, desde la planificación diaria hasta la toma de decisiones críticas en sectores como la agricultura, la investigación científica y la seguridad.

---

### *Caracterisiticas del sistema:
- Una pequeña estación meteorológica generalmente está diseñada para recopilar datos básicos sobre las condiciones climáticas en una ubicación específica. A continuación, se presentan algunas características comunes de una pequeña estación meteorológica:

  - Sensores e instrumentos

  - Transmisión de datos

  - Registro y almacenamiento de datos

  - Alimentación energética
  
  - Durabilidad y protección

  - Interfaz de usuario

  - Conectividad y compatibilidad


- Existen varias mejoras que se podrían implementar en una pequeña estación meteorológica para ampliar su funcionalidad y precisión. Algunas de estas mejoras podrían incluir:

    - Sensores adicionales
    - Comunicación mejorada
    - Integración con sistemas de automatización

    - Interfaz de usuario avanzada

    - Integración con sistemas de alerta temprana

    - Acceso a datos históricos y almacenamiento en la nube

Estas mejoras podrían hacer que la pequeña estación meteorológica sea aún más versátil y valiosa para una variedad de aplicaciones, desde la toma de decisiones en la agricultura y la investigación científica hasta el monitoreo ambiental y la planificación urbana.

---



### *Diagrama de bloques:
![Diagrama de bloques](images/Diagrama-en-blanco.png)

- Sensores:
  - Temperatura y Humedad: Estas dos variables seran medidas por un mismo sensor en tiempo real. (Htu21d)
  - Precipitacion: Para esta variable se usara un sistema en el cual se ira midiendo la precipitacion de a 2ml, el sistema sera parecido a un "sube y baja", y cada vez que se realice un cambio de movimiento, mediante un iman acoplado a la estructura y a un sensor de efecto hall, se iran contando la cantidad de veces que esto sucede. (A3144)
  - Radiacion solar: Este sensor medira el nivel de radiacion uv en tiempo real, en base a esta medicion se mostrara, ademas del valor, la escala correspondiente de raciacion. (Guva-s12s)
  - Direccion del viento: Esta variable sera sensada con una veleta, para saber la posicion de la veleta se probara con sensores de efecto o con una serie de disco B&W pintados con distintas divisiones indicando distintas posiciones, para saber si el disco en cierta posicion es blanco o negro se usaran sensores infrarrojos. (Efecto hall: A3144) (Infrarrojo: Lm393)
  - Velocidad del viento: Esta variable sera sensada con un anemometro, la velocidad se medira por la cantidad de vueta que se den en un lapso de tiempo, se usara un sensior de efecto hall para saber cuando se dio una vuelta. (A3144)
  - Presion atmosferica: Este sensor medira la presion atmosferica en tiempo real. (BMP280)
 
- Procesamiento y almacenamiento: Todos los datos recibidos por los sensores seran procesados por el microcontrolador ESP32, y opcionalmente guardados en una unidad de almacenamiento. Estos datos seran mostrador por display y una aplicacion y/o pagina web.

- Entrega de datos: La entrega de datos que saldran, una vez procesados por el microcontrolador, seran mostrados por una pequeña pantalla OLED y por una pagina web o aplicacion, en estas dos ultimas se hara uso de la tecnologia WI-FI del micro para que sea posible la transmision de datos de manera inalambrica.

- Interaccion: Este apartado es opcional, pero se tiene pensado que mediante una botonera, el usuario, viendo en la pantalla OLED, pueda navegar entre menues para poder mas y de manera mas comoda la informacion.
---


## Listado de componentes 
### Microcontrolador

Nombre: ESP32 - Wi-Fi & Bluetooth MCU
![ESP32](images/esp32.png)
Descripcion: ESP32 de 38 Pines es una placa de desarrollo que integra el microcontrolador ESP32-WROOM-32 SMD de Espressif. Esta placa permite controlar todo tipo de sensores, módulos y actuadores mediante WIFI y BLUETOOTH, para proyectos de Internet de las cosas “IoT” de forma eficiente y económica.

Caracteristicas tecnicas: 
Tipo: Módulo Wifi + Bluetooth
Modelo: ESP32 38 Pines
Voltaje de Alimentación (USB): 5V DC
Voltaje de Entradas/Salidas: 3.3V DC
Consumo de energía de 5μA en modo de suspensión
CPU principal: Tensilica Xtensa 32-bit LX6
Frecuencia de Reloj: hasta 240Mhz
Procesador secundario: Permite hacer operaciones básica en modo de ultra bajo consumo
Wifi: 802.11 b/g/n/e/i (802.11n @ 2.4 GHz hasta 150 Mbit/s)
Bluetooth: 4.2 BR/EDR BLE Modo de control dual
Memoria: 448 KByte ROM, 520 KByte SRAM, 6 KByte SRAM en RTC y QSPI admite múltiples chips flash /
SRAM
Chip USB-Serial: CP2102
Antena en PCB
Pines Digitales GPIO: 24  (Algunos pines solo como entrada)
Conversor Analógico Digital: Dos ADC de 12bits tipo SAR, soporta mediciones en hasta 18 canales, algunos pines soporta un amplificador con ganancia programable

![ESP32](images/ESP32-Pinout.png)
### Sensor Intensidad Luz UV 

Nombre: Guva-s12s 

### Sensor de humedad y temperatura

Nombre: AHT10

### Sensor de presion atmosferica

Nombre: BMP280

### Sensor efecto Hall

Nombre: A3144

### Adaptador de nivel logico 

Nombre: CJMCU 0108

### Pantalla OLED

Nombre: SSH1106

### Bateria

Nombre: Power bank 5000 mAh

