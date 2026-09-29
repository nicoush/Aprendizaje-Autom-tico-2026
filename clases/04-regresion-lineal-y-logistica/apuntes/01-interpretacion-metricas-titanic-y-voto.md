# Interpretación de métricas de regresión logística

**Ejemplos de Titanic e intención de voto**

Para evaluar un modelo, conviene seguir este orden: mirar la distribución de las clases, comparar con una regla sencilla, analizar los errores por clase y relacionarlos con el objetivo del problema. La exactitud, por sí sola, no alcanza.

## 1 Regresión logística binaria sobre Titanic

Suponiendo que 0 = no sobrevivió y 1 = sobrevivió, se evaluaron 90 pasajeros:

| **Clase real** | **Pasajeros** | **Porcentaje** |
| --- | --- | --- |
| No sobrevivió | 55 | 61,1% |
| Sobrevivió | 35 | 38,9% |

Existe una diferencia en las cantidades, pero no un desbalance extremo.

### Interpretar la exactitud y compararla con una referencia

La exactitud de 0,54 indica que el modelo clasificó correctamente aproximadamente al 54% de los pasajeros: 49 de 90.

¿Es un buen resultado? Comparemos con una regla que no aprende nada: si siempre predijéramos «no sobrevivió», acertaríamos 55 de los 90 casos: 61,1% de exactitud.

**Por lo tanto, el modelo obtiene menor exactitud que predecir siempre la clase mayoritaria.**

Esto no significa que esa regla sea útil para detectar sobrevivientes: no detectaría ninguno. Significa que el modelo todavía no justifica su utilidad por su exactitud general.

### Interpretar cada clase

| **Métrica** | **Clase 0 no sobrevivió** | **Clase 1 sobrevivió** |
| --- | --- | --- |
| Precisión | De quienes predijo como no sobrevivientes, aproximadamente el 61% realmente no sobrevivió. | De quienes predijo como sobrevivientes, aproximadamente el 39% realmente sobrevivió. |
| Recall | Detectó aproximadamente el 69% de los no sobrevivientes reales. | Detectó aproximadamente el 31% de los sobrevivientes reales. |
| F1 | 0,65: combina precisión y recall para esta clase. | 0,35: refleja un desempeño bajo en ambas métricas para los sobrevivientes. |

## Análisis de los errores en Titanic

La clase 1 presenta dos problemas diferentes:

- Baja precisión: muchas predicciones de supervivencia son incorrectas.

- Bajo recall: la mayoría de los sobrevivientes reales no son identificados.

### Traducir las métricas a cantidades

Los valores redondeados del informe son compatibles con esta matriz:

| **Real / Predicción** | **No sobrevivió 0** | **Sobrevivió 1** | **Total real** |
| --- | --- | --- | --- |
| No sobrevivió 0 | 38 | 17 | 55 |
| Sobrevivió 1 | 24 | 11 | 35 |
| Total predicho | 62 | 28 | 90 |

Podemos verificar:

$$
\text{Exactitud = }\frac{38 + 11}{90} = 54,4\%
$$

$$
\text{Precisión de sobrevivientes = }\frac{11}{11 + 17} = 39,3\%
$$

$$
\text{Recall de sobrevivientes = }\frac{11}{11 + 24} = 31,4\%
$$

El modelo anunció que 28 pasajeros sobrevivirían, pero acertó en 11. Además, de los 35 sobrevivientes reales, encontró solamente 11 y dejó sin detectar a 24.

### Interpretar los promedios

Macro avg: da el mismo peso a cada clase. El recall macro de 0,50 muestra que, al considerar ambas clases por igual, el desempeño es bajo.

Weighted avg: pondera según la cantidad de casos. La clase 0 pesa más porque tiene 55 pasajeros, frente a 35 de la clase 1.

El F1 ponderado de 0,53 no debe ocultar el F1 de 0,35 de los sobrevivientes.

### Conclusión posible para Titanic

Este modelo presenta un desempeño bajo en la muestra evaluada. Su exactitud es inferior a la de una regla que siempre predice “no sobrevivió”, y detecta apenas el 31% de los sobrevivientes. Además, cuando predice supervivencia, acierta solamente el 39% de las veces. No sería adecuado utilizarlo como predictor confiable sin revisar las variables, la preparación de los datos y el entrenamiento, y volver a evaluarlo.

