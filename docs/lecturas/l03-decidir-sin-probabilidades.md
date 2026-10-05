# L3 · Decidir sin probabilidades

**Tema:** 2.6 (criterios de decisión bajo incertidumbre: Wald, maximax, Hurwicz, Savage y Laplace)
**Sesiones que la utilizan:** 6 y 7 · **Lectura previa a la sesión 6 (miércoles 7 de octubre)**
**Tiempo estimado de lectura:** 30 minutos

**prof. dr. Jesús Zavala Ruiz** · Universidad Autónoma Metropolitana, Unidad Iztapalapa
**Última actualización:** 5 de octubre de 2026
Material de elaboración propia, publicado bajo licencia [Creative Commons Atribución-CompartirIgual 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Los ejemplos y ejercicios son originales y sus resultados se verificaron mediante un programa antes de su publicación.

> «…sin hacer jamás cálculos de probabilidad…»
> Simon (1955, p. 118, traducción libre)

---

## 1. Introducción

En las lecturas anteriores se construyó la matriz de pagos y se eliminaron las alternativas dominadas (L1); después se redujo el conjunto de alternativas mediante la norma mínima (L2). Queda por resolver la pregunta central del proyecto P1: ¿qué alternativa debe recomendarse cuando se desconoce la probabilidad de cada estado de la naturaleza? Esta situación se denomina **incertidumbre** (*uncertainty*) y se distingue de la de **riesgo** (*risk*), en la que sí se dispone de probabilidades, caso que se estudia en el proyecto P2.

No existe una respuesta única, porque la recomendación depende de la actitud del decisor ante lo desconocido: cautela, optimismo, aversión al arrepentimiento o indiferencia. Cada uno de los cinco criterios que se presentan traduce una de estas actitudes en una regla de cálculo. Cabe señalar que Simon (1955) ya había descrito la regla *max-min* como uno de los conceptos «clásicos» de racionalidad, junto con la regla probabilística y la de certeza; la diferencia es que aquí se estudian varias reglas para un mismo problema y se pregunta por qué discrepan.

La lectura se organiza como sigue. En primer lugar, se precisan la notación y las convenciones, y se presenta el ejemplo que se retoma en todo el texto. Enseguida, se desarrollan los criterios de Wald, maximax y Hurwicz, este último con la determinación del valor de α en el que cambia su recomendación. Después, se exponen los criterios de Savage y de Laplace. Posteriormente, se analizan los cinco criterios en conjunto, con las razones de su discrepancia y dos advertencias, y se indica cómo redactar la recomendación. Al final se presentan las conclusiones y los ejercicios.

Al concluir la lectura, el estudiante será capaz de: (1) aplicar a mano los criterios de Wald, maximax, Hurwicz, Savage y Laplace; (2) explicar qué pregunta responde cada criterio y qué actitud ante el riesgo representa; (3) determinar el valor de α en el que cambia la recomendación del criterio de Hurwicz; y (4) explicar por qué los criterios discrepan y redactar una recomendación que se haga cargo de esa discrepancia.

---

## 2. Notación y convenciones

**Números.** La coma separa los millares y el punto separa los decimales (35,000; 0.38). Dentro de una fórmula, los valores enumerados se separan con punto y coma: `min(26,000; 36,000; 46,000)`.

**Matriz de pagos.** Se conserva la disposición de la lectura L1:

- los **estados de la naturaleza** $\theta_i$, $i = 1, \dots, m$, ocupan las **filas**;
- las **alternativas** $a_j$, $j = 1, \dots, n$, ocupan las **columnas**;
- $c_{ij}$ es el pago de la alternativa $a_j$ cuando ocurre el estado $\theta_i$.

Dado que algunos autores presentan la matriz con las alternativas en las filas y los estados en las columnas, **cada criterio se enuncia en términos de «para cada alternativa» y «para cada estado»**, de modo que pueda trasladarse a cualquiera de las dos disposiciones. En el ejercicio 7 se practica con la disposición inversa.

**Fórmulas.** Cada una se presenta en notación algebraica de una línea (`*` para multiplicar, `/` para dividir, con paréntesis explícitos), con su desarrollo numérico y en LaTeX.

---

## 3. Ejemplo que se utiliza en el resto de la lectura

Una cooperativa de apicultores dispone de **500 kg de miel** lista para vender. Debe decidir cómo hacerlo antes de conocer el precio al que se pagará el kilo en la temporada, variable que la cooperativa no controla. Los estados de la naturaleza son tres: que el precio por kilo resulte de **60, 80 o 100 pesos**. No se cuenta con datos que permitan juzgar cuál es más probable.

Se consideran tres alternativas. La primera, **a₁**, consiste en vender a un intermediario, que paga un precio fijo de 70 pesos por kilo, independientemente del mercado. La segunda, **a₂**, consiste en vender en el mercado local, al precio que resulte, con gastos de flete y puesto de 4,000 pesos. La tercera, **a₃**, consiste en vender en línea, con envío; por la presentación del producto se obtiene un 25 % más por kilo que el precio de mercado, pero se gastan 12,000 pesos en envases y envíos. Sea $p_i$ el precio del kilo bajo el estado $\theta_i$: $p_1 = 60$, $p_2 = 80$ y $p_3 = 100$ pesos.

**Pago de a₁.** Notación algebraica: `c_i1 = 500 * 70 = 35,000` para $i = 1, 2, 3$.

**Pago de a₂.** Notación algebraica: `c_i2 = (500 * p_i) - 4,000`

$$c_{i2} = 500\,p_i - 4{,}000$$

- `c_12 = (500 * 60) - 4,000 = 30,000 - 4,000 = 26,000`
- `c_22 = (500 * 80) - 4,000 = 40,000 - 4,000 = 36,000`
- `c_32 = (500 * 100) - 4,000 = 50,000 - 4,000 = 46,000`

**Pago de a₃.** Notación algebraica: `c_i3 = ((500 * p_i) * 1.25) - 12,000`

$$c_{i3} = (500\,p_i)(1.25) - 12{,}000$$

- `c_13 = ((500 * 60) * 1.25) - 12,000 = (30,000 * 1.25) - 12,000 = 37,500 - 12,000 = 25,500`
- `c_23 = ((500 * 80) * 1.25) - 12,000 = (40,000 * 1.25) - 12,000 = 50,000 - 12,000 = 38,000`
- `c_33 = ((500 * 100) * 1.25) - 12,000 = (50,000 * 1.25) - 12,000 = 62,500 - 12,000 = 50,500`

**Matriz de pagos** (pesos):

| Estado ↓ / Alternativa → | a₁ · Intermediario | a₂ · Mercado local | a₃ · En línea |
|---|---|---|---|
| θ₁ · Precio de 60 pesos | 35,000 | 26,000 | 25,500 |
| θ₂ · Precio de 80 pesos | 35,000 | 36,000 | 38,000 |
| θ₃ · Precio de 100 pesos | 35,000 | 46,000 | 50,500 |

**Dominación (L1).** Ninguna alternativa domina a otra: a₁ es la mejor si el precio es bajo, y a₃ lo es si el precio es medio o alto. Por lo tanto, las tres son admisibles.

---

## 4. Criterio de Wald (maximin)

El criterio de Wald corresponde a una actitud de **cautela**: se supone que ocurrirá el peor estado. La pregunta que responde es *¿qué alternativa protege mejor frente al peor escenario?* Su nombre alterno, *maximin*, describe el procedimiento (*the maximum of the minimums*).

El procedimiento consta de dos pasos. En primer lugar, se determina, para cada alternativa $a_j$, su **pago mínimo** $W_j$ entre todos los estados. En segundo lugar, se elige la alternativa con el **mayor** de esos mínimos, de ahí «maximin».

Notación algebraica: `W(a_j) = min(c_1j; c_2j; c_3j)`; se elige la alternativa con `max(W(a_1); W(a_2); W(a_3))`.

$$W_j = \min_{i} \, c_{ij} \qquad \text{se elige } a_{j^{*}} \text{ tal que } W_{j^{*}} = \max_{j} \, W_j$$

En la disposición de esta lectura, el mínimo de cada alternativa se busca **por columna**. El desarrollo es el siguiente:

- `W(a_1) = min(35,000; 35,000; 35,000) = 35,000`
- `W(a_2) = min(26,000; 36,000; 46,000) = 26,000`
- `W(a_3) = min(25,500; 38,000; 50,500) = 25,500`

El criterio **recomienda a₁** (35,000). Esta alternativa garantiza el mismo pago en cualquier estado y, por lo tanto, ninguna otra tiene un mejor peor caso.

---

## 5. Criterio maximax

El criterio maximax corresponde a una actitud de **optimismo**: se supone que ocurrirá el mejor estado. La pregunta que responde es *¿cuál alternativa produce más si todo resulta favorable?*

El procedimiento es el simétrico del anterior. Primero, se determina, para cada alternativa $a_j$, su **pago máximo** $M_j$ entre todos los estados. Después, se elige la alternativa con el **mayor** de esos máximos.

Notación algebraica: `M(a_j) = max(c_1j; c_2j; c_3j)`; se elige la alternativa con `max(M(a_1); M(a_2); M(a_3))`.

$$M_j = \max_{i} \, c_{ij} \qquad \text{se elige } a_{j^{*}} \text{ tal que } M_{j^{*}} = \max_{j} \, M_j$$

Desarrollo:

- `M(a_1) = max(35,000; 35,000; 35,000) = 35,000`
- `M(a_2) = max(26,000; 36,000; 46,000) = 46,000`
- `M(a_3) = max(25,500; 38,000; 50,500) = 50,500`

El criterio **recomienda a₃** (50,500). Acepta ganar menos si el precio es bajo a cambio de ganar más si es alto. Cabe señalar que algunos textos denominan «conservador» al criterio de Wald y «optimista» al maximax; se trata de los mismos criterios.

---

## 6. Criterio de Hurwicz

Wald y maximax son posiciones extremas: nadie es perfectamente cauteloso ni perfectamente optimista. El criterio de Hurwicz permite adoptar una posición intermedia mediante el **coeficiente de optimismo α** (*coefficient of optimism*), con $0 \leq \alpha \leq 1$.

El procedimiento consta de tres pasos. Primero, se fija el valor de α. Segundo, se calcula para cada alternativa el **índice de Hurwicz**, que pondera el mejor y el peor pago según la fórmula que se presenta a continuación. Tercero, se elige la alternativa con el mayor índice.

Notación algebraica: `H(a_j) = (α * M(a_j)) + ((1 - α) * W(a_j))`

$$H_j = \alpha \, M_j + (1 - \alpha) \, W_j$$

El valor de α expresa el peso que se otorga al mejor caso frente al peor. Si **α = 0**, el índice equivale al pago mínimo y se obtiene el criterio de Wald; si **α = 1**, equivale al pago máximo y se obtiene el maximax; y si **α = 0.5**, el mejor y el peor caso pesan lo mismo.

Para obtener α se pregunta al decisor: «En una escala de 0 a 10, donde 0 significa esperar siempre lo peor y 10 esperar siempre lo mejor, ¿en qué punto se ubica al decidir esto?». La respuesta dividida entre 10 es α: `α = respuesta / 10`. Si responde 4, `α = 4 / 10 = 0.4`.

Con α = 0.4, el cálculo es el siguiente:

- `H(a_1) = (0.4 * 35,000) + ((1 - 0.4) * 35,000) = 14,000 + (0.6 * 35,000) = 14,000 + 21,000 = 35,000`
- `H(a_2) = (0.4 * 46,000) + ((1 - 0.4) * 26,000) = 18,400 + (0.6 * 26,000) = 18,400 + 15,600 = 34,000`
- `H(a_3) = (0.4 * 50,500) + ((1 - 0.4) * 25,500) = 20,200 + (0.6 * 25,500) = 20,200 + 15,300 = 35,500`

El criterio **recomienda a₃** (35,500). Sin embargo, conviene advertir que a₁ (35,000) queda muy cerca, lo cual es indicio de que la recomendación es sensible al valor de α.

### 6.1 Valor de α en el que cambia la recomendación

Al variar α se obtiene:

| α | H(a₁) | H(a₂) | H(a₃) | Recomienda |
|---|---|---|---|---|
| 0.2 | 35,000 | 30,000 | 30,500 | a₁ |
| 0.3 | 35,000 | 32,000 | 33,000 | a₁ |
| **0.38** | 35,000 | 33,600 | **35,000** | **empate entre a₁ y a₃** |
| 0.4 | 35,000 | 34,000 | 35,500 | a₃ |
| 0.5 | 35,000 | 36,000 | 38,000 | a₃ |
| 0.7 | 35,000 | 40,000 | 43,000 | a₃ |

El valor crítico α* se obtiene igualando los índices de las dos alternativas en competencia, a₁ y a₃. Notación algebraica y desarrollo:

- `H(a_1) = H(a_3)`
- `35,000 = (α * 50,500) + ((1 - α) * 25,500)`
- `35,000 = (α * 50,500) + 25,500 - (α * 25,500)`
- `35,000 - 25,500 = α * (50,500 - 25,500)`
- `9,500 = α * 25,000`
- `α = 9,500 / 25,000 = 0.38`

$$\alpha^{*} = \frac{35{,}000 - 25{,}500}{50{,}500 - 25{,}500} = \frac{9{,}500}{25{,}000} = 0.38$$

Para $\alpha < 0.38$, Hurwicz recomienda a₁; para $\alpha > 0.38$, recomienda a₃. Además, **a₂ no resulta ganadora para ningún α entre 0 y 1**, porque es una alternativa intermedia que no es la mejor ni en el peor caso ni en el mejor. Con este resultado puede informarse al decisor: «su α de 0.4 está apenas por encima de 0.38, valor en el que cambia la recomendación; si fuera algo más cauteloso, la recomendación sería a₁».

---

## 7. Criterio de Savage (minimax del arrepentimiento)

El criterio de Savage corresponde a una actitud de **aversión al arrepentimiento** (*regret*): importa menos cuánto se gana que cuánto se *deja de ganar* por haber elegido mal. La pregunta que responde es *¿qué alternativa deja el menor arrepentimiento, ocurra lo que ocurra?*

El procedimiento consta de tres pasos. En primer lugar, se construye la **matriz de arrepentimiento**: para cada **estado** $\theta_i$, se determina el mejor pago entre todas las alternativas y se resta el pago de cada alternativa. El resultado, $r_{ij}$, es lo que se deja de ganar en ese estado por no haber elegido la mejor alternativa, y nunca es negativo. En segundo lugar, se determina, para cada **alternativa**, su **mayor arrepentimiento** $R_j$ entre todos los estados. En tercer lugar, se elige la alternativa cuyo mayor arrepentimiento sea el **menor**, de ahí «minimax».

Notación algebraica: `r_ij = max(c_i1; c_i2; c_i3) - c_ij` y `R(a_j) = max(r_1j; r_2j; r_3j)`; se elige la alternativa con `min(R(a_1); R(a_2); R(a_3))`.

$$r_{ij} = \left(\max_{k} \, c_{ik}\right) - c_{ij} \qquad R_j = \max_{i} \, r_{ij} \qquad \text{se elige } a_{j^{*}} \text{ tal que } R_{j^{*}} = \min_{j} \, R_j$$

En la disposición de esta lectura, el mejor pago de cada estado se busca **por fila**, y el mayor arrepentimiento de cada alternativa **por columna**. Los mejores pagos por estado son: θ₁, 35,000; θ₂, 38,000; θ₃, 50,500. El desarrollo de la matriz de arrepentimiento (pesos) es el siguiente:

| Estado ↓ / Alternativa → | a₁ | a₂ | a₃ |
|---|---|---|---|
| θ₁ | `35,000 - 35,000 = 0` | `35,000 - 26,000 = 9,000` | `35,000 - 25,500 = 9,500` |
| θ₂ | `38,000 - 35,000 = 3,000` | `38,000 - 36,000 = 2,000` | `38,000 - 38,000 = 0` |
| θ₃ | `50,500 - 35,000 = 15,500` | `50,500 - 46,000 = 4,500` | `50,500 - 50,500 = 0` |
| **Mayor arrepentimiento R(aⱼ)** | **15,500** | **9,000** | **9,500** |

El criterio **recomienda a₂**, cuyo mayor arrepentimiento es de 9,000 pesos. Es la alternativa que nunca queda demasiado lejos de lo mejor. El arrepentimiento de 15,500 pesos en a₁ es lo que se dejaría de ganar si el precio resultara de 100 pesos y la cooperativa hubiera vendido a precio fijo.

---

## 8. Criterio de Laplace (equiprobabilidad)

El criterio de Laplace corresponde a una actitud de **indiferencia**: al no existir razón para considerar más probable un estado que otro, se les trata como igualmente probables. La pregunta que responde es *¿cuál alternativa rinde más, en promedio, si todos los estados fueran igualmente posibles?*

El procedimiento consta de dos pasos. Primero, se calcula, para cada alternativa $a_j$, el **promedio simple** de sus pagos entre los $m$ estados. Segundo, se elige la alternativa con el mayor promedio.

Notación algebraica (con $m = 3$ estados): `L(a_j) = (c_1j + c_2j + c_3j) / 3`

$$L_j = \frac{1}{m} \sum_{i=1}^{m} c_{ij}$$

Desarrollo:

- `L(a_1) = (35,000 + 35,000 + 35,000) / 3 = 105,000 / 3 = 35,000`
- `L(a_2) = (26,000 + 36,000 + 46,000) / 3 = 108,000 / 3 = 36,000`
- `L(a_3) = (25,500 + 38,000 + 50,500) / 3 = 114,000 / 3 = 38,000`

El criterio **recomienda a₃** (38,000).

Es frecuente confundir el criterio de Laplace con la decisión bajo riesgo. Sin embargo, Laplace no decide *con* probabilidades, sino *a falta* de ellas, suponiéndolas iguales por ignorancia. Si la cooperativa dispusiera de registros de precios de años anteriores, ya no estaría en incertidumbre sino en riesgo, caso que se estudia en P2, donde las probabilidades tienen una fuente declarada. En Laplace, la igualdad de probabilidades es un supuesto que debe declararse, no un dato.

---

## 9. Los cinco criterios en conjunto

| Criterio | Actitud | Recomienda |
|---|---|---|
| Wald (maximin) | Cautela | a₁ |
| Maximax | Optimismo | a₃ |
| Hurwicz (α = 0.4) | Intermedia | a₃ |
| Savage | Aversión al arrepentimiento | a₂ |
| Laplace | Indiferencia | a₃ |

Claramente, los criterios no coinciden. Esto no constituye una falla del método, sino la consecuencia de que cada uno plantea una pregunta distinta; si todos arrojaran la misma respuesta, no habría necesidad de emplear varios.

### 9.1 Razones de la discrepancia

La alternativa **a₁** resulta ganadora con Wald porque es la única que garantiza 35,000 pesos en cualquier circunstancia: protege frente al peor escenario. La alternativa **a₃** resulta ganadora con maximax, Hurwicz y Laplace porque posee el mayor potencial (50,500) y el mayor rendimiento promedio, aunque pierda cuando el precio es bajo. Por último, la alternativa **a₂** resulta ganadora con Savage porque es la que menos se aleja del mejor resultado en cualquier estado, aunque no sea nunca la mejor.

Al redactar la recomendación no basta, por lo tanto, con reproducir los resultados: es necesario explicar **por qué** cada criterio recomienda lo que recomienda, en términos de la decisión.

### 9.2 Dos advertencias

**Primera: no se decide por votación.** Aunque tres de los cinco criterios recomienden a₃, ello no la convierte en la respuesta. Los criterios no son jueces independientes con igual derecho al voto, sino actitudes ante el riesgo, y la que cuenta es la **del decisor**. Si el decisor es muy cauteloso (α bajo), Wald y Hurwicz con α bajo recomiendan a₁, aun cuando otros criterios señalen lo contrario. La recomendación se construye desde la actitud del decisor y no desde un conteo.

**Segunda: los resultados dependen de las alternativas incluidas en la matriz.** El criterio de Savage, en particular, cambia al agregar o suprimir una alternativa, porque se modifica el mejor pago de cada estado. Si la cooperativa descartara a₁, el mejor pago de cada estado pasaría a ser 26,000 (θ₁), 38,000 (θ₂) y 50,500 (θ₃), y la matriz de arrepentimiento sería:

| Estado ↓ / Alternativa → | a₂ | a₃ |
|---|---|---|
| θ₁ | `26,000 - 26,000 = 0` | `26,000 - 25,500 = 500` |
| θ₂ | `38,000 - 36,000 = 2,000` | `38,000 - 38,000 = 0` |
| θ₃ | `50,500 - 46,000 = 4,500` | `50,500 - 50,500 = 0` |
| **Mayor arrepentimiento** | **4,500** | **500** |

Sin a₁, Savage recomienda **a₃** y no a₂. Por ello, el análisis de dominación y la norma mínima se realizan *antes*, y la matriz que ingresa a los cinco criterios debe ser la definitiva.

---

## 10. Redacción de la recomendación

La recomendación de una cuartilla que exige el expediente sigue un orden de cinco elementos. En primer lugar, se indica **qué recomienda el equipo** y para qué actitud ante el riesgo. En segundo lugar, se explica **por qué los criterios no coinciden**, a partir de las características de la matriz y no solo de los números. En tercer lugar, se señala **cuál es la actitud del decisor** (el α que declaró) y qué criterio la representa. Enseguida, se precisa **qué tan sensible es la recomendación**, es decir, si cambia al modificar α ligeramente y a partir de qué valor. Al final, se identifica **qué dato nuevo modificaría la recomendación**.

En el caso de la cooperativa, un cierre apropiado sería: «Si el decisor se declara cauteloso (α menor que 0.38), se recomienda el intermediario, que garantiza 35,000 pesos. Si prefiere asumir mayor riesgo, se recomienda la venta en línea. La venta en el mercado local nunca es la mejor opción para el criterio de Hurwicz, aunque es la que menor arrepentimiento deja».

---

## 11. Antes de la sesión 7

En la sesión 7 se reproducen estos cálculos en una hoja de cálculo y se comparan con el cálculo manual. Por ello **el cálculo se realiza primero a mano**: quien no sabe calcular un criterio en papel no puede juzgar si la hoja está en lo correcto. El orden de verificación es el siguiente: cálculo manual, hoja de cálculo, consulta al asistente de IAG y comparación escrita de los tres resultados.

---

## 12. Conclusiones

Quedó claro que, ante la ausencia de probabilidades, no existe una regla única de decisión, sino cinco, y que cada una responde a una pregunta distinta: Wald, qué protege del peor escenario; maximax, qué produce más si todo sale bien; Hurwicz, qué conviene para una actitud intermedia, medida con el coeficiente α; Savage, qué deja menos arrepentimiento; y Laplace, qué rinde más si se supone, por ignorancia, que los estados son igualmente posibles. En el ejemplo de la cooperativa, las recomendaciones fueron a₁, a₃, a₃, a₂ y a₃, respectivamente.

También quedó claro que la discrepancia entre los criterios no es una falla sino información: indica que la decisión depende de la actitud del decisor. Por esta razón, la recomendación no se obtiene contando cuántos criterios la respaldan, sino explicando qué actitud representa cada uno y cuál corresponde al decisor. En el criterio de Hurwicz, el valor de α* (0.38 en el ejemplo) permite informar qué tan sensible es la recomendación. Por último, se señaló que los resultados, en particular los de Savage, dependen de las alternativas incluidas, de modo que la matriz que ingresa a los criterios debe ser la definitiva.

---

## 13. Ejercicios

Se recomienda resolverlos antes de consultar las respuestas. Los pagos están en **miles de pesos**.

Matriz de los ejercicios 1 a 6 (estados en filas, alternativas en columnas):

| Estado ↓ / Alternativa → | P | Q | R |
|---|---|---|---|
| θ₁ | 40 | 10 | 0 |
| θ₂ | 40 | 50 | 45 |
| θ₃ | 40 | 70 | 90 |

**Ejercicio 1.** Calcule, a mano, los criterios de Wald, maximax y Laplace, mostrando el desarrollo de cada fórmula.

**Ejercicio 2.** Construya la matriz de arrepentimiento y aplique el criterio de Savage.

**Ejercicio 3.** Aplique el criterio de Hurwicz con α = 0.5 y con α = 0.4.

**Ejercicio 4.** Determine el valor de α en el que Hurwicz cambia su recomendación entre P y R.

**Ejercicio 5.** ¿Resulta ganadora la alternativa Q con Hurwicz para algún valor de α? Explique por qué.

**Ejercicio 6.** Explique con sus palabras por qué el criterio de Laplace no equivale a decidir con probabilidades.

**Ejercicio 7 (disposición inversa).** Una fuente presenta la siguiente matriz con las **alternativas en las filas** y los **estados de la naturaleza en las columnas** (pagos en miles de pesos):

| Alternativa ↓ / Estado → | θ₁ | θ₂ | θ₃ |
|---|---|---|---|
| a₁ | 90 | 70 | 55 |
| a₂ | 45 | 35 | 125 |
| a₃ | 25 | 110 | 120 |

a) Verifique que ninguna alternativa domina a otra.
b) Aplique los criterios de Wald, maximax, Laplace y Savage, y el de Hurwicz con α = 0.5. Indique, en cada caso, si el mínimo, el máximo o el promedio de cada alternativa se calcula **por fila** o **por columna** en esta disposición, y si el mejor pago de cada estado se busca por fila o por columna.
c) Transcriba la matriz a la disposición de esta lectura y confirme que los resultados no cambian.

