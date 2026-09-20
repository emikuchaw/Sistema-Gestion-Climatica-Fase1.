# Sistema de Gestión Climática Inteligente — Fase 1

Repositorio conceptual correspondiente a la **Fase 1** del proyecto.

## Objetivo

Diseñar teóricamente un sistema de refrigeración termoeléctrico capaz de alcanzar una condición subambiente, monitorear temperatura y humedad, y plantear una arquitectura para transmitir, visualizar y almacenar datos en tiempo real.

> **Importante:** los valores mostrados actualmente en el dashboard son **datos simulados** utilizados únicamente para demostrar el funcionamiento conceptual de la interfaz. No corresponden a mediciones experimentales.

## Sistema de refrigeración propuesto

Se propone utilizar refrigeración termoeléctrica mediante un módulo **Peltier**, acompañado de:

- bloque frío o intercambiador;
- disipador tipo cooler de CPU;
- ventilación forzada;
- sensores de temperatura y humedad;
- ESP32 o microcontrolador equivalente;
- interfaz web para visualización;
- almacenamiento de datos.

## Arquitectura propuesta

```text
Sensores
   ↓
 ESP32
   ↓
 Wi‑Fi
   ↓
Dashboard
   ↓
Almacenamiento
```

## Dashboard

El archivo principal es:

`index.html`

Incluye de forma demostrativa:

- temperatura del agua;
- temperatura ambiente;
- humedad relativa;
- temperatura del lado frío;
- temperatura del lado caliente;
- voltaje;
- corriente;
- potencia;
- temperatura mínima registrada;
- gráfica temperatura vs. tiempo;
- historial de datos;
- almacenamiento local;
- exportación CSV.

## Dimensionamiento teórico base

Condición de diseño preliminar:

- Volumen de agua: **250 mL**
- Masa aproximada: **0.250 kg**
- Temperatura inicial: **25 °C**
- Temperatura objetivo de cálculo: **13 °C**
- Energía térmica a retirar: **12.54 kJ**
- Tiempo de diseño: **600 s**
- Capacidad frigorífica ideal: **20.9 W**

## Estructura del repositorio

```text
Sistema-Gestion-Climatica-Fase1/
├── index.html
├── README.md
├── assets/
│   ├── boceto_sistema_peltier.png
│   └── ciclo_refrigeracion_peltier.png
├── data/
│   └── datos_simulados.csv
├── calculos/
│   └── README.md
└── docs/
    └── README.md
```

## Uso

Abrir `index.html` en cualquier navegador moderno.

Cuando se implemente el prototipo físico, la generación de datos simulados podrá sustituirse por lecturas reales enviadas por un ESP32.

## Estado del proyecto

**Fase 1:** desarrollo teórico y demostración conceptual de adquisición, transmisión, visualización y almacenamiento de datos.
