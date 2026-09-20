# Sistema de Gestión Climática Inteligente — Fase 1

Proyecto enfocado en el diseño teórico de un sistema de refrigeración termoeléctrico capaz de producir temperaturas subambiente, monitorear variables climáticas y plantear una arquitectura para la transmisión y almacenamiento de datos en tiempo real.

---

## Dashboard de monitoreo

Puedes visualizar la interfaz propuesta para la Fase 1 aquí:

[Abrir Dashboard de Gestión Climática](https://emikuchaw.github.io/Sistema-Gestion-Climatica-Fase1./)

> **Nota:** actualmente el dashboard utiliza datos simulados únicamente para demostrar el funcionamiento conceptual de la adquisición, transmisión, visualización y almacenamiento de información.

---

## Objetivo de la Fase 1

Diseñar teóricamente un sistema de refrigeración capaz de disminuir la temperatura de una carga por debajo de la temperatura ambiente e integrar conceptualmente:

- Sensores de temperatura.
- Sensor de humedad relativa.
- Adquisición de datos.
- Transmisión de información en tiempo real.
- Almacenamiento de mediciones.
- Visualización mediante una interfaz web.
- Análisis mediante la Primera y Segunda Ley de la Termodinámica.

---

## Sistema de refrigeración propuesto

Para esta fase se propone utilizar un sistema de refrigeración termoeléctrico mediante un **módulo Peltier**.

### Flujo térmico propuesto

Carga térmica / agua  
↓  
Bloque frío o intercambiador  
↓  
Módulo Peltier  
↓  
Disipador tipo cooler de CPU  
↓  
Ventilador  
↓  
Ambiente  

El módulo Peltier transporta calor desde el lado frío hacia el lado caliente utilizando energía eléctrica.

---

## ¿Por qué utilizar una Peltier?

La tecnología Peltier fue seleccionada para esta etapa debido a que ofrece:

- Tamaño compacto.
- Ausencia de refrigerantes.
- Fácil integración electrónica.
- Control mediante corriente eléctrica.
- Compatibilidad con microcontroladores.
- Pocas partes móviles.
- Facilidad para integrar sensores.
- Posibilidad de aplicar control automático en etapas posteriores.

Aunque su eficiencia energética es menor que la de otros sistemas como la compresión de vapor, resulta adecuada para un prototipo académico a pequeña escala.

---

## Arquitectura de adquisición de datos

```text
Sensores
   ↓
 ESP32
   ↓
 Wi-Fi
   ↓
Dashboard
   ↓
Almacenamiento
