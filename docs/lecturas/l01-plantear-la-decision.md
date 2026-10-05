# L1 · Plantear la decisión

**Temas:** 1.4 (tipología de los problemas de decisión); 2.1 a 2.3 (elementos del problema, matriz de pagos y dominación)
**Sesiones que la utilizan:** 5 y 6 · **Lectura previa a la sesión 5 (lunes 5 de octubre)**
**Tiempo estimado de lectura:** 30 minutos

**prof. dr. Jesús Zavala Ruiz** · Universidad Autónoma Metropolitana, Unidad Iztapalapa
**Última actualización:** 5 de octubre de 2026
Material de elaboración propia, publicado bajo licencia [Creative Commons Atribución-CompartirIgual 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Los ejemplos y ejercicios son originales y sus resultados se verificaron mediante un programa antes de su publicación.

> «…reemplazar la racionalidad global del hombre económico…»
> Simon (1955, p. 99, traducción libre)

---

## 1. Introducción

Por lo general, quien debe tomar una decisión se plantea de inmediato la pregunta de cuál alternativa le conviene, y pasa por alto una pregunta previa y mucho más importante: ¿cuál es, exactamente, el problema que está decidiendo? Una decisión mal planteada no se corrige con un tratamiento matemático riguroso. De hecho, cuando las alternativas se traslapan, cuando se omite la opción de no actuar o cuando se confunde lo que el decisor controla con lo que no controla, la matriz resultante puede ser formalmente impecable y, sin embargo, carecer de utilidad para quien tiene que decidir.

Esta lectura se ocupa, por lo tanto, del **planteamiento** de la decisión, que es el trabajo que cada equipo realiza en la sesión 5 con la decisión real que obtuvo del decisor. En primer lugar, se introduce la tipología de los problemas de decisión y se explica en qué consiste la incertidumbre, que es el terreno del proyecto P1. En segundo lugar, se describen los cuatro elementos de todo problema de decisión y los requisitos que deben cumplir. Enseguida, se construye la matriz de pagos a partir de un ejemplo que se retoma a lo largo de la lectura, con el desarrollo de cada celda. Después, se define la dominación y se explica por qué permite eliminar alternativas sin necesidad de probabilidades. Al final se presentan una lista de comprobación, las conclusiones y seis ejercicios con sus respuestas.

Al concluir la lectura, el estudiante será capaz de: (1) clasificar una decisión como de certeza, riesgo, incertidumbre o conflicto, e indicar qué información modificaría su clasificación; (2) identificar al decisor, las alternativas, los estados de la naturaleza y las consecuencias, y reconocer los errores de planteamiento más frecuentes; (3) calcular cada celda de una matriz de pagos, mostrando la fórmula empleada; y (4) determinar si una alternativa está dominada y eliminarla con una justificación explícita.

---

## 2. Convenciones de notación

Los números se escriben con la notación usual en México: la **coma** separa los millares y el **punto** separa la parte decimal. Así, *treinta y cinco mil cuatrocientos* se escribe 35,400 y *cuarenta por ciento* se escribe 0.40 o 40 %. Cuando se enumeran varios valores dentro de una fórmula, se separan con **punto y coma**, para no confundirlos con los millares: `min(26,000; 36,000; 46,000)`.

Cada fórmula se presenta de tres maneras complementarias: (1) en **notación algebraica de una línea**, con `*` para la multiplicación y `/` para la división, y con paréntesis que hacen explícito el orden de las operaciones; (2) con su **desarrollo numérico**, paso a paso, hasta el resultado; y (3) en **notación LaTeX**, para la lectura en el sitio del curso. Las cantidades monetarias se expresan siempre en pesos y con signo, es decir, una pérdida es un número negativo.

---

## 3. Tipología de las decisiones

Decidir consiste en elegir una acción entre varias posibles. Lo que distingue un problema de otro no es tanto su magnitud como **cuánto se sabe** acerca de lo que ocurrirá después de elegir. Con este criterio se reconocen cuatro tipos de decisión, que se resumen a continuación.

| Tipo | Conocimiento del futuro | Ejemplo |
|---|---|---|
| **Certeza** | Se sabe con seguridad qué estado ocurrirá | Un taquero sabe que mañana atenderá una boda de 150 invitados y decide cuánta carne comprar |
| **Riesgo** | Pueden ocurrir varios estados y se conoce, o puede estimarse, su probabilidad | Una papelería con cinco años de ventas diarias registradas decide cuántos cuadernos pedir |
| **Incertidumbre** | Pueden ocurrir varios estados y no existe fundamento para asignarles probabilidades | Una cooperativa decide si siembra un cultivo que nadie en la región ha probado |
| **Conflicto** | El resultado depende de lo que decida otra persona con intereses opuestos | Dos gasolineras vecinas fijan su precio, cada una considerando la reacción de la otra |

Cabe hacer dos precisiones. La primera es que **los autores no siempre emplean los términos con el mismo sentido**: algunos textos denominan «riesgo» o «incertidumbre» a situaciones distintas de las que aquí se describen. En este curso se adoptan las definiciones de la tabla y se recomienda, al consultar otra fuente, verificar primero cómo define cada término.

La segunda precisión es más importante: **el tipo de decisión depende de lo que sabe el decisor, y no solo del problema**. Una misma decisión pasa de la incertidumbre al riesgo cuando se obtiene información; si la papelería del ejemplo no llevara registros, claramente se encontraría en incertidumbre. Esta observación estructura el curso, pues en el proyecto P1 se decide **sin** probabilidades (incertidumbre), en P2 se incorporan (riesgo) y en P3 se evalúa si conviene adquirir información adicional.

El conflicto, en el que otro decisor reacciona, corresponde a la teoría de juegos, que queda fuera del alcance de esta UEA. En consecuencia, las decisiones que se analizan en el curso son las de **una sola persona u organización** que decide ante circunstancias que no controla.

---

## 4. Elementos del problema de decisión

Todo problema de decisión, cualquiera que sea su magnitud, se describe mediante cuatro elementos. El primero es **el decisor**, quien elige y asume las consecuencias, y que debe tener nombre o cargo y ser localizable para consultas posteriores. El segundo son **las alternativas** (también llamadas acciones u opciones), es decir, las acciones entre las cuales se elige. El tercero son **los estados de la naturaleza** (*states of nature*), las circunstancias que el decisor no controla y que influyen en el resultado. El cuarto son **las consecuencias** (o pagos), lo que le ocurre al decisor para cada combinación de alternativa y estado.

### 4.1 Ejemplo que se utiliza en el resto de la lectura

Marisol elabora bisutería con chaquira. El próximo fin de semana se celebra la feria del pueblo y debe decidir, ese mismo día, de qué manera participará. La asistencia a la feria puede ser baja, media o alta, y no depende de ella. Si instala un puesto propio, estima ventas de 1,500 pesos con asistencia baja, 3,000 con asistencia media y 5,000 con asistencia alta. Los materiales le cuestan el 40 % de lo que vende y la renta del puesto es de 1,200 pesos.

Los cuatro elementos se identifican como sigue:

| Elemento | En el ejemplo |
|---|---|
| Decisor | Marisol |
| Alternativas | a₁: puesto propio · a₂: compartir un puesto con una amiga, por mitades · a₃: no participar · a₄: puesto propio en una esquina de poca circulación |
| Estados de la naturaleza | θ₁: asistencia baja · θ₂: asistencia media · θ₃: asistencia alta |
| Consecuencias | Ganancia neta del fin de semana, en pesos |

### 4.2 Requisitos de las alternativas

Las alternativas deben ser **exhaustivas** y **excluyentes**. Que sean exhaustivas significa que no debe quedar fuera ninguna acción que el decisor pudiera efectivamente emprender; por lo general, esto obliga a incluir **«no hacer nada»** o «dejar todo como está», que en el ejemplo es a₃. Que sean excluyentes significa que elegir una debe descartar las demás. Así, «colocar un anuncio» y «colocar un anuncio en redes sociales» no son excluyentes, porque la segunda es un caso particular de la primera.

### 4.3 Requisitos de los estados de la naturaleza

Los estados también deben ser exhaustivos y excluyentes y, sobre todo, **independientes de lo que decida el decisor**. Si el estado varía según la alternativa elegida, no es un estado: es una consecuencia, o una alternativa disfrazada.

Un error frecuente consiste en proponer como estados «ventas altas», «ventas medias» y «ventas bajas». Sin embargo, las ventas de Marisol sí dependen de sus decisiones (dónde instala el puesto, si baja sus precios, si lo comparte), mientras que lo que no depende de ella es la **asistencia a la feria**. Las ventas resultan de combinar alternativa y estado y son, por tanto, una consecuencia. Una prueba sencilla consiste en preguntar: *¿puede el decisor modificar esto eligiendo otra alternativa?* Si la respuesta es afirmativa, no se trata de un estado de la naturaleza.

### 4.4 Requisitos de las consecuencias

Cada combinación de alternativa y estado debe producir una consecuencia **expresable en pesos**. Si no puede cuantificarse, la decisión no es admisible para este curso, aunque los criterios no monetarios tienen su lugar y se tratan por separado en la lectura L2.

---

## 5. La matriz de pagos

### 5.1 Notación

Sean $\theta_1, \theta_2, \dots, \theta_m$ los $m$ estados de la naturaleza y $a_1, a_2, \dots, a_n$ las $n$ alternativas. La **función de consecuencias** asigna a cada par (estado, alternativa) un pago, que se denota

$$c_{ij} = \text{pago de la alternativa } a_j \text{ cuando ocurre el estado } \theta_i$$

La **matriz de pagos** (*payoff matrix*) es la tabla que reúne estos valores. En esta lectura, y en las demás del curso, se adopta la siguiente disposición: los **estados de la naturaleza** $\theta_i$ ocupan las **filas** (el índice $i$ recorre las filas), las **alternativas** $a_j$ ocupan las **columnas** (el índice $j$ recorre las columnas) y la celda $c_{ij}$ se ubica en el cruce de la fila $i$ con la columna $j$.

Es indispensable señalar que, según el autor, la disposición puede invertirse: algunos textos colocan las alternativas en las filas y los estados de la naturaleza en las columnas. La información contenida es la misma y las conclusiones no cambian; lo que sí cambia es el sentido en que se recorre la tabla al aplicar un criterio. Por ejemplo, el mínimo de cada alternativa se busca por *columna* en la disposición de esta lectura y por *fila* en la disposición inversa. Por lo tanto, es necesario identificar la convención antes de calcular. En el ejercicio 5 se practica con la disposición inversa.

### 5.2 Reglas para su construcción

La construcción de la matriz obedece a cuatro reglas. En primer lugar, cada celda se acompaña de su **fórmula**, escrita con los datos del decisor, y a continuación de su resultado. En segundo lugar, los pagos se expresan **en pesos y con signo**. En tercer lugar, todas las celdas se refieren a la **misma unidad y al mismo periodo** (en el ejemplo, pesos por fin de semana). Y en cuarto lugar, las celdas que dependen de un dato **supuesto por el equipo** se marcan con un asterisco (\*), y el supuesto se explica al pie de la tabla.

### 5.3 Cálculo de las celdas del ejemplo

Sea $V_i$ el monto de las ventas bajo el estado $\theta_i$: $V_1 = 1{,}500$, $V_2 = 3{,}000$ y $V_3 = 5{,}000$ pesos.

**Alternativa a₁ (puesto propio).** El pago es la venta, menos el costo de los materiales, menos la renta.

Notación algebraica: `c_i1 = V_i - 0.40 * V_i - 1,200 = (1 - 0.40) * V_i - 1,200`

$$c_{i1} = V_i - 0.40\,V_i - 1{,}200 = (1 - 0.40)\,V_i - 1{,}200$$

Desarrollo:

- `c_11 = (1 - 0.40) * 1,500 - 1,200 = 0.60 * 1,500 - 1,200 = 900 - 1,200 = -300`
- `c_21 = (1 - 0.40) * 3,000 - 1,200 = 0.60 * 3,000 - 1,200 = 1,800 - 1,200 = 600`
- `c_31 = (1 - 0.40) * 5,000 - 1,200 = 0.60 * 5,000 - 1,200 = 3,000 - 1,200 = 1,800`

**Alternativa a₂ (compartir).** Marisol y su amiga dividen por mitades el margen y la renta.

Notación algebraica: `c_i2 = 0.5 * ((1 - 0.40) * V_i) - 0.5 * 1,200`

$$c_{i2} = 0.5\,\bigl[(1 - 0.40)\,V_i\bigr] - 0.5\,(1{,}200)$$

Desarrollo:

- `c_12 = 0.5 * ((1 - 0.40) * 1,500) - 0.5 * 1,200 = 0.5 * 900 - 600 = 450 - 600 = -150`
- `c_22 = 0.5 * ((1 - 0.40) * 3,000) - 0.5 * 1,200 = 0.5 * 1,800 - 600 = 900 - 600 = 300`
- `c_32 = 0.5 * ((1 - 0.40) * 5,000) - 0.5 * 1,200 = 0.5 * 3,000 - 600 = 1,500 - 600 = 900`

**Alternativa a₃ (no participar).** No hay ingreso ni gasto: `c_i3 = 0` para $i = 1, 2, 3$.

**Alternativa a₄ (esquina de poca circulación).** Se paga la misma renta, pero las ventas equivalen al 60 % de las de a₁.

Notación algebraica: `c_i4 = 0.60 * ((1 - 0.40) * V_i) - 1,200`

$$c_{i4} = 0.60\,\bigl[(1 - 0.40)\,V_i\bigr] - 1{,}200$$

Desarrollo:

- `c_14 = 0.60 * ((1 - 0.40) * 1,500) - 1,200 = 0.60 * 900 - 1,200 = 540 - 1,200 = -660`
- `c_24 = 0.60 * ((1 - 0.40) * 3,000) - 1,200 = 0.60 * 1,800 - 1,200 = 1,080 - 1,200 = -120`
- `c_34 = 0.60 * ((1 - 0.40) * 5,000) - 1,200 = 0.60 * 3,000 - 1,200 = 1,800 - 1,200 = 600`

### 5.4 Matriz resultante

Pagos en pesos por fin de semana.

| Estado ↓ / Alternativa → | a₁ · Puesto propio | a₂ · Compartir | a₃ · No participar | a₄ · Esquina de poca circulación |
|---|---|---|---|---|
| θ₁ · Asistencia baja | −300 | −150 | 0 | −660 |
| θ₂ · Asistencia media | 600 | 300 | 0 | −120 |
| θ₃ · Asistencia alta | 1,800 | 900 | 0 | 600 |

Sin aplicar todavía ningún criterio de decisión, la matriz permite observar que la alternativa a₄ no conviene en ningún estado. Este hecho se formaliza en la sección siguiente.

---

## 6. Dominación y alternativas admisibles

Se dice que la alternativa $a_k$ **domina** a la alternativa $a_j$ cuando $a_k$ produce un pago **mayor o igual** que $a_j$ en **todos** los estados, y un pago **estrictamente mayor** en **al menos un** estado. En notación formal:

$$a_k \text{ domina a } a_j \iff \bigl(c_{ik} \geq c_{ij} \ \text{ para todo } i\bigr) \ \text{ y } \ \bigl(c_{ik} > c_{ij} \ \text{ para al menos un } i\bigr)$$

En la disposición adoptada, la verificación consiste en comparar **dos columnas**, celda por celda, de arriba hacia abajo. Si $a_k$ domina a $a_j$, ningún decisor que desee obtener más escogería $a_j$, pues $a_k$ es igual o mejor sin importar qué estado ocurra. La alternativa $a_j$ se denomina entonces **dominada** y se elimina; las restantes son las **alternativas admisibles**.

En el ejemplo, a₁ domina a a₄:

| Estado | Pago de a₁ | Pago de a₄ | ¿a₁ > a₄? |
|---|---|---|---|
| θ₁ | −300 | −660 | Sí |
| θ₂ | 600 | −120 | Sí |
| θ₃ | 1,800 | 600 | Sí |

La alternativa a₂ también domina a a₄, pero basta una para justificar la eliminación. Marisol puede suprimir la columna a₄ y conservar tres alternativas admisibles.

Deben tenerse presentes tres puntos. Primero, **la dominación no requiere probabilidades**: es el primer filtro y se aplica aunque nada se sepa del futuro. Segundo, **perder en un estado no equivale a estar dominada**. Entre a₂ y a₃, la segunda es mejor si la asistencia es baja (0 contra −150) pero peor si es media o alta; ninguna domina a la otra y ambas son admisibles. Tercero, **cada eliminación se documenta estado por estado**, pues una expresión como «era peor» no constituye una justificación. Cuando ninguna alternativa resulta dominada, el resultado es igualmente válido: se escribe «ninguna alternativa queda dominada» y se muestra la comparación que lo sustenta.

---

## 7. Lista de comprobación previa al cálculo

Las siguientes preguntas son las que los equipos se formularán entre sí al revisar las fichas, en la sesión 5. Conviene responderlas, para la decisión propia, antes de asistir:

1. ¿Quién decide? ¿Está identificado por nombre o cargo y puede consultarse de nuevo?
2. ¿Las alternativas son **exhaustivas** (incluyen «no hacer nada» cuando procede) y **excluyentes**?
3. ¿Los estados de la naturaleza **no dependen** de lo que decida el decisor? ¿Alguno es, en realidad, una alternativa disfrazada?
4. ¿Cada cruce de estado y alternativa produce una consecuencia expresable en pesos?
5. ¿Hasta cuándo debe decidir el decisor y cuándo se conocerá el estado de la naturaleza?
6. ¿Qué dato falta y a quién debe solicitarse?

---

## 8. Conclusiones

Quedó claro que plantear una decisión es una tarea previa al cálculo y que de ella depende la utilidad de todo lo que sigue. Una decisión se clasifica según lo que se sabe del futuro y no solo según el problema, de modo que la misma situación puede pasar de la incertidumbre al riesgo cuando se consigue información. Todo planteamiento requiere un decisor localizable, alternativas exhaustivas y excluyentes (con la opción de no actuar cuando procede), estados de la naturaleza que el decisor no controla y consecuencias expresables en pesos.

La matriz de pagos reúne esas consecuencias en una tabla en la que cada celda debe poder justificarse con una fórmula. En este curso se dispone con los estados en las filas y las alternativas en las columnas, pero lo esencial es identificar la convención del autor antes de recorrer la tabla. Finalmente, la dominación permite eliminar alternativas sin probabilidades y es, por lo tanto, el primer filtro. Con las alternativas admisibles en la mano, el siguiente paso es reducirlas y valorarlas con criterios que no se expresan en pesos, lo cual se aborda en la lectura L2.

---

## 9. Ejercicios

Se recomienda resolverlos antes de consultar las respuestas.

**Ejercicio 1.** Clasifique cada enunciado como *alternativa*, *estado de la naturaleza* o *consecuencia*, y justifique:

a) «Que llueva el sábado de la feria».
b) «Contratar a un ayudante para la feria».
c) «Obtener una ganancia de 450 pesos».
d) «Vender mucho porque se bajaron los precios».

