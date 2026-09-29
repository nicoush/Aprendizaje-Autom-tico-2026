# Aprendizaje Automático

Material de apoyo para las clases del **bloque de Aprendizaje Automático**: ejemplos en Python, Jupyter notebooks, actividades y apuntes para acompañar el trabajo en clase.

## Empezá por acá

Seguí el recorrido de las clases: **inspeccionar y limpiar → preparar variables → regresión lineal y logística → KNN y árboles**. Dentro de cada clase, los notebooks están numerados en el orden de lectura sugerido.

## Índice por clase

| Clase | Tema | Materiales |
|---|---|---|
| [Clase 2](clases/02-inspeccion-y-visualizacion/README.md) | Inspección, limpieza y visualización | 4 notebooks y archivos de datos |
| [Clase 3](clases/03-preparacion-de-datos/README.md) | Preparación de datos | 1 notebook |
| [Clase 4](clases/04-regresion-lineal-y-logistica/README.md) | Regresión lineal y logística | 3 notebooks y 1 apunte de métricas |
| [Clase 5](clases/05-knn-y-arboles/README.md) | KNN y árboles de decisión | 1 notebook |

El índice reúne los materiales disponibles: **9 notebooks y 1 apunte**. La numeración conserva la de las clases; no hay materiales de Clase 1 en esta versión.

## Acceso directo a los materiales

### Clase 2 · Inspección, limpieza y visualización de datos

| Material | Contenido |
|---|---|
| [Pandas: manipulación y limpieza](clases/02-inspeccion-y-visualizacion/notebooks/01-pandas-manipulacion-y-limpieza.ipynb) | Inspección, filtros, faltantes, duplicados, tipos, outliers y agrupaciones. Incluye diez actividades al final. |
| [Inspección y visualización](clases/02-inspeccion-y-visualizacion/notebooks/02-inspeccion-y-visualizacion.ipynb) | Histogramas, boxplots, relaciones entre variables y detección de outliers con IQR. |
| [Repaso de Matplotlib y seaborn](clases/02-inspeccion-y-visualizacion/notebooks/03-repaso-matplotlib.ipynb) | Gráficos básicos y estadísticos con datos sintéticos incluidos en la carpeta datos. |
| [Lectura de archivos con Pandas](clases/02-inspeccion-y-visualizacion/notebooks/04-lectura-de-archivos-pandas.ipynb) | Ejemplos de CSV, Excel, JSON, HTML, SQLite y XML con archivos incluidos. |

### Clase 3 · Preparación de datos

| Material | Contenido |
|---|---|
| [Preparación de datos paso a paso](clases/03-preparacion-de-datos/notebooks/01-preparacion-de-datos.ipynb) | Limpieza, imputación, escalado, normalización y codificación de categorías. Cuándo usar cada función y qué precauciones tomar. |

### Clase 4 · Regresión lineal y logística

| Material | Contenido |
|---|---|
| [Regresión lineal simple y múltiple](clases/04-regresion-lineal-y-logistica/notebooks/01-regresion-lineal.ipynb) | Comparación de modelos, evaluación, gráficos y análisis con statsmodels sobre datos simulados. |
| [Regresión lineal: estatura y presión arterial](clases/04-regresion-lineal-y-logistica/notebooks/02-regresion-lineal-estatura-y-presion.ipynb) | Casos simulados de estatura padre–hijo y presión arterial; coeficientes, métricas y residuos. |
| [Regresión logística y evaluación](clases/04-regresion-lineal-y-logistica/notebooks/03-regresion-logistica-y-evaluacion.ipynb) | Clasificación binaria y multiclase con ejemplos ficticios de Titanic e intención de voto. |
| [Interpretación de métricas: Titanic e intención de voto](clases/04-regresion-lineal-y-logistica/apuntes/01-interpretacion-metricas-titanic-y-voto.md) | Apunte para interpretar exactitud, precisión, recall, F1 y referencias de clase mayoritaria. |

### Clase 5 · KNN y árboles de decisión

