# Driving-Behavior-Analysis-Dragon-Teeth
Conjunto de herramientas en Python para el procesamiento de datos cinemáticos y análisis de seguridad vial en entornos de simulación (SUMO) con señalización horizontal tipo 'Dientes de Dragón'.
# Análisis del Comportamiento del Conductor: Marcado de Dientes de Dragón

Este repositorio contiene los scripts desarrollados para la evaluación de la efectividad de la señalización horizontal (Dientes de Dragón y Rayado Logarítmico) mediante simulación de conducción.

## 🚀 Funcionalidades
- **Procesamiento Cinemático:** Conversión de salidas FCD (SUMO) a métricas de velocidad y aceleración.
- **Análisis de Seguridad:** Identificación de cambios de carril preventivos en zonas críticas de 300 metros.
- **Automatización de Datos:** Consolidación de resultados de múltiples participantes (n=31) en matrices estadísticas.
- **Visualización:** Generación de mapas de calor de trayectoria y boxplots de factores humanos.

##reposito Código python
-**scripts_procesamiento_dientes_dragon.zip** el comprimido contiene los siguientes códigos python que efectúan las funciones:
-01_analisis_individual_participantes.py	Procesa los archivos FCD (XML) de SUMO. Genera reportes individuales por participante y visualiza perfiles de velocidad y aceleración en todo el trayecto.
02_generador_tabla_resumen_grupal.py	Toma los resultados individuales y los organiza en una estructura tabular comparativa, facilitando la visualización de datos entre diferentes sujetos.
03_analisis_maniobras_cambio_carril_zona_critica.py	Identifica y cuantifica las maniobras de cambio de carril específicamente en la zona de conflicto (300m), detectando comportamientos preventivos o reactivos.
04_consolidador_metricas_finales_participantes.py	Extrae automáticamente métricas clave de celdas específicas en Excel para construir la base de datos maestra necesaria para el análisis estadístico global.
05_cuestionario.py	Analiza los datos de los formularios post-experimento, procesando variables sociodemográficas (edad, género) y la percepción subjetiva de los conductores.
06_CDF_acc.py	Genera la Función de Distribución Acumulada (CDF) para la aceleración, permitiendo comparar el comportamiento de frenado/aceleración entre los tres escenarios.
07_CDF_speed.py	Genera la Función de Distribución Acumulada (CDF) para la velocidad, utilizada para identificar percentiles de velocidad y el cumplimiento de la señalización.
-----------------------------------------------------

-**excel.zip** el comprimido contiene las hojas de excel utilizadas para el procesamiendo de gráficos.
-**imagenes.zip** el comprimido contiene las gráficas generadas de los resultados de los participantes
-**outputs.zip** contienen los resultados generados de la simulación SUMO de los participantes
## 🛠️ Requisitos
- Python 3.x
- Librerías: `pandas`, `matplotlib`, `openpyxl`, `numpy`, `xml.etree.ElementTree`