**Ejercicio 2.** Clasifique cada situación como de certeza, riesgo, incertidumbre o conflicto:

a) Un restaurante tiene confirmada una reservación de 40 personas para mañana y decide cuántas mesas armar.
b) Una tienda de abarrotes decide cuánto pan pedir con base en las ventas diarias de los últimos tres años.
c) Un taller de costura decide si abre una línea de ropa deportiva en un mercado donde nunca ha vendido y del que carece de datos.
d) Dos taquerías ubicadas frente a frente fijan cada una su precio, considerando cómo reaccionará la otra.

**Ejercicio 3.** Escriba la fórmula, con su desarrollo, de la celda $c_{32}$ del ejemplo (compartir el puesto con asistencia alta), en notación algebraica.

**Ejercicio 4.** Determine si alguna alternativa domina a otra en la siguiente matriz (pagos en pesos):

| Estado ↓ / Alternativa → | X | Y | Z |
|---|---|---|---|
| θ₁ | 10 | 10 | 5 |
| θ₂ | 20 | 25 | 40 |
| θ₃ | 30 | 30 | 20 |

**Ejercicio 5 (disposición inversa).** Una fuente presenta la siguiente matriz de pagos con las **alternativas en las filas** y los **estados de la naturaleza en las columnas** (pagos en miles de pesos):

