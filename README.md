/*
==================================================
 PROYECTO FINAL
 Convertidor Buck con STM32
==================================================

Descripción:
Sistema encargado de regular el voltaje de un
panel solar utilizando un convertidor Buck
controlado mediante un STM32.

==================================================
 FUNCIONAMIENTO
==================================================

Panel Solar → Buck → Carga

STM32 → Driver IR2110 → MOSFETs

El STM32 genera PWM para controlar los MOSFETs
y regular el voltaje de salida.

==================================================
 COMPONENTES PRINCIPALES
==================================================

STM32F103C8T6
→ Control del sistema

IR2110
→ Driver de compuerta

IRFP460PBF
→ MOSFETs de potencia

100uH
→ Inductor principal

Capacitores
→ Filtrado de ruido y ripple

10mΩ Shunt
→ Medición de corriente

==================================================
 ADC
==================================================

El ADC mide:

- Voltaje de entrada
- Voltaje de salida
- Corriente

El STM32 soporta máximo 3.3V,
por eso se utilizan divisores resistivos.

==================================================
 PROTECCIONES
==================================================

- Sobrecorriente
- Sobrevoltaje
- Protección térmica

Si ocurre una falla:
→ El PWM se deshabilita.

==================================================
 PCB
==================================================

Diseñado en KiCad considerando:

- Pistas anchas
- Plano de tierra
- Separación potencia/control
- Disipación térmica

==================================================
*/
