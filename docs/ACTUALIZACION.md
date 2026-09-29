# Guía para actualizar el repositorio

Paquete preparado el 29 de septiembre de 2026 a partir de `main`, commit `4d08c69de121d4a84f81140db67e8a686ff6c8e3`.

## Contenido

- Nueve notebooks organizados en las clases 2, 3, 4 y 5.
- README general y un índice por clase.
- Diez archivos de datos existentes y su documentación, conservados sin cambios.
- Apunte de interpretación de métricas de Titanic e intención de voto.
- Archivo de dependencias y exclusiones de archivos temporales.

## Subir desde la web de GitHub

1. Descargá una copia del repositorio actual como respaldo y descomprimí este ZIP en una carpeta aparte.
2. En la raíz de `nicoush/Aprendizaje-Automatico`, usá **Add file → Upload files**. Arrastrá el contenido descomprimido: `README.md`, `requirements.txt`, `.gitignore`, `clases/` y `docs/`. No subas el ZIP ni una carpeta externa que envuelva esos elementos.
3. Confirmá la carga y comprobá que los enlaces del nuevo README abran las clases y sus notebooks.
4. Retirá las cuatro carpetas antiguas de la raíz para evitar duplicados: `02-inspeccion-y-visualizacion`, `03-preparacion-de-datos`, `04-regresiónLinealyLogística` y `05-KNNyArboles`. Los materiales que contenían ya están en `clases/`. Si agregaste nuevos archivos después del commit de referencia, trasladalos primero a la clase correspondiente.

**Subir archivos no elimina las rutas antiguas automáticamente.** Los enlaces viejos compartidos en Moodle u otros espacios deben actualizarse con las rutas de la tabla siguiente.

## Si trabajás con Git en tu computadora

Sobre una copia actualizada del repositorio, copiá el contenido de este paquete a la raíz, retirando las cuatro carpetas antiguas una vez verificado el traslado. Conservá la carpeta `.git` de tu copia. Revisá los cambios con `git status` y `git diff` antes de hacer el commit y el push.

## Cambios de contenido

Se conservaron íntegramente ocho notebooks, los archivos de datos y el apunte. En el notebook de estatura y presión se retiró la línea incompleta `"nombre": nombre`: tenía un error de sintaxis y refería una variable no definida. Se mantienen Edad, Peso, Ejercicio y Presion, que son las variables utilizadas en el ejemplo. No se reemplazaron las salidas guardadas de los notebooks.

La lista de dependencias fija el entorno utilizado para las comprobaciones, incluido scikit-learn 1.7.2 para conservar el uso de `multi_class` en el ejemplo de regresión logística. El README y los índices se reescribieron con las rutas nuevas. No se agregaron ejercicios ni modelos nuevos.

## Comprobaciones

- Inventario completo: los 24 archivos originales tienen un destino y ninguno se omitió.
- Nueve notebooks: celdas de código ejecutadas secuencialmente en espacios de variables independientes y una copia temporal; sin errores en el entorno indicado en requirements.txt.
- Ejecución mediante Python y Matplotlib sin interfaz; no se probó la interfaz de Colab o JupyterLab ni se hizo una auditoría pedagógica de las métricas.
- Enlaces relativos de Markdown verificados contra el contenido del paquete.
- Datos conservados byte por byte.

## Tabla de rutas

| Ruta anterior | Ruta nueva |
|---|---|
| `02-inspeccion-y-visualizacion/README.md` | `clases/02-inspeccion-y-visualizacion/README.md` |
| `02-inspeccion-y-visualizacion/datos/README.md` | `clases/02-inspeccion-y-visualizacion/datos/README.md` |
| `02-inspeccion-y-visualizacion/datos/anscombe.json` | `clases/02-inspeccion-y-visualizacion/datos/anscombe.json` |
| `02-inspeccion-y-visualizacion/datos/datos.csv` | `clases/02-inspeccion-y-visualizacion/datos/datos.csv` |
| `02-inspeccion-y-visualizacion/datos/datos.xml` | `clases/02-inspeccion-y-visualizacion/datos/datos.xml` |
| `02-inspeccion-y-visualizacion/datos/empleados.csv` | `clases/02-inspeccion-y-visualizacion/datos/empleados.csv` |
| `02-inspeccion-y-visualizacion/datos/empleados.db` | `clases/02-inspeccion-y-visualizacion/datos/empleados.db` |
| `02-inspeccion-y-visualizacion/datos/empleados.html` | `clases/02-inspeccion-y-visualizacion/datos/empleados.html` |
| `02-inspeccion-y-visualizacion/datos/empleados.xlsx` | `clases/02-inspeccion-y-visualizacion/datos/empleados.xlsx` |
| `02-inspeccion-y-visualizacion/datos/iris.csv` | `clases/02-inspeccion-y-visualizacion/datos/iris.csv` |
| `02-inspeccion-y-visualizacion/datos/wine.data` | `clases/02-inspeccion-y-visualizacion/datos/wine.data` |
| `02-inspeccion-y-visualizacion/datos/wine.names` | `clases/02-inspeccion-y-visualizacion/datos/wine.names` |
| `02-inspeccion-y-visualizacion/notebooks/01-pandas-manipulacion-y-limpieza.ipynb` | `clases/02-inspeccion-y-visualizacion/notebooks/01-pandas-manipulacion-y-limpieza.ipynb` |
| `02-inspeccion-y-visualizacion/notebooks/02-inspeccion-y-visualizacion.ipynb` | `clases/02-inspeccion-y-visualizacion/notebooks/02-inspeccion-y-visualizacion.ipynb` |
| `02-inspeccion-y-visualizacion/notebooks/03-repaso-matplotlib.ipynb` | `clases/02-inspeccion-y-visualizacion/notebooks/03-repaso-matplotlib.ipynb` |
| `02-inspeccion-y-visualizacion/notebooks/04-lectura-de-archivos-pandas.ipynb` | `clases/02-inspeccion-y-visualizacion/notebooks/04-lectura-de-archivos-pandas.ipynb` |
| `03-preparacion-de-datos/Clase3_Preparacion_de_Datos.ipynb` | `clases/03-preparacion-de-datos/notebooks/01-preparacion-de-datos.ipynb` |
| `03-preparacion-de-datos/README.md` | `clases/03-preparacion-de-datos/README.md` |
| `04-regresiónLinealyLogística/Interpretacion_metricas_Titanic_Intencion_de_voto.md` | `clases/04-regresion-lineal-y-logistica/apuntes/01-interpretacion-metricas-titanic-y-voto.md` |
| `04-regresiónLinealyLogística/regresion_lineal.ipynb` | `clases/04-regresion-lineal-y-logistica/notebooks/01-regresion-lineal.ipynb` |
| `04-regresiónLinealyLogística/regresion_lineal_padre_hijo_presion.ipynb` | `clases/04-regresion-lineal-y-logistica/notebooks/02-regresion-lineal-estatura-y-presion.ipynb` |
| `04-regresiónLinealyLogística/regresion_logistica_evaluación.ipynb` | `clases/04-regresion-lineal-y-logistica/notebooks/03-regresion-logistica-y-evaluacion.ipynb` |
| `05-KNNyArboles/knn_arbol.ipynb` | `clases/05-knn-y-arboles/notebooks/01-comparacion-knn-y-arboles.ipynb` |
| `README.md` | `README.md` |
