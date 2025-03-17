# Proyecto Team Challenge: Análisis y Predicción del Churn de Clientes

Este proyecto tiene como objetivo analizar y predecir el abandono de clientes (Churn) en una empresa de telecomunicaciones, utilizando técnicas de Machine Learning.

## Estructura del proyecto:

```
├── data
│   ├── Telco_customer_churn.csv (Dataset original)
│   ├── X_train.csv (Datos de entrenamiento)
│   ├── X_test.csv (Datos de prueba)
│   ├── y_train.csv (Etiquetas entrenamiento)
│   └── y_test.csv (Etiquetas prueba)
├── models
│   ├── best_random_forest_model.joblib
│   ├── best_random_forest_model_v2.joblib
│   └── best_lightgbm_smote_model.joblib (Modelo final optimizado con LightGBM y SMOTE)
├── notebooks
│   ├── Notebook_main_challenge_pipelines.ipynb
│   └── Notebook_meine_virtuelle_Umgebung.ipynb
└── utils
    ├── requirements.txt
    └── README.md
```

## Descripción:
El análisis se inició con la limpieza y exploración de los datos, identificando variables con posible fuga de datos (leakage), que posteriormente fueron eliminadas. Se realizó la división del dataset en entrenamiento (80%) y prueba (20%).

Se aplicaron técnicas de preprocesamiento, pipelines y validación cruzada. Los modelos utilizados fueron:

- **Random Forest:** modelo inicial y versión optimizada con GridSearchCV.
- **LightGBM:** optimizado mediante SMOTE para equilibrar clases desbalanceadas.

## Mejor modelo final:
El modelo final seleccionado es **LightGBM** con aplicación de **SMOTE** para mejorar el manejo del desequilibrio entre las clases.

**Métricas del modelo final:**

| Métrica      | Valor |
|--------------|-------|
| Accuracy     | 81 %  |
| Precision clase 1 | 0.68 |
| Recall clase 1    | 0.65 |
| F1-Score clase 1  | 0.66 |

Este modelo mostró la mejor combinación de precisión y recall para identificar clientes en riesgo de abandonar.

## Uso:

- Cargar el modelo desde la carpeta `models`.
- Realizar predicciones utilizando los archivos CSV preparados en `data`.

## Instalación:
```
pip install -r utils/requirements.txt
```

## Conclusión:

El proyecto logró identificar de manera efectiva clientes con alto riesgo de churn, proporcionando una base sólida para futuras estrategias de retención.