| Alternativa ↓ / Estado → | θ₁ | θ₂ | θ₃ |
|---|---|---|---|
| a₁ | 12 | 18 | 24 |
| a₂ | 15 | 18 | 30 |
| a₃ | 20 | 10 | 40 |

a) Transcriba la matriz a la disposición de esta lectura (estados en filas y alternativas en columnas).
b) Determine si alguna alternativa domina a otra. Indique si, en la disposición original, la comparación se hace entre filas o entre columnas.

---

## Respuestas para verificar

**Ejercicio 1.**
a) *Estado de la naturaleza:* el decisor no controla el clima.
b) *Alternativa:* es una acción que el decisor puede elegir.
c) *Consecuencia:* es un resultado expresado en pesos.
d) *Consecuencia:* depende de una acción del decisor (bajar los precios) y no puede considerarse un estado.

**Ejercicio 2.**
a) *Certeza:* se sabe qué estado ocurrirá.
b) *Riesgo:* existen registros a partir de los cuales estimar probabilidades.
c) *Incertidumbre:* hay varios estados posibles y ninguna base para asignarles probabilidades.
d) *Conflicto:* el resultado de cada una depende de la decisión de la otra.

**Ejercicio 3.**

`c_32 = 0.5 * ((1 - 0.40) * 5,000) - 0.5 * 1,200 = 0.5 * (0.60 * 5,000) - 600 = 0.5 * 3,000 - 600 = 1,500 - 600 = 900`