El informe no permite afirmar que existe sobreajuste: para eso necesitamos, entre otras evidencias, comparar entrenamiento y evaluación. Tampoco demuestra por sí solo un error de programación.

## 2 Regresión logística multiclase sobre intención de voto

Se evaluaron 120 personas:

| **Partido real** | **Personas** | **Porcentaje** |
| --- | --- | --- |
| A | 35 | 29,2% |
| B | 39 | 32,5% |
| C | 46 | 38,3% |

Las clases tienen cantidades relativamente cercanas. No hay un desbalance marcado que, por sí solo, explique los resultados.

### Interpretar la exactitud y compararla con una referencia

La exactitud de 0,40 significa que el modelo acertó la intención de voto de 48 de las 120 personas.

Si siempre predijéramos el partido C, el más frecuente:

$$
\text{Exactitud de referencia = }\frac{46}{120} = 38,3\%
$$

El modelo obtiene 40% frente a 38,3%: una mejora de apenas 1,7 puntos porcentuales, equivalente a dos aciertos adicionales.

**El modelo supera ligeramente a la regla mayoritaria, pero esta muestra no alcanza para demostrar que la mejora sea estable y relevante.**

### Interpretar cada partido

| **Partido** | **Interpretación de precisión** | **Interpretación de recall** | **F1** |
| --- | --- | --- | --- |
| A | De quienes predice como votantes de A, solo el 34% realmente corresponde a A. | Detecta al 60% de los votantes reales de A. | 0,44 |
| B | De quienes predice como votantes de B, el 44% realmente corresponde a B. | Detecta solamente al 28% de los votantes reales de B. | 0,34 |
| C | De quienes predice como votantes de C, el 47% realmente corresponde a C. | Detecta solamente al 35% de los votantes reales de C. | 0,40 |

### Partido A encuentra más casos pero se equivoca mucho al asignarlos

Identifica aproximadamente 21 de los 35 votantes de A. Su recall es el mayor, pero su precisión es la menor. Esto indica que predice A para muchas personas que realmente votarían a otros partidos.

Un recall más alto no significa automáticamente un mejor modelo: puede lograrse asignando esa clase con demasiada frecuencia.

## Análisis de los errores en intención de voto

### Partido B deja sin detectar a la mayoría

Identifica aproximadamente 11 de los 39 votantes de B y confunde a los otros 28 con otros partidos. Su F1 de 0,34 es el menor de las tres clases.

### Partido C tiene la mayor precisión pero bajo recall

Identifica aproximadamente 16 de los 46 votantes de C y deja sin detectar a 30. Aunque su precisión es la mayor, 0,47 sigue significando que más de la mitad de las predicciones de C son incorrectas.

### Interpretar los promedios

El F1 macro y el F1 ponderado son ambos aproximadamente 0,39. Como las cantidades por partido son relativamente parecidas, ambos promedios resultan cercanos. El desempeño general sigue siendo bajo, aunque cada partido presenta un patrón de errores diferente.

Sin la matriz de confusión completa, no podemos determinar exactamente entre qué partidos se producen esos errores.

### Conclusión posible para intención de voto

El modelo muestra una capacidad limitada para clasificar la intención de voto. Su exactitud apenas supera la de predecir siempre el partido más frecuente. Identifica una mayor proporción de votantes de A, pero también asigna erróneamente A a muchas personas. Para B y C, deja sin detectar a la mayoría de sus votantes. Antes de considerarlo útil, sería necesario revisar las variables y comprobar si estas diferencias se mantienen en otras muestras.

## La idea central

**No alcanza con preguntar “¿cuánto accuracy tiene?”. Hay que preguntar:**

1. ¿Supera una regla sencilla?

2. ¿Qué clases reconoce y cuáles deja sin detectar?

3. ¿Sus predicciones de cada clase son confiables?

4. ¿Qué errores importan más para el objetivo?

5. ¿El resultado se mantiene con otros datos?

En Titanic, el modelo queda por debajo de la referencia mayoritaria en exactitud. En intención de voto, la supera apenas. En ambos casos, las métricas por clase muestran limitaciones que la exactitud general no explica por sí sola.
