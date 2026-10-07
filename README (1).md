# Aprendizaje Automático · 2026

Material de apoyo para las clases del **bloque de Aprendizaje Automático**: ejemplos en Python, Jupyter notebooks, actividades y apuntes para acompañar el trabajo en clase.

## Empezá por acá

Seguí el recorrido de las clases: **inspeccionar y limpiar → preparar variables → regresión lineal y logística → KNN y árboles → máquinas de vectores de soporte (SVM)**. Dentro de cada clase, los notebooks están numerados en el orden de lectura sugerido.

## Índice por clase

| Clase | Tema | Materiales |
|---|---|---|
| [Clase 2](clases/02-inspeccion-y-visualizacion/README.md) | Inspección, limpieza y visualización | 4 notebooks y archivos de datos |
| [Clase 3](clases/03-preparacion-de-datos/README.md) | Preparación de datos | 1 notebook |
| [Clase 4](clases/04-regresion-lineal-y-logistica/README.md) | Regresión lineal y logística | 3 notebooks y 1 apunte de métricas |
| [Clase 5](clases/05-knn-y-arboles/README.md) | KNN y árboles de decisión | 1 notebook |
| [Clase 6](clases/06-SMV/) | Máquinas de vectores de soporte (SVM) | 2 notebooks y 1 dataset |

El índice reúne los materiales disponibles: **11 notebooks y 1 apunte**, además de los archivos de datos. La numeración conserva la de las clases; no hay materiales de Clase 1 en esta versión.

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

### Clase 6 · Máquinas de vectores de soporte (SVM)

| Material | Contenido |
|---|---|
| [SVM lineal y no lineal](clases/06-SMV/notebooks/Ejemplo_SVM_Lineal_NoLineal.ipynb) | Ejemplos con datos sintéticos, kernel lineal y RBF, parámetros C y gamma, métricas y gráficos de las fronteras de decisión. |
| [SVM con UniversalBank](clases/06-SMV/notebooks/UniversalBank_CreditCard_SVM_.ipynb) | Exploración, preparación y escalado de datos; comparación de kernels lineal, RBF, polinómico y sigmoide para predecir la variable CreditCard. Incluye métricas y visualizaciones en dos dimensiones con PCA. |
| [Dataset UniversalBank.csv](clases/06-SMV/dataset/UniversalBank.csv) | Archivo de entrada para el ejemplo bancario. Consultá las instrucciones de carga más abajo. |

**Orden sugerido:** comenzá por el ejemplo lineal y no lineal; después trabajá con UniversalBank para comparar kernels y analizar los errores de clasificación.

## Ejercicios y actividades

