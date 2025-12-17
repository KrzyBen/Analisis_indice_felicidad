# Analisis_indice_felicidad
# Mental Health and Social Media Balance – Machine Learning Project

Este repositorio contiene un proyecto de Machine Learning y Deep Learning orientado a la clasificación de niveles de felicidad a partir de hábitos digitales y factores asociados a la salud mental. El sistema utiliza una red neuronal artificial entrenada sobre el *Mental Health and Social Media Balance Dataset* y se ejecuta dentro de un entorno contenedorizado mediante Docker.

---

## Tabla de Contenidos

- [Descripción](#descripción)
- [Dataset](#dataset)
- [Tecnologías](#tecnologías)
- [Características del Proyecto](#características-del-proyecto)
- [Estructura del Repositorio](#estructura-del-repositorio)
- [Instalación](#instalación)
- [Uso](#uso)
- [Evaluación del Modelo](#evaluación-del-modelo)
- [Conclusión](#conclusión)
- [Agradecimientos](#agradecimientos)
- [Licencia](#licencia)

---

## Descripción

El aumento del uso de redes sociales ha generado un creciente interés por comprender su impacto en la salud mental y el bienestar subjetivo. Este proyecto aborda dicha problemática mediante la construcción de un modelo de clasificación multiclase que predice niveles de felicidad (baja, media y alta) a partir de variables relacionadas con hábitos digitales, estrés, calidad del sueño y actividad física.

El flujo completo del proyecto —preprocesamiento de datos, entrenamiento del modelo, evaluación y visualización de resultados— se ejecuta dentro de un contenedor Docker, lo que garantiza reproducibilidad, portabilidad y facilidad de ejecución en distintos sistemas operativos.

---

## Dataset

El dataset utilizado en este proyecto es **Mental Health and Social Media Balance Dataset**, disponible públicamente en Kaggle.

Variables principales:
- Edad
- Género
- Tiempo diario en pantalla
- Calidad del sueño
- Nivel de estrés
- Días sin redes sociales
- Frecuencia de ejercicio
- Plataforma de redes sociales
- Happiness Index (1–10)

El dataset **no se incluye en este repositorio**, ya que no es de autoría propia.

### Descarga y preparación del dataset

1. Descargar el dataset desde Kaggle:

https://www.kaggle.com/datasets/prince7489/mental-health-and-social-media-balance-dataset

2. Colocar el archivo descargado dentro de la carpeta `data/`.

3. Extraer el archivo `.csv` y asegurarse de que quede directamente al dentro de la carpeta `data/`.


---

## Tecnologías

- Python 3.8 o superior
- Docker
- Docker Compose
- Jupyter Notebook
- TensorFlow / Keras
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## Características del Proyecto

- Preprocesamiento de datos tabulares (codificación de variables categóricas y normalización).
- Transformación del índice de felicidad en tres clases para clasificación multiclase.
- Implementación de una red neuronal artificial con capas densas y Dropout.
- Entrenamiento y evaluación del modelo mediante métricas estándar.
- Visualización de resultados y curvas de entrenamiento.
- Integración con TensorBoard.
- Ejecución reproducible mediante Docker.

---

## Estructura del Repositorio
```text
.
├── data/
├── logs/
│ └── fit/
├── notebooks/
│ └── proyecto_ml.ipynb
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
├── LICENSE
└── README.md
```
---

## Instalación

### Requisitos

- Docker Desktop o Docker Engine
- Docker Compose
- Sistema operativo compatible (Windows, macOS o Linux)
- Navegador web moderno

El contenedor se construye sobre una **imagen base de Ubuntu** (a través de una imagen oficial de Jupyter), la cual incluye Python y las herramientas necesarias para ejecutar el proyecto. Todas las dependencias del proyecto se instalan automáticamente dentro del contenedor, por lo que no es necesario realizar instalaciones manuales de librerías en el sistema anfitrión.

---

## Uso

### Construcción del contenedor (solo la primera vez o tras cambios)

En máquinas donde el contenedor aún no ha sido construido, ejecutar:

docker compose build

Este comando descarga la imagen base de Ubuntu y construye la imagen del proyecto con todas sus dependencias.

### Ejecución del proyecto

Una vez construida la imagen, iniciar el contenedor con:

docker compose up

### Acceso al entorno

Abrir un navegador web y acceder a:

Jupyter notebook local: http://localhost:8888
Tensorboard: http://localhost:6006

Desde la interfaz de Jupyter Notebook, abrir el archivo ubicado en `notebooks/proyecto_ml.ipynb` y ejecutar las celdas en orden.

---

## Evaluación del Modelo

El modelo se evalúa utilizando un conjunto de prueba independiente. Las métricas empleadas incluyen:

- Accuracy
- Curvas de pérdida y precisión
- Matriz de confusión

Estas métricas permiten analizar el desempeño del modelo y su capacidad para clasificar correctamente los distintos niveles de felicidad.

---

## Conclusión

Este proyecto demuestra la viabilidad de aplicar técnicas de Machine Learning y Deep Learning para analizar la relación entre hábitos digitales y bienestar subjetivo. A pesar del tamaño limitado del dataset, el modelo logra identificar patrones relevantes entre variables asociadas a la salud mental.

Como trabajo futuro, se propone ampliar el conjunto de datos, explorar modelos alternativos y aplicar técnicas de interpretabilidad para comprender mejor la influencia de cada característica.

---

## Agradecimientos

Se agradece a los autores del *Mental Health and Social Media Balance Dataset* por disponibilizar públicamente el conjunto de datos utilizado en este proyecto con fines académicos.

---

## Licencia

Este proyecto se distribuye bajo la licencia MIT. Para más información, consultar el archivo `LICENSE`.