---

## Respuestas para verificar

**Ejercicio 1.**

- Wald: `W(P) = min(40; 40; 40) = 40`; `W(Q) = min(10; 50; 70) = 10`; `W(R) = min(0; 45; 90) = 0`. **Recomienda P.**
- Maximax: `M(P) = 40`; `M(Q) = max(10; 50; 70) = 70`; `M(R) = max(0; 45; 90) = 90`. **Recomienda R.**
- Laplace: `L(P) = (40 + 40 + 40) / 3 = 40`; `L(Q) = (10 + 50 + 70) / 3 = 130 / 3 = 43.33`; `L(R) = (0 + 45 + 90) / 3 = 135 / 3 = 45`. **Recomienda R.**

**Ejercicio 2.** Los mejores pagos por estado son: θ₁, 40; θ₂, 50; θ₃, 90.

| Estado ↓ / Alternativa → | P | Q | R |
|---|---|---|---|
| θ₁ | `40 - 40 = 0` | `40 - 10 = 30` | `40 - 0 = 40` |
| θ₂ | `50 - 40 = 10` | `50 - 50 = 0` | `50 - 45 = 5` |
| θ₃ | `90 - 40 = 50` | `90 - 70 = 20` | `90 - 90 = 0` |
| **Mayor arrepentimiento** | 50 | **30** | 40 |

