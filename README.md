# Construcción de Tablas de Vida y Análisis de Indicadores de Fecundidad: Veracruz (2010, 2019, 2021)

### Proyecto Final - Demografía II
**Autores:** * Naomi Adai Monsalvo Velázquez
* Héctor López Domínguez

---

## Descripción del Proyecto
Este repositorio contiene la memoria de cálculo, los scripts de automatización y el informe actuarial definitivo en PDF sobre la evolución demográfica del estado de **Veracruz de Ignacio de la Llave** para los años **2010, 2019 y 2021**. 

El proyecto está diseñado bajo los más estrictos criterios de **reproducibilidad y transparencia metodológica**, permitiendo al cliente comprender a detalle la transición epidemiológica (incluyendo el impacto de la pandemia de COVID-19), el modelado de decrementos múltiples por causas exógenas (homicidios) y el comportamiento histórico de la fecundidad en la región comparada con el contexto nacional e internacional.

---

## Estructura del Repositorio

El proyecto se encuentra organizado de acuerdo con las mejores prácticas de gestión de código y reproducibilidad:

```text
├── data/                                 # Datos crudos y memorias de cálculo en Excel
│   ├── ProyectoFinal_avance_LópezMonsalvo.xlsx  # Memoria definitiva: Prorrateos, APV y Tasas Mx
│   ├── Homicidios_ver.xlsx               # Memoria definitiva: Causa eliminada (Homicidios 2019)
│   ├── APV_2010-2019-2021.csv            # Datos limpios de Años-Persona Vividos
│   └── Deaths_Ver_2010-2019-2021.csv     # Datos limpios de Defunciones Generales
├── script/                               # Código fuente de automatización
│   └── Reporte_Final_Demografia.qmd      # Archivo fuente en Quarto (.qmd) que genera el PDF
├── images/                               # Gráficas y diagramas exportados
│   ├── diagrama_flujo_tablas_vida.png    # Diagrama de flujo corregido (Inicio/Fin con óvalos)
│   ├── grafica_qx_homicidios_hombres.png # Probabilidades de muerte sin homicidios (Hombres)
│   ├── grafica_qx_homicidios_mujeres.png # Probabilidades de muerte sin homicidios (Mujeres)
│   ├── grafica_ex_homicidios.png         # Comparación de Esperanza de vida con causa eliminada
│   └── curvas_tefe_2019.png              # Curvas de Tasas Específicas de Fecundidad comparadas
├── output/                               # Entregables finales para el cliente
│   └── Reporte_Final_Demografia.pdf      # Informe actuarial definitivo compilado

## Metodología y Alcance del Informe

El informe final consolidado en `output/Reporte_Final_Demografia.pdf` cubre los siguientes cinco ejes fundamentales requeridos:

### a) Tablas de Vida Definitivas e Inclusión de Observaciones
* **Flujo Metodológico:** Incorporación de un diagrama de flujo corregido utilizando la notación geométrica estándar (óvalos para Inicio/Fin, rectángulos para procesos de cálculo de $m_x, q_x, l_x, d_x, L_x, T_x, e_x$).
* **Modelado Matemático y Código:** Documentación explícita de todas las fórmulas de crecimiento exponencial intercensal, prorrateo multiplicativo y relaciones actuariales de la tabla de vida, junto con el código definitivo en R para su total replicabilidad.
* **Resultados Integrados:** Inclusión de las tablas de vida completas dentro del texto y un cuadro resumen con las esperanzas de vida al nacer ($e_0$) por sexo para analizar el severo choque exógeno de la pandemia de COVID-19 en 2021.

### b) Tabla de Vida de Causa Eliminada (Homicidios 2019)
* Modelado a través de decrementos múltiples en donde se aísla el impacto de la violencia en Veracruz para el año 2019.
* El archivo dinámico interactivo con las fórmulas vivas se localiza en `data/Homicidios_ver.xlsx`. El informe PDF despliega exclusivamente el análisis demográfico profundo apoyado por las tres gráficas de la carpeta `images/` que contrastan el comportamiento de las curvas de mortalidad por sexo a escala logarítmica.

### c) Demostración Matemática del Reemplazo Poblacional
* Documentación formal y desarrollo algebraico de la demostración analítica que fundamenta por qué la **Tasa de Reemplazo Estándar es igual a 2.1** bajo condiciones demográficas contemporáneas (considerando la razón de masculinidad al nacer y las probabilidades de supervivencia materna).

### d) Evolución de Indicadores de Fecundidad (2010 vs. 2019)
* Estimación y análisis comparativo para Veracruz de los siguientes indicadores macro-demográficos:
  * **TGF:** Tasa Global de Fecundidad (número promedio de hijos por mujer).
  * **TBR:** Tasa Bruta de Reproducción (promedio de hijas nacidas por mujer).
  * **TNR:** Tasa Neta de Reproducción (hijas promedio que sobrevivirán hasta la edad reproductiva de la madre).

### e) Análisis Comparativo Internacional de las TEFE (2019)
* Graficación y análisis de las **Tasas Específicas de Fecundidad (TEFE)** por grupos quinquenales de edad para el año 2019, contrastando de forma simultánea la estructura de la fecundidad de:
  1. El estado de **Veracruz**.
  2. El contexto nacional (**México**).
  3. El país seleccionado para la comparación internacional.
└── README.md                             # Portada de presentación del repositorio

de la fecundidad de:El estado de Veracruz.El contexto nacional (México).El país seleccionado para la comparación internacional.
