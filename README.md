Proyecto: Comunicador en Código Morse con micro:bit
📌 Descripción general

Este proyecto implementa un sistema de comunicación inalámbrica en código Morse utilizando placas BBC micro:bit y el módulo de radio integrado.
Cada micro:bit utiliza el mismo programa, pudiendo actuar como emisor o receptor según la interacción del usuario.

El mensaje se construye localmente en código Morse, se envía completo por radio, y el micro:bit receptor lo decodifica y muestra en texto.

🎯 Objetivo

Implementar un traductor de código Morse → texto

Utilizar radiofrecuencia para comunicar micro:bits

Diseñar un protocolo simple de transmisión

Aplicar lógica de eventos, manejo de strings y estructuras de datos

🧩 Funcionamiento general

El usuario ingresa el mensaje en Morse usando los botones

El mensaje se guarda en memoria

Al confirmar el envío, se transmite por radio

El micro:bit receptor decodifica el mensaje

El texto resultante se muestra en la pantalla LED

🎮 Controles
Entrada de código Morse
Acción	Botón
Punto (.)	Botón A
Raya (-)	Botón B
Fin de letra (`	`)
Enviar mensaje completo	Agitar el micro:bit
📡 Comunicación por radio

Grupo de radio: 42

Tipo de mensaje: string

Protocolo:

. y - → símbolos Morse

| → fin de letra

Ejemplo de mensaje transmitido:

....|---|.-..

🔁 Arquitectura del sistema

Código único para emisor y receptor

El comportamiento depende del evento:

Botones → emisión

Radio → recepción

No existe distinción fija entre dispositivos

🗂️ Estructura del código

Diccionario Morse (arrays paralelos)

Buffer de mensaje Morse

Función de traducción

Eventos de entrada (botones y gestos)

Evento de recepción por radio

🧪 Pruebas
En simulador MakeCode

Abrir dos micro:bits

Cargar el mismo código en ambos

Ingresar un mensaje en uno

Agitar para enviar

El otro micro:bit muestra el texto decodificado

En hardware real

Ambos micro:bits deben estar:

Encendidos

En el mismo grupo de radio

A una distancia adecuada

⚠️ Limitaciones

No se soportan números ni símbolos especiales

No hay corrección de errores

No se distinguen presiones cortas y largas

El envío se realiza manualmente

🚀 Posibles mejoras

Soporte para palabras (espacios)

Confirmación de recepción

Borrar mensaje

Soporte para números y signos

Visualización del mensaje completo antes de enviar

🛠️ Tecnologías utilizadas

BBC micro:bit

MakeCode (JavaScript / TypeScript)

Radio integrada micro:bit
