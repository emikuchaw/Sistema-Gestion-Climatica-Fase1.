\# Sistema de Gestión Climática Inteligente — Fase 1



Proyecto enfocado en el diseño teórico de un sistema de refrigeración termoeléctrico capaz de producir temperaturas subambiente, monitorear variables climáticas y plantear una arquitectura para la transmisión y almacenamiento de datos en tiempo real.



\---



\## Dashboard de monitoreo



Puedes visualizar la interfaz propuesta para la Fase 1 aquí:



👉 \[Abrir Dashboard de Gestión Climática](https://emikuchaw.github.io/Sistema-Gestion-Climatica-Fase1/)



> \*\*Nota:\*\* actualmente el dashboard utiliza datos simulados únicamente para demostrar el funcionamiento conceptual de la adquisición, transmisión, visualización y almacenamiento de información.



\---



\## Objetivo de la Fase 1



Diseñar teóricamente un sistema de refrigeración capaz de disminuir la temperatura de una carga por debajo de la temperatura ambiente e integrar conceptualmente:



\- Sensores de temperatura.

\- Sensor de humedad relativa.

\- Adquisición de datos.

\- Transmisión de información en tiempo real.

\- Almacenamiento de mediciones.

\- Visualización mediante una interfaz web.

\- Análisis mediante la Primera y Segunda Ley de la Termodinámica.



\---



\## Sistema de refrigeración propuesto



Para esta fase se propone utilizar un sistema de refrigeración termoeléctrico mediante un \*\*módulo Peltier\*\*.



\### Flujo térmico propuesto



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



\---



\## ¿Por qué utilizar una Peltier?



La tecnología Peltier fue seleccionada para esta etapa debido a que ofrece:



\- Tamaño compacto.

\- Ausencia de refrigerantes.

\- Fácil integración electrónica.

\- Control mediante corriente eléctrica.

\- Compatibilidad con microcontroladores.

\- Pocas partes móviles.

\- Facilidad para integrar sensores.

\- Posibilidad de aplicar control automático en etapas posteriores.



Aunque su eficiencia energética es menor que la de otros sistemas como la compresión de vapor, resulta adecuada para un prototipo académico a pequeña escala.



\---



\## Arquitectura de adquisición de datos



La arquitectura propuesta para futuras mediciones reales es:



Sensores  

↓  

ESP32  

↓  

Wi-Fi  

↓  

Dashboard web  

↓  

Almacenamiento de datos



Durante esta fase, los valores utilizados en el dashboard son simulados.



En una implementación física posterior, la simulación podrá ser sustituida por lecturas reales obtenidas directamente desde los sensores conectados al ESP32.



\---



\## Dashboard



La interfaz desarrollada permite representar de manera conceptual:



\- Temperatura del agua.

\- Temperatura ambiente.

\- Humedad relativa.

\- Temperatura de la cara fría de la Peltier.

\- Temperatura de la cara caliente.

\- Voltaje.

\- Corriente.

\- Potencia eléctrica.

\- Temperatura mínima registrada.

\- Gráfica de temperatura contra tiempo.

\- Historial de registros.

\- Almacenamiento local.

\- Exportación de datos en formato CSV.



\---



\## Dimensionamiento teórico



Para el análisis preliminar se consideraron las siguientes condiciones:



| Parámetro | Valor |

|---|---:|

| Volumen de agua | 250 mL |

| Masa aproximada | 0.250 kg |

| Temperatura inicial | 25 °C |

| Temperatura objetivo de cálculo | 13 °C |

| Diferencia de temperatura | 12 °C |

| Energía térmica a retirar | 12.54 kJ |

| Tiempo considerado | 600 s |

| Capacidad frigorífica ideal | 20.9 W |



\### Cálculo de energía térmica



La energía requerida para enfriar el agua se calcula mediante:



`Q = m × Cp × ΔT`



Sustituyendo:



`Q = 0.250 × 4.18 × 12`



Resultado:



`Q = 12.54 kJ`



\---



\### Capacidad frigorífica ideal



Para un tiempo de 600 segundos:



`Qc = Q / t`



Sustituyendo:



`Qc = 12 540 / 600`



Resultado:



`Qc = 20.9 W`



Este valor representa únicamente la \*\*capacidad frigorífica ideal requerida\*\*, sin considerar pérdidas térmicas.



\---



\## Primera Ley de la Termodinámica



El balance energético conceptual del sistema se expresa como:



`Qh = Qc + Win`



Donde:



\- `Qc` = calor retirado de la región fría.

\- `Win` = energía eléctrica suministrada.

\- `Qh` = calor rechazado hacia el ambiente.



Esto significa que el sistema de disipación debe eliminar tanto el calor extraído de la carga como parte de la energía eléctrica suministrada al módulo.



\---



\## Segunda Ley de la Termodinámica



El desempeño máximo teórico puede compararse con un refrigerador reversible mediante el COP de Carnot:



`COP Carnot = Tc / (Th - Tc)`



El COP real será determinado posteriormente cuando se disponga de mediciones experimentales de:



\- temperatura;

\- voltaje;

\- corriente;

\- potencia;

\- capacidad frigorífica.



\---



\## Componentes propuestos



\- Módulo termoeléctrico Peltier.

\- Bloque frío o intercambiador.

\- Pasta térmica.

\- Disipador tipo cooler de CPU.

\- Ventilador.

\- Recipiente aislado.

\- Sensores de temperatura.

\- Sensor de humedad.

\- ESP32.

\- Fuente de alimentación.

\- Dashboard web.

\- Sistema de almacenamiento de datos.



\---



\## Estructura del repositorio



&#x20;   Sistema-Gestion-Climatica-Fase1/

&#x20;   │

&#x20;   ├── index.html

&#x20;   ├── README.md

&#x20;   │

&#x20;   ├── assets/

&#x20;   │   ├── boceto\_sistema\_peltier.png

&#x20;   │   └── ciclo\_refrigeracion\_peltier.png

&#x20;   │

&#x20;   ├── data/

&#x20;   │   └── datos\_simulados.csv

&#x20;   │

&#x20;   ├── calculos/

&#x20;   │   └── README.md

&#x20;   │

&#x20;   └── docs/

&#x20;       └── README.md



\---



\## Estado actual del proyecto



\### Fase 1



\- ✅ Diseño conceptual del sistema.

\- ✅ Selección teórica del sistema de refrigeración.

\- ✅ Dimensionamiento térmico preliminar.

\- ✅ Análisis mediante Primera Ley.

\- ✅ Análisis mediante Segunda Ley.

\- ✅ Arquitectura de adquisición de datos.

\- ✅ Dashboard web.

\- ✅ Datos simulados en tiempo real.

\- ✅ Almacenamiento local.

\- ✅ Exportación CSV.



\### Desarrollo posterior



\- ⏳ Integración del ESP32.

\- ⏳ Sensores físicos.

\- ⏳ Lecturas experimentales.

\- ⏳ Control térmico real.

\- ⏳ Sustitución de datos simulados por datos reales.

\- ⏳ Aplicación final del sistema.



\---



\## Aclaración



Este repositorio corresponde al desarrollo conceptual y teórico de la \*\*Fase 1\*\*.



Los valores mostrados actualmente en el dashboard no representan mediciones experimentales. Se utilizan únicamente para demostrar el funcionamiento de la interfaz y la arquitectura propuesta para la recopilación, transmisión y almacenamiento de datos.