**Savage recomienda Q** (mayor arrepentimiento de 30).

**Ejercicio 3.**

- Con **α = 0.5**: `H(P) = (0.5 * 40) + ((1 - 0.5) * 40) = 20 + 20 = 40`; `H(Q) = (0.5 * 70) + (0.5 * 10) = 35 + 5 = 40`; `H(R) = (0.5 * 90) + (0.5 * 0) = 45`. **Recomienda R.**
- Con **α = 0.4**: `H(P) = (0.4 * 40) + (0.6 * 40) = 40`; `H(Q) = (0.4 * 70) + (0.6 * 10) = 28 + 6 = 34`; `H(R) = (0.4 * 90) + (0.6 * 0) = 36`. **Recomienda P.**

**Ejercicio 4.** `H(P) = 40` para cualquier α; `H(R) = (α * 90) + ((1 - α) * 0) = 90 * α`. Se igualan: `90 * α = 40`, de donde `α = 40 / 90 = 0.4444…` ≈ 0.444 (es decir, 4/9). Para α menor, Hurwicz recomienda P; para α mayor, recomienda R.

$$\alpha^{*} = \frac{40 - 0}{90 - 0} = \frac{4}{9} \approx 0.444$$

**Ejercicio 5.** **No.** El índice de Q es `H(Q) = (α * 70) + ((1 - α) * 10) = 10 + (60 * α)`. Q superaría a P solo si `10 + (60 * α) > 40`, es decir, si α > 0.5; pero para α > 1/3 el índice de R, `90 * α`, ya supera al de Q (`90 * α > 10 + (60 * α)` equivale a `30 * α > 10`). Por lo tanto, cuando Q podría superar a P, R es mejor que Q. En α = 0.5, Q empata con P en 40, mientras R obtiene 45. Q nunca gana: es la alternativa intermedia que no es la mejor ni en el mejor ni en el peor caso. Es, sin embargo, la que recomienda Savage.

