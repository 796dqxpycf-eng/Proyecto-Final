/*
========================================================
 PROYECTO FINAL
 Convertidor Buck Sincrónico usando STM32
========================================================

Descripción:
Este proyecto consiste en el diseño de un convertidor
DC-DC tipo Buck para regular la energía de un panel
solar de aproximadamente 45V y 10A utilizando un
microcontrolador STM32.

El sistema utiliza PWM para controlar MOSFETs de
potencia mediante un driver IR2110, permitiendo
regular el voltaje de salida de forma eficiente.

========================================================
 FUNCIONAMIENTO GENERAL
========================================================

Panel Solar → Convertidor Buck → Filtro LC → Carga

STM32 → Driver IR2110 → MOSFETs

El STM32 genera señales PWM de aproximadamente
50kHz para controlar la conmutación de los MOSFETs.

La regulación del voltaje depende del Duty Cycle:

Vout = D × Vin

========================================================
 COMPONENTES PRINCIPALES
========================================================

STM32F103C8T6
→ Control principal del sistema

IR2110PBF
→ Driver High Side / Low Side

IRFP460PBF
→ MOSFETs de potencia

100uH
→ Inductor principal

Capacitores
→ Reducción de ripple y filtrado

10mΩ Shunt
→ Medición de corriente

========================================================
 ADC Y MONITOREO
========================================================

El ADC del STM32 mide:

- Voltaje de entrada
- Voltaje de salida
- Corriente

El ADC soporta máximo 3.3V,
por ello se utilizan divisores resistivos.

========================================================
 PROTECCIONES
========================================================

- Protección por sobrecorriente
- Protección por sobrevoltaje
- Protección térmica

Si ocurre una falla:
→ El PWM se deshabilita automáticamente.

========================================================
 PCB EN KICAD
========================================================

El PCB fue diseñado considerando:

- Pistas anchas para 10A
- Plano de tierra
- Separación potencia/control
- Disipación térmica
- Reducción de ruido EMI

========================================================
*/
