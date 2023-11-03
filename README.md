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


### *Estudio de factibilidad:

  Como ya se vio en la investigacion de los antecedentes de la estacion metereologica existen muchas funciones que se pueden aplicar, pero en el proyecto se van a tomar como esenciales la implementacion de los siguientes items:
  
  -Microcontrolador: Se usara el ESP32 por su buena capacidad de procesamiento, cantidad de perifericos, cantidad de puertos, cantidad de puertos GPIO y mas iportante en este proyecto, comunicacion wifi y bluetooth.
  - Sensores:
    - Temperatura
    - Humedad
    - Precipitacion
    - Direccion del viento
    - Velocidad del viento
    - Presion atmosferica
    - Indice UV
  * Los sensores usados se explican en el diagrama de bloques
  
  - Muestra de Datos mediante display OLED
  - Muestra de datos mediante aplicacipn y pagina web (WIFI)
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