- **Clase 2:** diez actividades al final de [Pandas: manipulación y limpieza](clases/02-inspeccion-y-visualizacion/notebooks/01-pandas-manipulacion-y-limpieza.ipynb), con filtros, promedios, agrupaciones y nuevas columnas.
- **Clase 3:** mini práctica al final de [Preparación de datos](clases/03-preparacion-de-datos/notebooks/01-preparacion-de-datos.ipynb): modificar un valor, anticipar el resultado y explicar qué información se conserva o se pierde.
- **Clases 4, 5 y 6:** ejemplos resueltos para ejecutar, interpretar y explorar. Las condiciones de entrega son las indicadas por el docente.

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
https://github.com/nicoush/Aprendizaje-Autom-tico-2026
```

Los ejemplos que generan datos dentro del notebook pueden ejecutarse sin descargar datasets. Los notebooks de lectura de archivos y algunos de visualización necesitan los archivos indicados a continuación.

Guardá una copia personal del notebook. Si Colab utiliza versiones incompatibles con el código, consultá [requirements.txt](requirements.txt), instalá las versiones correspondientes y reiniciá el entorno antes de volver a importar las bibliotecas.

### Cargar los datos de Clase 2

Los notebooks **03 y 04 de Clase 2** utilizan la carpeta `clases/02-inspeccion-y-visualizacion/datos/`.

- **En tu computadora:** descargá el repositorio completo y ejecutá el notebook desde su carpeta o desde la raíz del repositorio; la celda inicial busca las rutas locales.
- **En Colab:** descargá el ZIP del repositorio, subilo y descomprimilo en `/content/`. Al usar este repositorio, la carpeta suele llamarse `Aprendizaje-Autom-tico-2026-main`. La celda inicial conserva una ruta con el nombre anterior del repositorio: reemplazá esa ruta por la ubicación real de la carpeta de datos.

Por ejemplo, en la lista `carpetas` de esa celda, la ruta de Colab debe ser:

```python
Path("/content/Aprendizaje-Autom-tico-2026-main/clases/02-inspeccion-y-visualizacion/datos")
```

### Cargar UniversalBank en Clase 6

El notebook bancario contiene esta lectura:

```python
df = pd.read_csv("UniversalBank.csv")
```

Por eso, el CSV debe estar en el directorio desde el que se ejecuta el código, o debe indicarse su ruta:

- **En Colab:** descargá [UniversalBank.csv](clases/06-SMV/dataset/UniversalBank.csv) y subilo al panel de archivos de la sesión. Si queda en `/content/`, la lectura original funciona desde ese directorio.
- **En Jupyter, ejecutando desde la carpeta del notebook:** reemplazá la lectura por:

```python
df = pd.read_csv("../dataset/UniversalBank.csv")
```

- **Ejecutando desde la raíz del repositorio:** usá:

```python
df = pd.read_csv("clases/06-SMV/dataset/UniversalBank.csv")
```

Abrir el notebook desde GitHub en Colab no descarga automáticamente los archivos de datos.

## Datos de las prácticas

- [Clase 2: archivos incluidos y sus formatos](clases/02-inspeccion-y-visualizacion/datos/README.md). Contiene CSV, Excel, HTML, SQLite, XML, JSON y ejemplos para visualización.
- **Clases 3, 4 y 5:** los datos se generan en el código de los notebooks.
- **Clase 6:** el ejemplo lineal/no lineal genera datos sintéticos; el ejemplo bancario utiliza [UniversalBank.csv](clases/06-SMV/dataset/UniversalBank.csv).
- Los archivos llamados Iris, Wine y anscombe.json de Clase 2 son sintéticos y **no son los datasets originales**. Los demás ejemplos que generan datos ficticios lo indican dentro del notebook.

## Organización del repositorio

| Carpeta o archivo | Función |
|---|---|
| `README.md` | Índice general y guía de uso |
| `clases/02-inspeccion-y-visualizacion/` | Notebooks y datos de Clase 2 |
| `clases/03-preparacion-de-datos/` | Notebook de Clase 3 |
| `clases/04-regresion-lineal-y-logistica/` | Notebooks y apunte de Clase 4 |
| `clases/05-knn-y-arboles/` | Notebook de Clase 5 |
| `clases/06-SMV/` | Notebooks SVM y dataset UniversalBank de Clase 6 |
| `requirements.txt` | Dependencias del entorno de trabajo |

Las clases 2 a 5 tienen su propio README; la Clase 6 se encuentra enlazada directamente a su carpeta. Los notebooks se guardan en `notebooks/`; los archivos de entrada están en `datos/` para Clase 2 y en `dataset/` para Clase 6; los textos complementarios se guardan en `apuntes/`.

La carpeta de Clase 6 conserva el nombre publicado `06-SMV`; el tema y la sigla utilizados en el contenido son **SVM**.

## Para aprovechar los ejemplos

Leé la explicación antes de ejecutar, compará entradas y resultados y justificá cada decisión. Una buena métrica no reemplaza la revisión de los datos, la comparación con una referencia y el análisis de errores. Usá los materiales como punto de partida para experimentar.

