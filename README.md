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
└── README.md                             # Portada de presentación del repositorio