**Ejercicio 6.** Respuesta modelo: decidir con probabilidades supone contar con información sobre qué tan probable es cada estado, ya sea por registros o por el juicio del decisor. Laplace, en cambio, asigna probabilidades iguales *porque no se sabe nada*, no porque se haya comprobado que sean iguales. Es un supuesto de ignorancia, no un dato. Si se contara con datos, la distribución dejaría de ser uniforme y la decisión pasaría al terreno del riesgo.

**Ejercicio 7.**

a) Se comparan las filas dos a dos. Entre a₁ y a₂: a₁ es mayor en θ₁ y θ₂, pero menor en θ₃. Entre a₁ y a₃: a₁ es mayor en θ₁ y menor en θ₂ y θ₃. Entre a₂ y a₃: a₂ es mayor en θ₁ y θ₃, pero menor en θ₂. Ninguna alternativa domina a otra.

b) En esta disposición, el mínimo, el máximo y el promedio de cada alternativa se calculan **por fila**; el mejor pago de cada estado se busca **por columna**.

- Wald: `W(a_1) = min(90; 70; 55) = 55`; `W(a_2) = min(45; 35; 125) = 35`; `W(a_3) = min(25; 110; 120) = 25`. **Recomienda a₁.**
- Maximax: `M(a_1) = 90`; `M(a_2) = 125`; `M(a_3) = 120`. **Recomienda a₂.**
- Hurwicz con α = 0.5: `H(a_1) = (0.5 * 90) + (0.5 * 55) = 72.5`; `H(a_2) = (0.5 * 125) + (0.5 * 35) = 80`; `H(a_3) = (0.5 * 120) + (0.5 * 25) = 72.5`. **Recomienda a₂.**
- Laplace: `L(a_1) = (90 + 70 + 55) / 3 = 215 / 3 = 71.67`; `L(a_2) = (45 + 35 + 125) / 3 = 205 / 3 = 68.33`; `L(a_3) = (25 + 110 + 120) / 3 = 255 / 3 = 85`. **Recomienda a₃.**
- Savage: los mejores pagos por estado (por columna) son θ₁, 90; θ₂, 110; θ₃, 125. Arrepentimientos: a₁: `(90 - 90; 110 - 70; 125 - 55) = (0; 40; 70)`, mayor 70; a₂: `(90 - 45; 110 - 35; 125 - 125) = (45; 75; 0)`, mayor 75; a₃: `(90 - 25; 110 - 110; 125 - 120) = (65; 0; 5)`, mayor 65. **Recomienda a₃.**

