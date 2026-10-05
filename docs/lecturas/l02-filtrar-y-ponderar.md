# L2 · Filtrar y ponderar

**Temas:** 2.4 (modelo de norma mínima); 2.5 (modelo de *scoring*)
**Sesión que la utiliza:** 6 · **Lectura previa a la sesión 6 (miércoles 7 de octubre)**
**Tiempo estimado de lectura:** 30 minutos

**prof. dr. Jesús Zavala Ruiz** · Universidad Autónoma Metropolitana, Unidad Iztapalapa
**Última actualización:** 5 de octubre de 2026
Material de elaboración propia, publicado bajo licencia [Creative Commons Atribución-CompartirIgual 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Los ejemplos y ejercicios son originales y sus resultados se verificaron mediante un programa antes de su publicación.

> «…el nivel de aspiración, que define una alternativa satisfactoria…»
> Simon (1955, p. 111, traducción libre)

---

## 1. Introducción

En la lectura L1 se expuso el planteamiento de la decisión: quién decide, entre qué alternativas, ante qué estados de la naturaleza y con qué consecuencias. En una situación real, sin embargo, las alternativas iniciales rara vez son tres; pueden ser seis, diez o veinte, y antes de construir la matriz de pagos conviene reducirlas. Además, el decisor suele valorar aspectos que no se expresan en pesos, como la confiabilidad, la comodidad o la reputación, y que no por ello son menos importantes para él.

Para atender ambas necesidades se presentan dos modelos. La **norma mínima** responde a la pregunta *¿cuáles alternativas son aceptables?*, mientras que el ***scoring*** responde a la pregunta *entre las aceptables, ¿cuál se prefiere en función de lo que no se mide en pesos?* La lectura se organiza como sigue. En primer lugar, se contrastan los dos modelos y se explica la diferencia entre un modelo compensatorio y uno no compensatorio. En segundo lugar, se presenta el ejemplo que se retoma a lo largo de la lectura. Enseguida, se desarrolla el procedimiento de la norma mínima y después el del *scoring*, con sus cuatro pasos. Posteriormente, se analiza qué tan sensible es la recomendación a las ponderaciones y se examina un caso en el que el orden de aplicación resulta decisivo. Al final se relacionan ambos modelos con el expediente del proyecto P1 y se presentan las conclusiones y los ejercicios.

Al concluir la lectura, el estudiante será capaz de: (1) aplicar una norma mínima y documentar el umbral que eliminó a cada alternativa; (2) construir una tabla de *scoring* con criterios, ponderaciones y calificaciones, y calcular la puntuación de cada alternativa; (3) distinguir un modelo **compensatorio** de uno **no compensatorio**; y (4) explicar por qué las ponderaciones deben acordarse con el decisor.

**Notación.** Rigen las convenciones de la lectura L1: coma para los millares, punto para los decimales, punto y coma para separar valores dentro de una fórmula, `*` para la multiplicación y `/` para la división. Cada fórmula se presenta en notación algebraica, con su desarrollo numérico, y en LaTeX.

---

## 2. Dos preguntas distintas

Considérese la elección de un local para una fiesta. En primer lugar, se descartan sin mayor deliberación los que no tienen capacidad para los invitados o exceden el presupuesto. En segundo lugar, entre los que subsisten, se comparan el ambiente, la ubicación y la comida, y se elige el que resulta más convincente. En esa secuencia se emplearon los dos modelos, y en ese orden.

| | Norma mínima | *Scoring* |
|---|---|---|
| Pregunta | ¿Es aceptable? | ¿Cuál se prefiere? |
| Función | Elimina alternativas | Ordena alternativas |
| Regla | Cada criterio tiene un **umbral**; la alternativa que no lo cumple queda fuera | Cada criterio tiene un **peso**; se suman las calificaciones ponderadas |
| Tipo de modelo | **No compensatorio** | **Compensatorio** |

Un modelo es **no compensatorio** cuando una deficiencia no puede suplirse con una virtud, es decir, cuando basta incumplir un umbral para quedar excluido, por sobresaliente que sea la alternativa en los demás aspectos. Un modelo es **compensatorio** cuando una calificación baja en un criterio puede equilibrarse con una alta en otro. Por esta razón se aplican en el orden indicado: primero se filtra y después se ordena.

### 2.1 Fundamento de la norma mínima

La lógica de la norma mínima se vincula con la obra de Simon (1955), quien sostuvo que, dadas las limitaciones de información y de capacidad de cálculo del decisor real, la elección no se realiza maximizando sobre todas las alternativas posibles, sino comparando cada una con un **nivel de aspiración** (*aspiration level*) que define lo que resulta satisfactorio o insatisfactorio. En esta lectura, los umbrales de la norma mínima desempeñan precisamente ese papel, pues son los niveles de aspiración del decisor.

---

## 3. Ejemplo que se utiliza en el resto de la lectura

Don Arturo posee una purificadora de agua y requiere una camioneta usada para repartir garrafones. Obtuvo seis ofertas:

| Camioneta | Precio (pesos) | Kilometraje (km) | Carga (kg) |
|---|---|---|---|
| A | 120,000 | 150,000 | 900 |
| B | 135,000 | 90,000 | 850 |
| C | 165,000 | 60,000 | 1,000 |
| D | 145,000 | 110,000 | 1,100 |
| E | 128,000 | 100,000 | 700 |
| F | 140,000 | 80,000 | 900 |

---

## 4. Modelo de norma mínima

### 4.1 Procedimiento

El procedimiento consta de cuatro pasos. Primero, se solicitan al decisor los niveles mínimos de aceptación; cada umbral $u_k$ es un **mínimo** o un **máximo**, según la naturaleza del criterio. Segundo, se compara cada alternativa con cada umbral. Tercero, se elimina la alternativa que incumpla **al menos un** umbral. Y cuarto, se registra el umbral que eliminó a cada descartada, junto con el valor que presentaba.

Sea $x_{jk}$ el valor que la alternativa $a_j$ toma en el criterio $k$. La alternativa $a_j$ **sobrevive** si cumple todos los umbrales:

$$x_{jk} \geq u_k \ \text{ (criterios con umbral mínimo)} \qquad \text{y} \qquad x_{jk} \leq u_k \ \text{ (criterios con umbral máximo)}$$

Don Arturo establece que no pagará más de 150,000 pesos, que no comprará una unidad con más de 120,000 km y que la camioneta debe cargar al menos 800 kg.

| Camioneta | ¿Precio ≤ 150,000? | ¿Km ≤ 120,000? | ¿Carga ≥ 800 kg? | Resultado |
|---|---|---|---|---|
| A | Sí | **No** (150,000) | Sí | Eliminada por kilometraje |
| B | Sí | Sí | Sí | Sobrevive |
| C | **No** (165,000) | Sí | Sí | Eliminada por precio |
| D | Sí | Sí | Sí | Sobrevive |
| E | Sí | Sí | **No** (700) | Eliminada por carga |
| F | Sí | Sí | Sí | Sobrevive |

Sobreviven las camionetas B, D y F.

### 4.2 Precauciones

Cabe señalar cuatro precauciones. La primera es que **los umbrales pertenecen al decisor, no al equipo**: si el equipo los establece, decide en lugar de aquel, así que deben solicitarse en la entrevista y registrarse quién los fijó y en qué fecha. La segunda es que **el orden de los criterios no altera el resultado**, pues basta incumplir uno para quedar excluido; lo relevante es registrar *cuál* eliminó a cada alternativa.

La tercera es que, si **ninguna alternativa sobrevive**, los umbrales son más exigentes que el mercado. El equipo no debe relajarlos por su cuenta; corresponde consultar al decisor sobre cuál está dispuesto a flexibilizar. La cuarta es que, si **todas sobreviven**, los umbrales no filtraron nada, por lo que conviene verificar con el decisor si son realmente mínimos o si omitió alguno.

---

## 5. Modelo de *scoring*

El *scoring* se emplea para los criterios que importan al decisor pero **no se expresan en pesos**. Consta de cuatro pasos: la selección de los criterios, su ponderación, la calificación de las alternativas y el cálculo de la puntuación.

### 5.1 Paso 1. Selección de los criterios

Los criterios deben ser relevantes para el decisor, medibles o calificables y **no duplicar** lo que ya consideran la norma mínima o la matriz de pagos. Si el precio se utilizó como umbral y entrará como costo en la matriz, no debe incluirse de nuevo en el *scoring*, porque contarlo dos veces le otorga un peso mayor del que el decisor le asignó.

Don Arturo selecciona tres criterios: **confiabilidad** (reputación mecánica del modelo y estado general), **rendimiento de combustible** y **comodidad del chofer**.

### 5.2 Paso 2. Ponderación de los criterios

La **ponderación** $w_k$ expresa la importancia relativa del criterio $k$. Se representa con un número entre 0 y 1, y **la suma de todas debe ser 1**:

$$\sum_{k=1}^{r} w_k = 1$$

Una forma práctica de obtenerlas con el decisor es la siguiente. En primer lugar, se le solicita que **ordene** los criterios, del más al menos importante. En segundo lugar, se le pide que **distribuya 100 puntos** entre ellos. Enseguida, se divide cada asignación entre 100, es decir, `w_k = puntos_k / 100`. Por último, se le muestra el resultado y se le pregunta si lo considera adecuado; si no, la discusión revela qué criterio faltaba o qué peso era incorrecto.

Don Arturo distribuye 50, 30 y 20 puntos:

| Criterio | Puntos | Ponderación $w_k$ |
|---|---|---|
| Confiabilidad | 50 | `50 / 100 = 0.50` |
| Rendimiento de combustible | 30 | `30 / 100 = 0.30` |
| Comodidad del chofer | 20 | `20 / 100 = 0.20` |
| **Suma** | 100 | **1.00** |

### 5.3 Paso 3. Calificación de las alternativas

Cada alternativa recibe una calificación $v_{kj}$ **de 0 a 10** en cada criterio $k$. Para que distintas personas califiquen de manera comparable, conviene definir con el decisor, de antemano, **qué significan un 0, un 5 y un 10** en cada criterio, y anotar **quién** asignó cada calificación (el decisor, su mecánico, el equipo).

Para mantener la misma convención de la lectura L1, los **criterios ocupan las filas** y las **alternativas las columnas**:

| Criterio $k$ ↓ / Alternativa $j$ → | Ponderación $w_k$ | B | D | F |
|---|---|---|---|---|
| Confiabilidad | 0.50 | 7 | 9 | 6 |
| Rendimiento de combustible | 0.30 | 6 | 5 | 8 |
| Comodidad del chofer | 0.20 | 5 | 6 | 7 |

### 5.4 Paso 4. Cálculo de la puntuación

La **puntuación** de la alternativa $a_j$ es la suma de las calificaciones multiplicadas por sus ponderaciones.

Notación algebraica: `V_j = (w_1 * v_1j) + (w_2 * v_2j) + (w_3 * v_3j)`

$$V_j = \sum_{k=1}^{r} w_k \, v_{kj}$$

Desarrollo para cada alternativa:

- `V_B = (0.50 * 7) + (0.30 * 6) + (0.20 * 5) = 3.5 + 1.8 + 1.0 = 6.3`
- `V_D = (0.50 * 9) + (0.30 * 5) + (0.20 * 6) = 4.5 + 1.5 + 1.2 = 7.2`
- `V_F = (0.50 * 6) + (0.30 * 8) + (0.20 * 7) = 3.0 + 2.4 + 1.4 = 6.8`

| Criterio ↓ / Alternativa → | $w_k$ | B | D | F |
|---|---|---|---|---|
| Confiabilidad | 0.50 | 7 | 9 | 6 |
| Rendimiento de combustible | 0.30 | 6 | 5 | 8 |
| Comodidad del chofer | 0.20 | 5 | 6 | 7 |
| **Puntuación $V_j$** | 1.00 | **6.3** | **7.2** | **6.8** |

Con las ponderaciones de don Arturo, la mejor alternativa es **D**.

---

## 6. Sensibilidad a las ponderaciones

Supóngase que don Arturo hubiera distribuido los puntos de otra manera: 30 a la confiabilidad, 50 al rendimiento y 20 a la comodidad, es decir, $w = (0.30; 0.50; 0.20)$. Las calificaciones no cambian; solo las ponderaciones.

- `V_B = (0.30 * 7) + (0.50 * 6) + (0.20 * 5) = 2.1 + 3.0 + 1.0 = 6.1`
- `V_D = (0.30 * 9) + (0.50 * 5) + (0.20 * 6) = 2.7 + 2.5 + 1.2 = 6.4`
- `V_F = (0.30 * 6) + (0.50 * 8) + (0.20 * 7) = 1.8 + 4.0 + 1.4 = 7.2`

Ahora resulta ganadora **F**. Las camionetas y las calificaciones son las mismas; lo que cambió es la recomendación.

| Ponderaciones (confiabilidad; rendimiento; comodidad) | B | D | F | Gana |
|---|---|---|---|---|
| 0.50; 0.30; 0.20 | 6.3 | 7.2 | 6.8 | D |
| 0.30; 0.50; 0.20 | 6.1 | 6.4 | 7.2 | F |

Este resultado explica por qué **las ponderaciones deben acordarse con el decisor**: expresan sus valores y no los del equipo. Explica también la conveniencia de una **prueba de sensibilidad**, que consiste en modificar ligeramente las ponderaciones y observar si cambia la alternativa ganadora. Si cambia con poco, debe señalarse en la recomendación; si no cambia, la recomendación es más sólida. Cabe añadir que una diferencia de 0.1 o 0.2 puntos entre dos alternativas **no es concluyente**, ya que las calificaciones son juicios y no mediciones exactas.

---

## 7. El caso de la camioneta E

Se calcula la puntuación de E, cuyas calificaciones son 9, 8 y 7, con las ponderaciones de don Arturo:

`V_E = (0.50 * 9) + (0.30 * 8) + (0.20 * 7) = 4.5 + 2.4 + 1.4 = 8.3`

Es la puntuación más alta de las seis ofertas. Sin embargo, E no cumple con el mínimo de 800 kg que don Arturo exige para su operación. De haberse aplicado el *scoring* sin filtro previo, habría resultado ganadora una unidad que no cubre la función básica.

Esto es lo que significa que la norma mínima sea **no compensatoria**: la confiabilidad y el rendimiento sobresalientes de E no compensan su insuficiente capacidad de carga. Un modelo compensatorio, empleado en solitario, habría permitido esa compensación. Debe formularse, no obstante, una salvedad: si el umbral de 800 kg fuera arbitrario, se estaría descartando la mejor opción por una cifra sin sustento. Por ello se pregunta al decisor la razón de cada umbral y se anota su respuesta.

---

## 8. Relación con el proyecto P1

En el proyecto, cada modelo tiene un lugar definido en el expediente:

| Paso del proyecto | Modelo | Componente del expediente |
|---|---|---|
| Reducir las alternativas iniciales | Norma mínima | Componente 2: alternativas iniciales y sobrevivientes, con el umbral que eliminó a cada descartada |
| Valorar lo que no se expresa en pesos | *Scoring* | Componente 3: criterios, ponderaciones acordadas con el decisor, calificaciones y puntuación |
| Calcular los pagos de las sobrevivientes | Matriz de pagos (L1) | Componente 4 |

Debe tenerse presente que **el *scoring* y la matriz de pagos pueden recomendar alternativas distintas**, pues el primero valora lo cualitativo y la segunda lo monetario. Si no coinciden, no se trata de un error sino de información. La recomendación final debe hacerse cargo de la diferencia y explicar cuánto pesa lo no monetario para el decisor.

También deben evitarse seis errores frecuentes: (1) umbrales establecidos por el equipo en lugar del decisor; (2) ponderaciones cuya suma no es 1; (3) calificaciones sin criterio explícito, de modo que cada integrante califica con su propio parámetro; (4) duplicación de un criterio, por ejemplo, el precio en la norma, en el *scoring* y en la matriz; (5) aplicación del *scoring* antes del filtro, con el riesgo de recomendar una alternativa inaceptable; y (6) falta de registro del umbral que eliminó a cada alternativa, que es parte de lo que se evalúa.

---

## 9. Conclusiones

Quedó claro que la norma mínima y el *scoring* responden a preguntas distintas y que deben aplicarse en un orden determinado. La primera es un modelo no compensatorio que elimina las alternativas inaceptables mediante umbrales que fija el decisor, que son sus niveles de aspiración, y que obliga a registrar cuál umbral eliminó a cada una. El segundo es un modelo compensatorio que ordena las sobrevivientes mediante ponderaciones y calificaciones, y que solo tiene sentido si se aplica después del filtro, como mostró el caso de la camioneta E.

También quedó claro que el resultado del *scoring* depende de las ponderaciones, de manera que estas no pueden decidirlas los estudiantes y deben acordarse con el decisor, y que conviene verificar siempre si la recomendación cambia con pequeñas variaciones de los pesos. Por último, el *scoring* y la matriz de pagos valoran cosas diferentes, de modo que su eventual discrepancia constituye información que la recomendación debe explicar. Con la matriz de las alternativas sobrevivientes ya construida, la lectura L3 aborda cómo decidir cuando se desconoce la probabilidad de los estados de la naturaleza.

---

## 10. Ejercicios

Se recomienda resolverlos antes de consultar las respuestas.

**Contexto.** Un grupo de 25 estudiantes elige el lugar de su comida de fin de curso. Fija como condiciones mínimas: precio de **120 pesos por persona o menos**, capacidad de **25 personas o más** y distancia a la Unidad de **2 km o menos**. Posteriormente califica de 0 a 10 tres criterios no monetarios.

| Lugar | Precio por persona (pesos) | Capacidad (personas) | Distancia (km) |
|---|---|---|---|
| P | 110 | 30 | 1.5 |
| Q | 95 | 20 | 0.5 |
| R | 130 | 40 | 1.0 |
| S | 115 | 28 | 1.8 |
| T | 100 | 50 | 1.2 |

| Criterio ↓ / Lugar → | P | Q | R | S | T |
|---|---|---|---|---|---|
| Ambiente | 8 | 9 | 7 | 6 | 7 |
| Menú | 6 | 9 | 8 | 8 | 6 |
| Accesibilidad | 9 | 9 | 8 | 6 | 10 |

**Ejercicio 1.** Aplique la norma mínima. ¿Qué lugares sobreviven y qué umbral eliminó a cada uno de los demás?

**Ejercicio 2.** Con las ponderaciones ambiente 0.20; menú 0.50; accesibilidad 0.30, calcule la puntuación de los lugares sobrevivientes, mostrando el desarrollo de la fórmula con paréntesis. ¿Cuál resulta ganador?

**Ejercicio 3.** Si las ponderaciones fueran ambiente 0.50; menú 0.20; accesibilidad 0.30, ¿cambia el ganador?

**Ejercicio 4.** Calcule la puntuación del lugar Q con las ponderaciones del ejercicio 2. ¿Importa que sea elevada?

**Ejercicio 5.** Explique con sus palabras por qué la norma mínima es no compensatoria y el *scoring* es compensatorio. Proporcione un ejemplo de cada uno que no provenga de esta lectura.

---

## Respuestas para verificar

**Ejercicio 1.** Sobreviven **P, S y T**. El lugar Q queda eliminado por capacidad (20 < 25) y el lugar R por precio (130 > 120).

**Ejercicio 2.** Con $w = (0.20; 0.50; 0.30)$:

- `V_P = (0.20 * 8) + (0.50 * 6) + (0.30 * 9) = 1.6 + 3.0 + 2.7 = 7.3`
- `V_S = (0.20 * 6) + (0.50 * 8) + (0.30 * 6) = 1.2 + 4.0 + 1.8 = 7.0`
- `V_T = (0.20 * 7) + (0.50 * 6) + (0.30 * 10) = 1.4 + 3.0 + 3.0 = 7.4`

Gana **T** (7.4), seguido de cerca por P (7.3); la diferencia es de una décima.

**Ejercicio 3.** Con $w = (0.50; 0.20; 0.30)$:

- `V_P = (0.50 * 8) + (0.20 * 6) + (0.30 * 9) = 4.0 + 1.2 + 2.7 = 7.9`
- `V_S = (0.50 * 6) + (0.20 * 8) + (0.30 * 6) = 3.0 + 1.6 + 1.8 = 6.4`
- `V_T = (0.50 * 7) + (0.20 * 6) + (0.30 * 10) = 3.5 + 1.2 + 3.0 = 7.7`

Gana **P**. El ganador cambia, de modo que la recomendación del ejercicio anterior era frágil.

**Ejercicio 4.** `V_Q = (0.20 * 9) + (0.50 * 9) + (0.30 * 9) = 1.8 + 4.5 + 2.7 = 9.0`, la puntuación más alta de todas. No es relevante, porque Q fue eliminado por no tener capacidad para 25 personas: el modelo de norma mínima es no compensatorio.

**Ejercicio 5.** Respuesta modelo: la norma mínima es no compensatoria porque basta incumplir un umbral para quedar excluido, aun cuando se destaque en todo lo demás (un aspirante con excelente currículum que no posee el título que exige la convocatoria). El *scoring* es compensatorio porque una calificación baja puede equilibrarse con una alta (un aspirante de experiencia limitada que lo compensa con excelentes referencias, en una evaluación por puntos).

---

## Para la sesión 6

Se solicita presentar los umbrales de aceptación proporcionados por el decisor, con fecha, y la lista de criterios no monetarios de la decisión con el orden de importancia que el decisor les asigna.

En la sesión 6 el uso del asistente de IAG es obligatorio, con bitácora. Una consulta pertinente consiste en solicitarle que explique la diferencia entre modelo compensatorio y no compensatorio con un ejemplo ajeno a esta lectura, y **verificar su explicación contra el contenido de esta lectura**.

---

## Para ampliar (opcional)

Las obras citadas tienen derechos reservados; se mencionan por capítulo y no se reproducen. Pueden consultarse en el [catálogo del acervo físico](https://amoxcalli.izt.uam.mx/) o en la [biblioteca digital](https://bidi.uam.mx).

- Racionalidad limitada y niveles de aspiración: Simon (1955).
- Modelos de toma de decisión y sus tipos: Amaya Amaya (2010), cap. 2.
- Costos relevantes para una decisión, útil para determinar qué debe entrar en la matriz de pagos y qué debe quedar fuera: Torres Salinas (2010), cap. 1.

## Referencias

Amaya Amaya, J. (2010). *Toma de decisiones gerenciales* (2.ª ed.). Ecoe Ediciones.
Simon, H. A. (1955). A behavioral model of rational choice. *The Quarterly Journal of Economics, 69*(1), 99–118. https://doi.org/10.2307/1884852
Torres Salinas, A. S. (2010). *Contabilidad de costos: Análisis para la toma de decisiones* (3.ª ed.). McGraw-Hill Interamericana.
