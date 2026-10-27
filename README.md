# Analítica de datos y aprendizaje automático para la predicción de la calidad del concentrado en un proceso minero industrial

Proyecto de grado de la Especialización en Analítica de Datos, Corporación Unificada Nacional de Educación Superior (CUN).

**Autores:** Brayan Estevan Zapata Mesa, Andrea Yizeth Vasquez Moreno y Oscar David Jiménez Ruiz
**Docente:** Andrés Felipe Solis Pino

## Objetivo

Evaluar el efecto de la dosificación de reactivos y de las variables operativas sobre la calidad del concentrado (porcentaje de sílice) en un proceso industrial de flotación, mediante analítica de datos y modelos de aprendizaje automático. Metodología: CRISP-DM.

## Datos

- **Conjunto:** Quality Prediction in a Mining Process (Magalhães Oliveira, 2017).
- **Fuente:** [Kaggle](https://www.kaggle.com/datasets/edumagalhaes/quality-prediction-in-a-mining-process) · réplica en [OpenML (ID 43311)](https://www.openml.org/d/43311).
- **Licencia:** CC0 1.0 Universal (dominio público). No contiene datos personales.

Los datos crudos no se guardan en el repositorio por su tamaño: el cuaderno los descarga desde OpenML y guarda una copia con la fecha en `data/raw/`. También se puede subir el CSV de Kaggle a `data/raw/` antes de ejecutar.

## Estructura

```
├── notebooks/
│   └── 01_ETL_EDA_flotacion.ipynb     # Fase 1: adquisición, ficha, diccionario, ETL y EDA
├── data/
│   ├── raw/                           # copia de los datos con fecha de descarga (no versionada)
│   └── processed/                     # flotacion_horaria.csv para la fase de modelado
├── reports/
│   ├── figures/                       # figuras del EDA
│   ├── tables/                        # ficha, diccionario, conteos del ETL, VIF, correlaciones
│   └── resumen_fase1.json             # cifras clave de la fase 1
├── requirements.txt
└── README.md
```

## Cómo reproducir

1. Abrir `notebooks/01_ETL_EDA_flotacion.ipynb` en Google Colab.
2. Ejecutar todo: *Entorno de ejecución → Ejecutar todo*.
3. Los resultados quedan en `reports/` y el conjunto horario en `data/processed/`.

Semilla aleatoria fija: `42`.

## Versiones

| Versión | Fase | Contenido |
|---|---|---|
| v0.1 | Objetivo específico 1 | Adquisición, ficha, diccionario, ETL y EDA multivariado |