$$c_{32} = 0.5\,\bigl[(1 - 0.40)(5{,}000)\bigr] - 0.5\,(1{,}200) = 1{,}500 - 600 = 900 \text{ pesos}$$

**Ejercicio 4.** **Y domina a X:** los pagos coinciden en θ₁ y θ₃ (10 y 30), y Y es estrictamente mayor en θ₂ (25 contra 20). La alternativa Z no domina a ninguna ni es dominada: es mejor en θ₂ (40), pero peor en θ₁ y θ₃. Las alternativas admisibles son Y y Z.

**Ejercicio 5.**

a) Matriz transcrita (miles de pesos):

| Estado ↓ / Alternativa → | a₁ | a₂ | a₃ |
|---|---|---|---|
| θ₁ | 12 | 15 | 20 |
| θ₂ | 18 | 18 | 10 |
| θ₃ | 24 | 30 | 40 |

b) **a₂ domina a a₁:** es mayor en θ₁ (15 > 12), igual en θ₂ (18 = 18) y mayor en θ₃ (30 > 24). La alternativa a₃ no domina a ninguna ni es dominada, pues es mayor en θ₁ y θ₃ pero menor en θ₂. En la disposición original, la comparación se realiza entre **filas** (a₁ con a₂); en la de esta lectura, entre **columnas**. El resultado es el mismo.

