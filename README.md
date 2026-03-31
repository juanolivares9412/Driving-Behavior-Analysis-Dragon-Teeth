# Driving-Behavior-Analysis-Dragon-Teeth
Conjunto de herramientas en Python para el procesamiento de datos cinemáticos y análisis de seguridad vial en entornos de simulación (SUMO) con señalización horizontal tipo 'Dientes de Dragón'.
# Análisis del Comportamiento del Conductor: Marcado de Dientes de Dragón

Este repositorio contiene los scripts desarrollados para la evaluación de la efectividad de la señalización horizontal (Dientes de Dragón y Rayado Logarítmico) mediante simulación de conducción.

##  Funcionalidades
- **Procesamiento Cinemático:** Conversión de salidas FCD (SUMO) a métricas de velocidad y aceleración.
- **Análisis de Seguridad:** Identificación de cambios de carril preventivos en zonas críticas de 300 metros.
- **Automatización de Datos:** Consolidación de resultados de múltiples participantes (n=31) en matrices estadísticas.
- **Visualización:** Generación de mapas de calor de trayectoria y boxplots de factores humanos.

---

##  Scripts de Procesamiento (`scripts_procesamiento_dientes_dragon.zip`)

Esta carpeta contiene el ecosistema de herramientas en **Python** diseñadas para el procesamiento, análisis y visualización de los datos obtenidos en el simulador.

###  Descripción de Módulos

| # | Archivo | Función Principal |
| :--- | :--- | :--- |
| 01 | `01_analisis_individual_participantes.py` | Procesa archivos FCD (XML) de SUMO. Genera informes individuales y visualiza perfiles de velocidad/aceleración. |
| 02 | `02_generador_tabla_resumen_grupal.py` | Organiza resultados individuales en una estructura tabular comparativa entre sujetos. |
| 03 | `03_analisis_maniobras_cambio_carril_zona_critica.py` | Identifica y cuantifica cambios de carril en la zona de conflicto (300m). |
| 04 | `04_consolidador_metricas_finales_participantes.py` | Extrae métricas clave de Excel para construir la base de datos maestra estadística. |
| 05 | `05_cuestionario.py` | Analiza datos sociodemográficos y percepción subjetiva (post-experimento). |
| 06 | `06_CDF_acc.py` | Genera la Función de Distribución Acumulada (CDF) para el análisis de frenado/aceleración. |
| 07 | `07_CDF_speed.py` | Genera la Función de Distribución Acumulada (CDF) para identificar percentiles de velocidad. |

---

###  Flujo de Trabajo Sugerido

1. **Procesamiento Base:** Ejecutar los scripts `01` y `03` para extraer la cinemática de los vehículos desde los archivos crudos de SUMO.
2. **Consolidación:** Utilizar `02` y `04` para agrupar los resultados de todos los participantes en una sola base de datos de Excel.
3. **Análisis Estadístico y Percepción:** Emplear `05` para los datos de encuestas y `06`/`07` para generar las curvas de distribución acumulada que validan el comportamiento grupal.
-----------------------------------------------------

 |-**excel.zip** el comprimido contiene las hojas de excel utilizadas para el procesamiendo de gráficos. |
 |-**imagenes.zip** el comprimido contiene las gráficas generadas de los resultados de los participantes |
 |-**outputs.zip** contienen los resultados generados de la simulación SUMO de los participantes |
##  Requisitos
- Python 3.x
- Librerías: `pandas`, `matplotlib`, `openpyxl`, `numpy`, `xml.etree.ElementTree`