| Material | Contenido |
|---|---|
| [Comparación entre KNN y árboles de decisión](clases/05-knn-y-arboles/notebooks/01-comparacion-knn-y-arboles.ipynb) | Distancias, escalado, categóricas, Gini, métricas por enfermedad, valores de k y escenarios de desbalanceo. |

## Ejercicios y actividades

- **Clase 2:** diez actividades al final de [Pandas: manipulación y limpieza](clases/02-inspeccion-y-visualizacion/notebooks/01-pandas-manipulacion-y-limpieza.ipynb), con filtros, promedios, agrupaciones y nuevas columnas.
- **Clase 3:** mini práctica al final de [Preparación de datos](clases/03-preparacion-de-datos/notebooks/01-preparacion-de-datos.ipynb): modificar un valor, anticipar el resultado y explicar qué información se conserva o se pierde.
- **Clases 4 y 5:** ejemplos resueltos para ejecutar, interpretar y explorar. Las condiciones de entrega son las indicadas por el docente.

Las actividades permanecen dentro de los notebooks. No hay una carpeta separada de ejercicios ni soluciones independientes.

## Cómo usar los notebooks

### Consultar en GitHub

Abrí los enlaces del índice para leer las explicaciones, el código y las salidas guardadas. Para ejecutar y modificar código usá Jupyter o Google Colab.

### Trabajar en tu computadora

Descargá el repositorio desde **Code → Download ZIP** y descomprimilo completo. Desde la carpeta que contiene este README, instalá las dependencias y abrí JupyterLab:

```bash
python -m pip install -r requirements.txt
python -m jupyterlab
```

Abrí el notebook desde `clases/`, elegí un kernel del mismo entorno y ejecutá las celdas en orden. Trabajá con Python 3.11 o 3.12. La lista de dependencias fija versiones para conservar compatibilidad con los ejemplos existentes.

### Trabajar en Google Colab

En la opción de abrir un notebook desde GitHub, pegá la dirección del repositorio y elegí el archivo:

```text
https://github.com/nicoush/Aprendizaje-Automatico
```

Los ejemplos que generan datos dentro del notebook pueden ejecutarse sin descargar datasets. Para los notebooks **03 y 04 de Clase 2**, descargá también el repositorio completo como ZIP, subilo a Colab y descomprimilo en `/content/`. La celda inicial busca los archivos en `/content/Aprendizaje-Automatico-main/clases/02-inspeccion-y-visualizacion/datos`. Si elegís otra carpeta, ajustá esa ruta.

Si Colab utiliza versiones incompatibles con los ejemplos, instalá las del archivo `requirements.txt` y reiniciá el entorno de ejecución antes de volver a importar las bibliotecas. Guardá una copia personal del notebook para conservar tus cambios.

## Datos de las prácticas

- [Clase 2: archivos incluidos y sus formatos](clases/02-inspeccion-y-visualizacion/datos/README.md). Contiene CSV, Excel, HTML, SQLite, XML, JSON y ejemplos para visualización.
- **Clases 3, 4 y 5:** los datos se generan en el código de los notebooks.
- Los datos son sintéticos o ficticios y se utilizan para aprender. Los archivos llamados Iris, Wine y anscombe.json de Clase 2 **no son los datasets originales**.

## Organización del repositorio

| Carpeta o archivo | Función |
|---|---|
| `README.md` | Índice general y guía de uso |
| `clases/02-inspeccion-y-visualizacion/` | Notebooks y datos de Clase 2 |
| `clases/03-preparacion-de-datos/` | Notebook de Clase 3 |
| `clases/04-regresion-lineal-y-logistica/` | Notebooks y apunte de Clase 4 |
| `clases/05-knn-y-arboles/` | Notebook de Clase 5 |
| `requirements.txt` | Dependencias del entorno de trabajo |

Cada clase tiene su propio README. Los notebooks se guardan en `notebooks/`; los archivos de entrada, cuando existen, en `datos/`; y los textos complementarios en `apuntes/`.

## Para aprovechar los ejemplos

Leé la explicación antes de ejecutar, compará entradas y resultados y justificá cada decisión. Una buena métrica no reemplaza la revisión de los datos, la comparación con una referencia y el análisis de errores. Usá los materiales como punto de partida para experimentar.
