# Telecom X – Parte 2: Predicción de Churn

## Propósito del proyecto

El objetivo de este proyecto es analizar el comportamiento de los clientes de Telecom X y predecir la cancelación del servicio (churn) utilizando técnicas de machine learning.

A partir de variables relacionadas con los clientes, como el tiempo de permanencia, el tipo de contrato y los cargos mensuales, se busca identificar qué factores influyen en la cancelación y construir modelos que permitan anticipar estos casos.

---

## Estructura del proyecto

El proyecto está organizado de la siguiente manera:

Telecom_X_2/
│
├── Telecom_X_2.ipynb      # Cuaderno principal con todo el análisis
├── datos_tratados.csv     # Dataset limpio y preparado para el análisis
├── graficas/              # Visualizaciones generadas durante el análisis
└── README.md              # Documentación del proyecto

El cuaderno principal contiene todo el flujo del proyecto, desde la exploración de los datos hasta la construcción y evaluación de modelos predictivos.

---

## Preparación de los datos

Antes de construir los modelos se realizó un proceso de preparación de los datos.

### Clasificación de variables

Variables categóricas:
- gender
- contract
- internet_service
- payment_method

Variables numéricas:
- tenure
- monthly_charges
- total_charges

### Codificación de variables

Las variables categóricas fueron transformadas a formato numérico utilizando codificación (get_dummies) para que pudieran ser utilizadas por los modelos de machine learning.

### División de los datos

El dataset fue dividido en:

- 80% datos de entrenamiento
- 20% datos de prueba

Esto permite entrenar los modelos con una parte de los datos y evaluar su desempeño con información que el modelo no ha visto antes.

---

## Modelos utilizados

Se entrenaron dos modelos de clasificación:

Árbol de Decisión  
Modelo simple basado en reglas que permite interpretar fácilmente cómo se toman las decisiones.

Random Forest  
Modelo basado en múltiples árboles de decisión que ayuda a reducir el riesgo de sobreajuste y mejorar la capacidad de generalización.

Al comparar los resultados, Random Forest mostró un mejor desempeño general en métricas como accuracy, precision, recall y F1-score.

---

## Análisis exploratorio de datos (EDA)

Durante el análisis exploratorio se identificaron algunos patrones importantes:

- Los clientes con menor tiempo en el servicio (tenure) presentan mayor probabilidad de cancelar.
- Los clientes con contratos más largos tienden a permanecer más tiempo.
- Existe una relación entre mayor gasto acumulado y mayor permanencia.

Se generaron visualizaciones como:

- Matriz de correlación
- Boxplots entre churn y variables numéricas
- Gráficas de dispersión
- Gráficas de importancia de variables

Estas visualizaciones ayudaron a entender mejor el comportamiento de los clientes.

---

## Variables más importantes

A partir del modelo Random Forest se identificaron las variables con mayor impacto en la predicción de churn.

Entre las más relevantes se encuentran:

- tenure
- monthly_charges
- contract
- total_charges

Estas variables tienen mayor influencia en la probabilidad de cancelación del cliente.

---

## Cómo ejecutar el proyecto

Para ejecutar el proyecto se recomienda utilizar Google Colab o Jupyter Notebook.

1. Instalar las bibliotecas necesarias:

pip install pandas
pip install numpy
pip install matplotlib
pip install seaborn
pip install scikit-learn

2. Abrir el cuaderno:

Telecom_X_2.ipynb

3. Asegurarse de que el archivo de datos esté en la misma carpeta:

datos_tratados.csv

---

## Conclusión

Este análisis permitió identificar variables clave relacionadas con la cancelación de clientes y construir modelos que ayudan a predecir el churn.

Los resultados muestran que factores como el tiempo de permanencia, el tipo de contrato y los cargos mensuales influyen significativamente en la probabilidad de cancelación.

Este tipo de análisis puede servir como apoyo para desarrollar estrategias que ayuden a mejorar la retención de clientes.
