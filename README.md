# \# Sistema de Gestión Climática Inteligente — Fase 1

# 

# Proyecto enfocado en el diseño teórico de un sistema de refrigeración termoeléctrico capaz de producir temperaturas subambiente, monitorear variables climáticas y plantear una arquitectura para la transmisión y almacenamiento de datos en tiempo real.

# 

# \## 🌐 Dashboard de monitoreo

# 

# Puedes visualizar la interfaz propuesta para la Fase 1 en el siguiente enlace:

# 

# \### 👉 \[Abrir Dashboard de Gestión Climática](https://emikuchaw.github.io/Sistema-Gestion-Climatica-Fase1/)

# 

# > \*\*Nota:\*\* actualmente el dashboard trabaja con datos simulados utilizados únicamente para demostrar el funcionamiento conceptual del sistema de adquisición, transmisión, visualización y almacenamiento de información.

# 

# \---

# 

# \## Objetivo de la Fase 1

# 

# Diseñar teóricamente un sistema de refrigeración capaz de disminuir la temperatura de una carga por debajo de la temperatura ambiente e integrar conceptualmente:

# 

# \- Sensores de temperatura.

# \- Sensor de humedad relativa.

# \- Adquisición de datos.

# \- Transmisión de información en tiempo real.

# \- Almacenamiento de mediciones.

# \- Visualización mediante una interfaz web.

# \- Análisis mediante la Primera y Segunda Ley de la Termodinámica.

# 

# \---

# 

# \## Sistema de refrigeración propuesto

# 

# Se propone utilizar un sistema de refrigeración termoeléctrico mediante un \*\*módulo Peltier\*\*.

# 

# La arquitectura térmica propuesta es:

# 

# Carga térmica / agua  

# ↓  

# Bloque frío o intercambiador  

# ↓  

# Módulo Peltier  

# ↓  

# Disipador tipo cooler de CPU  

# ↓  

# Ventilador  

# ↓  

# Ambiente

# 

# El módulo Peltier transporta calor desde la cara fría hacia la cara caliente utilizando energía eléctrica.

# 

# \---

# 

# \## Arquitectura de adquisición de datos

# 

# La arquitectura propuesta para futuras mediciones reales es:

# 

# Sensores  

# ↓  

# ESP32  

# ↓  

# Wi-Fi  

# ↓  

# Dashboard web  

# ↓  

# Almacenamiento de datos

# 

# Durante esta fase, los valores utilizados en el dashboard son simulados.

# 

# En una implementación física posterior, la simulación podrá sustituirse por datos obtenidos directamente desde los sensores conectados al ESP32.

# 

# \---

# 

# \## Dashboard

# 

# El dashboard desarrollado permite representar de manera conceptual:

# 

# \- Temperatura del agua.

# \- Temperatura ambiente.

# \- Humedad relativa.

# \- Temperatura de la cara fría de la Peltier.

# \- Temperatura de la cara caliente.

# \- Voltaje.

# \- Corriente.

# \- Potencia eléctrica.

# \- Temperatura mínima registrada.

# \- Gráfica de temperatura contra tiempo.

# \- Historial de registros.

# \- Almacenamiento local.

# \- Exportación de datos en formato CSV.

# 

# \---

# 

# \## Dimensionamiento teórico

# 

# Para el análisis preliminar se consideraron:

# 

# | Parámetro | Valor |

# |---|---:|

# | Volumen de agua | 250 mL |

# | Masa aproximada | 0.250 kg |

# | Temperatura inicial | 25 °C |

# | Temperatura objetivo de cálculo | 13 °C |

# | Diferencia de temperatura | 12 °C |

# | Energía térmica a retirar | 12.54 kJ |

# | Tiempo considerado | 600 s |

# | Capacidad frigorífica ideal | 20.9 W |

# 

# La energía térmica se calculó mediante:

# 

# Q = m · Cp · ΔT

# 

# obteniéndose:

# 

# Q = 12.54 kJ

# 

# Para un tiempo de 600 segundos:

# 

# Qc = Q / t

# 

# Qc = 20.9 W

# 

# Estos valores corresponden únicamente al \*\*dimensionamiento teórico preliminar de la Fase 1\*\*.

# 

# \---

# 

# \## Primera Ley de la Termodinámica

# 

# El balance energético conceptual del sistema se expresa como:

# 

# Qh = Qc + Win

# 

# donde:

# 

# \- \*\*Qc:\*\* calor retirado de la región fría.

# \- \*\*Win:\*\* energía eléctrica suministrada.

# \- \*\*Qh:\*\* calor rechazado hacia el ambiente.

# 

# \---

# 

# \## Segunda Ley de la Termodinámica

# 

# El desempeño ideal del sistema puede compararse posteriormente mediante el coeficiente de desempeño de Carnot:

# 

# COP = Tc / (Th - Tc)

# 

# El COP experimental será determinado cuando se disponga de mediciones reales de temperatura, voltaje, corriente y capacidad frigorífica.

# 

# \---

# 

# \## Estructura del repositorio

# 

# ```text

# Sistema-Gestion-Climatica-Fase1/

# │

# ├── index.html

# ├── README.md

# │

# ├── assets/

# │   ├── boceto\_sistema\_peltier.png

# │   └── ciclo\_refrigeracion\_peltier.png

# │

# ├── data/

# │   └── datos\_simulados.csv

# │

# ├── calculos/

# │   └── README.md

# │

# └── docs/

# &#x20;   └── README.md

