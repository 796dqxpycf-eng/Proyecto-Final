# Convertidor Buck Sincrónico para Aplicaciones Fotovoltaicas usando STM32

## Descripción General

Este proyecto consiste en el diseño e implementación de un convertidor DC-DC tipo Buck sincrónico controlado mediante un microcontrolador STM32 para aplicaciones fotovoltaicas. El sistema regula la energía proveniente de un panel solar con parámetros aproximados de:

- Voltaje máximo del panel: 45V
- Corriente máxima: 10A
- Potencia aproximada: 450W

El objetivo principal es reducir y controlar el voltaje del panel solar mediante PWM utilizando un STM32 y una etapa de potencia basada en MOSFETs.

---

# Objetivos del Proyecto

## Objetivo General

Diseñar un convertidor Buck controlado digitalmente mediante STM32 para regulación de energía fotovoltaica.

## Objetivos Específicos

- Implementar control PWM.
- Regular voltaje de salida.
- Monitorear corriente y voltaje mediante ADC.
- Implementar protecciones electrónicas.
- Diseñar PCB en KiCad.
- Generar documentación técnica y BOM.

---

# Arquitectura General del Sistema

```text
Panel Solar → Convertidor Buck → Filtro LC → Carga

STM32 → Driver MOSFET → MOSFETs de Potencia
