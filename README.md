

 PROYECTO FINAL
 Convertidor Buck Sincrónico usando STM32
========================================================

Saul Villanueva Elias,
Emiliano Olaya Tobias,
Gael Hurtado.
 
Descripción:
Diseño e implementación de un convertidor Buck
sincrónico para regular energía de un panel solar
de 45V y 10A utilizando un STM32.

El sistema usa PWM para controlar MOSFETs mediante
un driver IR2110, permitiendo una conversión de
energía eficiente y estable.

Durante el proyecto se realizaron prácticas de:
•⁠  ⁠Blink LED

•⁠  ⁠PWM complementario

•⁠  ⁠Control con driver IR2110

•⁠  ⁠ADC y monitoreo



 FUNCIONAMIENTO GENERAL
========================================================

Panel Solar → Convertidor Buck → Filtro LC → Carga

STM32 → Driver IR2110 → MOSFETs

El convertidor Buck reduce el voltaje de entrada
utilizando conmutación de alta frecuencia (~50kHz).

La regulación del voltaje depende del Duty Cycle PWM:

Vout = D × Vin


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
→ Filtrado y reducción de ripple

10mΩ Shunt
→ Medición de corriente


 ADC Y MONITOREO
========================================================

El ADC del STM32 mide:

- Voltaje de entrada
- Voltaje de salida
- Corriente

Como el ADC soporta máximo 3.3V,
se utilizan divisores resistivos para protección.


 PROTECCIONES
========================================================

- Protección por sobrecorriente
- Protección por sobrevoltaje
- Protección térmica

Si ocurre una falla:
→ El PWM se deshabilita automáticamente.


 PCB EN KICAD
========================================================

El PCB fue diseñado considerando:

- Pistas anchas para 10A
- Plano de tierra
- Separación potencia/control
- Disipación térmica
- Reducción de ruido EMI


 RESULTADOS ESPERADOS
========================================================

- Regulación estable del voltaje
- Alta eficiencia energética
- Protección del sistema
- Monitoreo en tiempo real