c) Transcrita (estados en filas):

| Estado ↓ / Alternativa → | a₁ | a₂ | a₃ |
|---|---|---|---|
| θ₁ | 90 | 45 | 25 |
| θ₂ | 70 | 35 | 110 |
| θ₃ | 55 | 125 | 120 |

Con esta disposición, el mínimo y el máximo de cada alternativa se buscan por columna, y el mejor pago de cada estado por fila. Los valores y las recomendaciones son idénticos.

---

## Para la sesión 6

Se solicita presentar la matriz de pagos de la decisión propia, en papel, con la fórmula de cada celda y la lista de las alternativas que sobrevivieron, así como el valor de α proporcionado por el decisor o la forma en que se le preguntará.

En la sesión 6 se emplea el asistente de IAG con bitácora. Un uso pertinente consiste en solicitarle que explique el criterio menos comprendido mediante un ejemplo distinto y **verificar su explicación contra el contenido de esta lectura**.

---

## Para ampliar (opcional)

Las obras citadas tienen derechos reservados; se mencionan por capítulo y no se reproducen. Pueden consultarse en el [catálogo del acervo físico](https://amoxcalli.izt.uam.mx/) o en la [biblioteca digital](https://bidi.uam.mx). Los nombres de los criterios y la disposición de la matriz varían entre textos.

- Regla *max-min* y su contraste con la regla probabilística y la de certeza: Simon (1955), secciones 1.2 y 2.
- Toma de decisiones sin probabilidades, con los enfoques optimista, conservador y de arrepentimiento minimax: Anderson et al. (2016), cap. 4, sec. 4.2.
- Decisión bajo incertidumbre: Taha (2012), cap. 15, sec. 15.3.
- Criterios de decisión: Bronson (1983), cap. 17.
- Elementos del análisis de decisiones: Winston y Albright (2019), cap. 9.
- Decisiones en situación de incertidumbre: Amaya Amaya (2010), cap. 3.

## Referencias

Amaya Amaya, J. (2010). *Toma de decisiones gerenciales* (2.ª ed.). Ecoe Ediciones.
Anderson, D. R., Sweeney, D. J., Williams, T. A., Camm, J. D., Cochran, J. J., Fry, M. J., y Ohlmann, J. W. (2016). *Métodos cuantitativos para los negocios* (13.ª ed.). Cengage Learning.
Bronson, R. (1983). *Teoría y problemas de investigación de operaciones* (M. L. Fournier García, Trad.). McGraw-Hill.
Simon, H. A. (1955). A behavioral model of rational choice. *The Quarterly Journal of Economics, 69*(1), 99-118.
Taha, H. A. (2012). *Investigación de operaciones* (9.ª ed.). Pearson Educación.
Winston, W. L., y Albright, S. C. (2019). *Practical management science* (6.ª ed.). Cengage Learning.