---

## Para la sesión 5

Se solicita presentar la ficha de la decisión, con las seis preguntas de la sección 7 respondidas, y la lista de los datos que aún faltan al equipo.

---

## Para ampliar (opcional)

Las obras citadas tienen derechos reservados; se mencionan por capítulo y no se reproducen. Pueden consultarse en el [catálogo del acervo físico](https://amoxcalli.izt.uam.mx/) o en la [biblioteca digital](https://bidi.uam.mx).

- Tipología de las decisiones: Amaya Amaya (2010), cap. 2.
- Formulación del problema y matrices de pago: Anderson et al. (2016), cap. 4, sec. 4.1.
- Elementos del análisis de decisiones: Winston y Albright (2019), cap. 9, sec. 9.2.
- Proceso y teoría de decisiones: Bronson (1983), cap. 17.

## Referencias

Amaya Amaya, J. (2010). *Toma de decisiones gerenciales* (2.ª ed.). Ecoe Ediciones.
Anderson, D. R., Sweeney, D. J., Williams, T. A., Camm, J. D., Cochran, J. J., Fry, M. J., y Ohlmann, J. W. (2016). *Métodos cuantitativos para los negocios* (13.ª ed.). Cengage Learning.
Bronson, R. (1983). *Teoría y problemas de investigación de operaciones* (M. L. Fournier García, Trad.). McGraw-Hill.
Simon, H. A. (1955). A behavioral model of rational choice. *The Quarterly Journal of Economics, 69*(1), 99–118. https://doi.org/10.2307/1884852
Winston, W. L., y Albright, S. C. (2019). *Practical management science* (6.ª ed.). Cengage Learning.
