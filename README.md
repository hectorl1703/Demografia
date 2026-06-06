### Proyecto Final - Demografía II
## Autores
- Monsalvo Velázquez Naomi Adai
- López Domínguez Héctor

## Descripción del Proyecto
Este repositorio contiene el código, la fundamentación matemática y el análisis demográfico completo del estado de Veracruz de Ignacio de la Llave. El proyecto tiene como eje central estimar la esperanza de vida al nacer y analizar la evolución de la mortalidad, con especial atención al impacto demográfico y epidemiológico de la COVID-19 en 2021, integrando a su vez un estudio riguroso sobre la dinámica de la fecundidad en la región bajo un estricto orden metodológico y de organización de datos.

En cuanto al análisis de **mortalidad**, se construyeron Tablas de Vida para los años 2010, 2019 y 2021. Se incluye la versión definitiva del código en R, todas las expresiones matemáticas utilizadas, un diagrama de flujo metodológico corregido (con inicio y fin), cuadros resumidos de las esperanzas de vida al nacer por sexo/año y las tablas insertadas directamente en el reporte. Adicionalmente, se presenta el impacto actuarial de los homicidios en 2019 mediante una tabla de vida de *causa eliminada* (decrementos múltiples), evaluando gráficamente las probabilidades de muerte ($q_x$) y esperanzas de vida ($e_0$) por sexo.

En cuanto a la **fecundidad**, el trabajo documenta la demostración analítica de por qué la Tasa de Reemplazo es igual a 2.1. Asimismo, detalla el cálculo, análisis y evolución histórica (2010 vs. 2019) de las Tasas Globales de Fecundidad (TGF), Tasas Brutas de Reproducción (TBR) y Tasas Netas de Reproducción (TNR). Finalmente, incluye la modelación y graficación con títulos normativos (*captions*) de las curvas de Tasas Específicas de Fecundidad (TEF), contrastando a Veracruz con el promedio nacional de México y Mónaco.

## Estructura del Repositorio

A continuación se describe la organización de los archivos e insumos de este proyecto:

```text
├── data/                                 # Bases de datos y memorias de cálculo
│   ├── APV_2010-2019-2021.csv            # Datos limpios de Años-Persona Vividos
│   ├── Deaths_Ver_2010-2019-2021.csv     # Datos limpios de Defunciones Generales
│   ├── Medidas_Fecundidad_MexVer.xlsx    # Reporte final de medidas de fecundidad
│   ├── ProyectoFinal_avance_LópezMonsalvo (1).xlsx # Memoria de cálculo
│   └── Tabla de vida Causa eliminada.xlsx # Memoria: Causa Eliminada (Homicidios)
├── images/                               # Gráficas y diagramas exportados
│   ├── diagrama_flujo.png                # Diagrama de flujo metodológico
│   ├── grafica_ex_homicidios.png         # Comparación de Esperanza de vida (e_x)
│   ├── grafica_qx_homicidios_Mujeres.png # Probabilidades de muerte sin homicidios (Mujeres)
│   ├── grafica_qx_homicidios_hombres.png # Probabilidades de muerte sin homicidios (Hombres)
│   └── graficas_fecundidad.png           # Gráficas de fecundidad
├── output/                               # Entregables finales
│   └── Trabajo-final.pdf                 # Documento final en PDF (Versión entregada)
├── .RDataTmp                             # Archivos temporales de entorno de R
├── .gitignore                            # Archivo de exclusión de Git
├── Demografia.Rproj                      # Archivo de entorno de RStudio
└── README.md                             # Documentación principal del repositorio
```
## Contexto del Estudio
Veracruz es el 11° estado con mayor superficie en México. Entre los hallazgos demográficos clave analizados en este proyecto destacan:
* Un crecimiento poblacional del 5.49% entre 2010 y 2020 (llegando a 8,062,579 habitantes). Sin embargo, se prevén tasas de crecimiento negativo para años futuros
* Factores migratorios internos movilizados por la pobreza marginal (norte a sur).
* Una estructura de mortalidad dominada por enfermedades del corazón, tumores malignos y diabetes (tasa bruta de 130.8 por cada 100,000 habitantes, muy por encima de la media nacional).

## Metodología y Flujo de Trabajo
El procesamiento de los datos siguió un rigor metodológico estructurado en las siguientes etapas:

1. **Obtención de Datos:** Extracción de microdatos oficiales del INEGI correspondientes al Censo de Población y Vivienda (CPV) 2010 y 2020, y a las Estadísticas de Defunciones Registradas (EDR).
2. **Preprocesamiento:** Agrupación de la población en intervalos de edad estándar (0 años, 1 a 4 años, y grupos quinquenales hasta el grupo abierto de 85 y más).
3. **Prorrateo:** Redistribución proporcional de los registros con edades y sexos "no especificados" en cada año para evitar subestimaciones en la mortalidad.
4. **Estimación de Años Persona Vividos (APV):** Se calculó usando tasas de crecimiento exponencial intercensal (r) y fracciones de tiempo a proyectar.
5. **Construcción de Tablas de Vida Base:** Cálculo de tasas centrales de mortalidad (mx), probabilidades de fallecer (qx), sobrevivientes (lx), años-persona vividos (Lx) y esperanza de vida al nacer (ex).
6. **Decrementos Múltiples (Causa Eliminada):** Aplicación de la metodología de Chiang para aislar y "eliminar" el riesgo de morir por homicidios en 2019, calculando nuevas probabilidades de supervivencia y esperanzas de vida teóricas.

## Herramientas y Requisitos
El análisis computacional de las tablas de vida se programó en **R** y **Quarto**.
Las librerías principales requeridas para ejecutar los scripts `.qmd` son:
* `data.table`: Para el manejo eficiente, lectura y procesamiento de los microdatos.
* `knitr` y `kableExtra`: Para la renderización y estilización avanzada de las tablas de vida en los reportes finales.

