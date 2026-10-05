### Ejemplo: Despido del tesorero

Fuente: Bronson, R. (1983). *Teoría y problemas de investigación de operaciones* (Problema 17.22, p. 208). México: McGraw-Hill.

Resuelto por el prof. J. Zavala

La presidenta de una compañía de una rama industrial altamente competitiva considera que un empleado de la compañía está proporcionando información confidencial a la competencia. Está 90% segura de que este informante es el tesorero de la compañía, cuyos contactos han sido extremadamente valiosos para obtener financiamiento para la empresa. Si lo despide y resulta ser el informante, la compañía gana \$100,000. Si lo despide pero no es el informante, la compañía pierde su experiencia y aún tiene un informante en el equipo, con una pérdida para la compañía de \$500,000. Si ella no despide al tesorero, la compañía pierde \$300,000, sea o no el informante, ya que en ambos casos el informante sigue en la compañía.

Antes de decidir la suerte del tesorero, la presidenta podría ordenar pruebas con el detector de mentiras. Para evitar posibles demandas, estas pruebas tendrían que administrarse a todos los empleados de la compañía, con un costo total de \$30,000. Otro problema es que las pruebas con detector de mentiras no son definitivas. Si una persona está mintiendo, la prueba lo revelará el 90% de las veces; pero si una persona no está mintiendo, la prueba lo indicará solo el 70% de las veces.

¿Qué acciones deberá tomar la presidenta de la compañía?

---
### *Solución*

### Fase 0. Encuadre del Problema

El **encuadre del problema** define los elementos o *datos clave* del problema de decisión que influyen en la elección de la mejor alternativa en un contexto de incertidumbre. El encuadre del problema incluye los siguientes elementos del análisis de decisión: 

#### **1. Decisor**

¿*Quién toma la decisión* y cuál es su objetivo principal?

El decisor es central porque sus acciones influirán directamente en el resultado económico de la compañía. Su meta es tomar una decisión que sea óptima bajo condiciones de incertidumbre.

- **Decisor**: La presidenta de la compañía es quien toma la decisión.  
- Su **objetivo** principal es minimizar las pérdidas económicas derivadas de la filtración de información confidencial. Esto implica balancear los costos asociados con despedir al tesorero (quien podría ser inocente o culpable), los riesgos de mantenerlo y el costo de usar un detector de mentiras para confirmar la situación.

#### **2. Acciones o decisiones ($a_j$)**

¿Qué *opciones* están disponibles para el decisor?

Las acciones o decisiones representan las alternativas disponibles para la presidenta. Estas alternativas deben ser evaluadas considerando las posibles consecuencias económicas de cada una, en combinación con los estados de la naturaleza.

- **Decisión 1 ($a_1$)**: Despedir al tesorero sin realizar pruebas.
- **Decisión 2 ($a_2$)**: No despedir al tesorero.
- **Decisión 3 ($a_3$)**: Realizar pruebas con el detector de mentiras antes de decidir.

#### **3. Estados de la naturaleza ($\theta_i$)**

¿Cuáles son las *condiciones fuera del control del decisor* que afectan el resultado?

Los estados de la naturaleza son escenarios que determinan el resultado de las decisiones tomadas. El decisor no tiene control directo sobre cuál estado es verdadero, pero puede asignar probabilidades a cada estado basándose en la información disponible (e.g., la presidenta está 90% segura de que el tesorero es el informante).

- **Estado 1 ($\theta_1$)**: El tesorero es el informante.
- **Estado 2 ($\theta_2$)**: El tesorero no es el informante.


#### **4. Función de utilidad (U($\theta, a$)) y matriz de pagos**
**¿Cuáles son las consecuencias asociadas con cada combinación de estados de la naturaleza y decisiones?**

La **función de utilidad** (U($\theta, a$)) evalúa el valor (económico en este caso) de cada decisión ($a_j$) bajo un estado de la naturaleza específico ($\theta_i$).

**Matriz de pagos**:
Esta matriz organiza las ganancias o pérdidas económicas para cada combinación de $a_j$ y $\theta_i$:

Aquí está la matriz con las filas y columnas intercambiadas:

| **Estado ($\theta_i$) / Acción ($a_j$)** | **$a_1$: Despedir al tesorero** | **$a_2$: No despedir al tesorero** | **$a_3$: Realizar pruebas** |
|---------------------------------------------|----------------------------------|----------------------------------|---------------------------------------------------------------|
| **$\theta_1$: El tesorero es el informante** | $+100,000$                      | $-300,000$                      | Depende del resultado de las pruebas (ver análisis más abajo). |
| **$\theta_2$: El tesorero no es el informante** | $-500,000$                      | $-300,000$                      | Depende del resultado de las pruebas (ver análisis más abajo). |

Este formato presenta los estados de la naturaleza en las filas y las acciones en las columnas.**Cálculo adicional para $a_3$: Realizar pruebas**:
Las pruebas introducen complejidad debido a su falta de precisión:
- Si el tesorero está mintiendo ($\theta_1$):
  - Probabilidad de detectar mentira correctamente: $90$%.
  - Probabilidad de no detectar mentira: %10$%.
- Si el tesorero no está mintiendo ($\theta_2$):
  - Probabilidad de detectar verdad correctamente: $70$%.
  - Probabilidad de error: $30$%.

Para evaluar $a_3$, necesitaríamos calcular el valor esperado, incorporando los costos de las pruebas (\$30,000) y las probabilidades de error del detector.

La matriz de pagos proporciona una representación clara de los resultados posibles, permitiendo comparar las decisiones. Para acciones con incertidumbre (como $a_3$), se deben incluir cálculos adicionales basados en probabilidades condicionales y costos, tal como se analizará en la Fase 3.

#### **Resumen del Encuadre**
- El decisor es la presidenta, cuyo objetivo es minimizar las pérdidas económicas.
- Las decisiones disponibles son: despedir al tesorero, no despedirlo o realizar pruebas con el detector de mentiras.
- Los estados de la naturaleza son: el tesorero es el informante o no lo es.
- La matriz de pagos organiza las posibles ganancias o pérdidas económicas, dependiendo de la combinación de decisiones y estados de la naturaleza. En el caso de realizar pruebas, se debe incorporar un análisis probabilístico adicional.

---

### **Fase 1: Análisis de Decisiones Bajo Riesgo**

**Nota:** El análisis de decisiones bajo riesgo se utiliza cuando no se dispone de información probabilística. Sin embargo, en este caso ya tenemos probabilidades asignadas (*a priori*) ($P(\theta_1) = 0.9$ (90% de certeza de que el tesorero es el informante)), por lo que **estos criterios no se aplican** a este problema. Aún así, los mostramos para recordar el algoritmo de cálculo.

#### **1: Construcción de la Matriz de Pagos**  

Primero, organizamos los datos del problema en la **matriz de pagos**, que representa las ganancias o pérdidas para cada decisión dependiendo de si el tesorero es o no el informante.

| **Estado ($\theta_i$) / Acción ($a_j$)** | **$a_1$: Despedir al tesorero** | **$a_2$: No despedir al tesorero** |
|---------------------------------------------|----------------------------------|----------------------------------|
| **$\theta_1$: El tesorero ES el informante ($90\%$)** | $+100,000$                      | $-300,000$                      |
| **$\theta_2$: El tesorero NO es el informante ($10\%$)** | $-500,000$                      | $-300,000$                      |

Aplicaremos **cuatro criterios** para evaluar cuál es la mejor acción sin usar probabilidades.

#### **2. Criterio Maximin (Pesimista)**  

Este criterio elige la opción que garantiza la **mejor ganancia mínima posible**. Se basa en un enfoque conservador que asume que ocurrirá el peor escenario.  

1. **Identificamos la peor ganancia de cada acción:**  
   - Para **$a_1$: Despedir al tesorero**, el peor caso es **$-500,000$**.  
   - Para **$a_2$: No despedir al tesorero**, el peor caso es **$-300,000$**.  

2. **Seleccionamos la opción con la mejor de estas peores ganancias:**  
   $\max (-500,000, -300,000) = -300,000$

3. **Decisión** según **Maximin**

   No despedir al tesorero ($a_2$), porque la peor pérdida es menor.


#### **3. Criterio Maximax (Optimista)**  

Este criterio elige la acción con el **mejor resultado posible**, asumiendo el mejor de los casos.  

1. **Identificamos la mejor ganancia de cada acción:**  
- Para **$a_1$: Despedir al tesorero**, la mejor ganancia es **$100,000$**.  
- Para **$a_2$: No despedir al tesorero**, la mejor ganancia es **$-300,000$** (ya que no cambia entre estados de la naturaleza).  

2. **Seleccionamos la acción con la mayor ganancia:**  
   $\max (100,000, -300,000) = 100,000$, que corresponde a $a_1$.

3. *Decisión según Maximax**:

   Despedir al tesorero ($a_1$), porque el mejor caso es más favorable.


#### **4. Criterio de Hurwicz (Optimismo-Pesimismo)**  

Este criterio es un **balance** entre el optimismo y el pesimismo. Utiliza un coeficiente $\alpha$ (entre $0$ y $1$) que representa el **grado de optimismo** del decisor.  

1. **Supongamos** que el decisor elige $\alpha = 0.6$ (es decir, **60% optimista y 40% pesimista**).

2. **Calculamos el valor de Hurwicz para cada acción:**  

   $H(a_1) = (0.6)(100,000) + (0.4)(-500,000) = 60,000 - 200,000 = -140,000$

   $H(a_2) = (0.6)(-300,000) + (0.4)(-300,000) = -180,000 - 120,000 = -300,000$

3. **Seleccionamos la acción con el mayor valor de Hurwicz:**  

   $\max (-140,000, -300,000) = -140,000$, que corresponde a $a_1$.

4. **Decisión según Hurwicz**:

   Despedir al tesorero ($a_1$), porque su balance entre optimismo y pesimismo es mejor.


#### **5. Criterio de Savage (Minimax de Pesar)**  

Este criterio minimiza el **arrepentimiento máximo** que podría sentir el decisor por no haber elegido la mejor opción.  

1. **Construimos la Matriz de Pérdida de Oportunidad**  
   - Para cada estado de la naturaleza, identificamos la mejor ganancia.  
   - Luego, calculamos la **pérdida de oportunidad** de cada acción restando su ganancia de la mejor ganancia en esa columna.

| **Acción ($a_j$) / Estado ($\theta_i$)** | **$\theta_1$: Tesorero ES informante** | **$\theta_2$: Tesorero NO es informante** |
|---------------------------------------------|--------------------------------|--------------------------------|
| **$a_1$: Despedir al tesorero**           | $0$                          | $500,000 - (-500,000) = 600,000$ |
| **$a_2$: No despedir al tesorero**        | $100,000 - (-300,000) = 400,000$ | $0$ |

2. **Identificamos el máximo pesar para cada acción:**  
   - Para **$a_1$**, el máximo pesar es **$600,000$**.  
   - Para **$a_2$**, el máximo pesar es **$400,000$**.  

3. **Seleccionamos la acción con el menor de estos máximos:**  
   $\min (600,000, 400,000) = 400,000$, que corresponde a $a_2$.

4. **Decisión según Savage**:

   No despedir al tesorero ($a_2$), porque minimiza el arrepentimiento máximo.

#### **6. Conclusión de la Fase 1**   

| **Criterio de Decisión** | **Decisión Óptima** |
|----------------------|----------------------|
| **Maximin (Pesimista)** | **No despedir ($a_2$)** |
| **Maximax (Optimista)** | **Despedir ($a_1$)** |
| **Hurwicz ($\alpha = 0.6$)** | **Despedir ($a_1$)** |
| **Savage (Minimax de pesar)** | **No despedir ($a_2$)** |

**Conclusión general:**  
- Si la presidenta **es conservadora** y quiere minimizar el peor caso, **NO despedirá al tesorero ($a_2$)**.  
- Si la presidenta **es optimista y busca la mejor ganancia posible**, **DESPEDIRÁ al tesorero ($a_1$)**.  
- Si busca un **balance entre optimismo y pesimismo**, con un **coeficiente de 0.6**, **DESPEDIRÁ al tesorero ($a_1$)**.  
- Si quiere **minimizar su posible arrepentimiento**, **NO despedirá al tesorero ($a_2$)**.

Para una **decisión más informada**, debemos considerar **las probabilidades** en la **Fase 2** y analizar el **Valor Esperado Medio (VEM)**. Esto nos permitirá evaluar qué acción tiene un rendimiento esperado mejor cuando incorporamos la probabilidad de que el tesorero sea el informante. 

---

### Fase 2: Análisis de Decisiones Bajo Riesgo Sin Experimentación

Esta fase evalúa las decisiones disponibles sin considerar información adicional, es decir, sin la aplicación del detector de mentiras. Se trabaja con las probabilidades asignadas *a priori* y se aplican diferentes criterios de decisión para identificar la mejor opción.

#### **1: Matriz de Pagos**

La matriz de pagos describe las posibles consecuencias económicas de cada acción en función del estado de la naturaleza y se complementa con la probabilidad de cada estado. 

| **Estado ($\theta_i$) / Acción ($a_j$)** | **$a_1$: Despedir al tesorero** | **$a_2$: No despedir al tesorero** | **$P(\theta_i)$** |
|---------------------------------------------|----------------------------------|----------------------------------|----------------|
| **$\theta_1$: El tesorero ES el informante** | $+100,000$                      | $-300,000$                      | $0.9$ |
| **$\theta_2$: El tesorero NO es el informante** | $-500,000$                      | $-300,000$                      | $0.1$ |

La columna $P(\theta_i)$ muestra las probabilidades asociadas a cada estado de la naturaleza, donde:
- $P(\theta_1) = 0.9$ (90% de certeza de que el tesorero es el informante).
- $P(\theta_2) = 0.1$ (10% de certeza de que el tesorero no es el informante).

Esta tabla será la base para la aplicación de los criterios de decisión probabilísticos.

### **2. Criterio de Laplace (Principio de Indiferencia)**  

**Nota:** El **Criterio de Laplace** se utiliza cuando no se dispone de información probabilística y se asume que cada estado de la naturaleza tiene la **misma probabilidad**. Sin embargo, en este caso ya tenemos probabilidades asignadas (*a priori*) ($P(\theta_1) = 0.9$ (90% de certeza de que el tesorero es el informante)), por lo que **este criterio no se aplica** en esta situación. Aún así, lo mostramos para recordar el algoritmo de cálculo.

Se utiliza la matriz de pagos original, asignándole probabilidades iguales:

| **Estado ($\theta_i$) / Acción ($a_j$)** | **$a_1$: Despedir al tesorero** | **$a_2$: No despedir al tesorero** | **$P(\theta_i)$** |
|---------------------------------------------|----------------------------------|----------------------------------|----------------|
| **$\theta_1$: El tesorero ES el informante** | $+100,000$                      | $-300,000$                      | $0.5$ |
| **$\theta_2$: El tesorero NO es el informante** | $-500,000$                      | $-300,000$                      | $0.5$ |

**Cálculo del Valor Esperado Medio para cada Acción**  

Dado que asumimos que ambos estados tienen la misma probabilidad $P(\theta_1) = P(\theta_2) = 0.5$, calculamos:

$VEM(a_1) = (0.5)(100,000) + (0.5)(-500,000) = 50,000 - 250,000 = -200,000$

$VEM(a_2) = (0.5)(-300,000) + (0.5)(-300,000) = -150,000 - 150,000 = -300,000$

| **Acción ($a_j$)** | **$VEM(a_j)$** |
|----------------|-------------|
| **$a_1$: Despedir** | **$-200,000$** |
| **$a_2$: No despedir** | **$-300,000$** |

**Conclusión:**  

Como $max(-200,000, -300,000) = -200,000$, la decisión sería **$a_1$: Despedir al tesorero**.

Este cálculo muestra cómo se aplicaría el Criterio de Laplace en un caso sin probabilidades *a priori*. Sin embargo, dado que en este problema sí contamos con probabilidades, *el Criterio de Laplace no es relevante* para la toma de decisiones final de este problema.

#### **2. Criterio de la Máxima Posibilidad**  

Este criterio selecciona la acción con la mejor ganancia en el estado de la naturaleza más probable.

1. **Identificamos el estado más probable:**  
   $\theta_1$: El tesorero es el informante, $P = 0.9$ porque 0.9 es mayor que 0.1.

2. **Comparamos los pagos en este estado:**  
   - $a_1$ (Despedir) $\rightarrow +100,000$
   - $a_2$ (No despedir) $\rightarrow -300,000$

**Decisión según Máxima Posibilidad:**  
   Despedir al tesorero ($a_1$).

#### **3. Criterio del Valor Esperado Medio (VEM) o Regla de Bayes**  

Este criterio calcula el rendimiento esperado de cada acción ponderando cada posible resultado con su probabilidad.

**Cálculo del VEM para cada acción:**  

   $VEM(a_1) = P(\theta_1) U(\theta_1, a_1) + P(\theta_2) U(\theta_2, a_1)$

   $VEM(a_1) = (0.9)(100,000) + (0.1)(-500,000) = 90,000 - 50,000 = 40,000$

   $VEM(a_2) = P(\theta_1) U(\theta_1, a_2) + P(\theta_2) U(\theta_2, a_2)$

   $VEM(a_2) = (0.9)(-300,000) + (0.1)(-300,000) = -270,000 - 30,000 = -300,000$

| **Acción ($a_j$)** | **$VEM(a_j)$** |
|----------------|-------------|
| **$a_1$: Despedir** | **$+40,000$** |
| **$a_2$: No despedir** | **$-300,000$** |

Como $max(VEM(a_1), VEM(a_2)) = max (+40,000, -300,000) = +40,000$ y corresponde a $a_1$.  
 
**Decisión según VEM:**  Despedir al tesorero ($a_1$).

#### **3: Evaluación del Impacto de las Decisiones**  

| **Criterio de Decisión** | **Decisión Óptima** |
|----------------------|----------------------|
| **Máxima Posibilidad** | **Despedir ($a_1$)** |
| **Valor Medio Esperado (VEM)** | **Despedir ($a_1$)** |

#### **4. Conclusión de la Fase 2**  

1. **El criterio de Máxima Posibilidad** selecciona la mejor acción en el estado más probable. Como hay un 90% de probabilidad de que el tesorero sea el informante, despedirlo es la mejor opción.
2. **El criterio del VEM** pondera los posibles resultados con sus respectivas probabilidades y selecciona la acción con el mayor rendimiento esperado. Despedir al tesorero tiene un valor esperado positivo de $+40,000$, mientras que no despedirlo genera una pérdida esperada de $-300,000$.

**Decisión final en esta fase:**  
Todos los criterios coinciden en que la mejor decisión es: **despedir al tesorero ($a_1$)**.

En la siguiente fase, se analizará si la realización de pruebas con el detector de mentiras cambia esta decisión.

---

### Fase 3: Análisis de Decisiones Bajo Riesgo Con Experimentación

#### **1. Estructura inicial de la Matriz de Pagos (sin prueba)**

| **Estado ($\theta_i$) / Acción ($a_j$)** | **$a_1$: Despedir al tesorero** | **$a_2$: No despedir al tesorero** | **$P(\theta_i)$ A priori** |
|---------------------------------------------|----------------------------------|----------------------------------|----------------|
| **$\theta_1$: El tesorero ES el informante** | $+100,000$                      | $-300,000$                      | $0.9$ |
| **$\theta_2$: El tesorero NO es el informante** | $-500,000$                      | $-300,000$                      | $0.1$ |

Para recalcular la matriz de pagos, primero debemos considerar las acciones posibles, los resultados de la prueba del detector de mentiras y ajustar las probabilidades usando el **Teorema de Bayes**.

#### **2. Acciones posibles:**

1. **$a_1$: Despedir al tesorero directamente.**
2. **$a_2$: No despedir al tesorero.**
3. **$a_3$: Aplicar la prueba del detector de mentiras y luego decidir.**

Cada una de estas acciones tiene costos y beneficios dependiendo de los resultados de la prueba y la actualización de probabilidades usando el **Teorema de Bayes**.

#### **3: Recalcular Probabilidades Posteriores o *a posteriori***

Se refiere a las probabilidades condicionales al usar el detector de mentiras, del que sabemos que:
- Si el tesorero **es el informante** ($\theta_1$), la prueba lo detecta correctamente en el **$90$%** de los casos.
- Si el tesorero **NO es el informante** ($\theta_2$), la prueba indica inocencia correctamente en el **$70$%** de los casos.

**Aplicación del Teorema de Bayes para actualizar las probabilidades**

La probabilidad de que el tesorero sea el informante dado un resultado positivo (+) se calcula como sigue:

$P(\theta_1 | +) = \frac{P(+ | \theta_1) P(\theta_1)}{P(+ | \theta_1) P(\theta_1) + P(+ | \theta_2) P(\theta_2)} = \frac{(0.9)(0.9)}{(0.9)(0.9) + (0.3)(0.1)} = \frac{0.81}{0.81 + 0.03} = \frac{0.81}{0.84} = 0.964$

Y la probabilidad de que el tesorero NO sea el informante dado un resultado negativo (-), se calcula de mandera semejante:

$P(\theta_2 | -) = \frac{P(- | \theta_2) P(\theta_2)}{P(- | \theta_1) P(\theta_1) + P(- | \theta_2) P(\theta_2)} = \frac{(0.7)(0.1)}{(0.1)(0.9) + (0.7)(0.1)} = \frac{0.07}{0.07 + 0.09} = \frac{0.07}{0.16} = 0.4375$

Esas son las nuevas probabilidades asociadas a cada uno de los eventos, por lo tanto las reemplazamos en la matriz de pagos.

#### **4: Recalcular la Matriz de Pagos con Experimentación**

Después de aplicar el **Teorema de Bayes**, se pueden estimar las consecuencias de las decisiones en términos económicos, ajustando las probabilidades.

Si se realiza la prueba ($a_3$), se deben considerar tres costos:
- **Costo de la prueba**: $\$30,000$.
- **Costo de tomar la decisión equivocada** (despedir a alguien inocente o dejar a un informante dentro de la empresa).
- **Mejora en la certeza** al actualizar las probabilidades después de la prueba.

Esto se debe reflejar en la nueva matriz de pagos:

| **Estado ($\theta_i$) / Acción ($a_j$)** | **$a_1$: Despedir al tesorero** | **$a_2$: No despedir al tesorero** | **$a_3$: Aplicar prueba** | **$P(\theta_i)$ Actualizado** |
|---------------------------------------------|----------------------------------|----------------------------------|----------------------------------|----------------|
| **$\theta_1$: El tesorero ES el informante** | $+100,000$                      | $-300,000$                      | Depende del resultado de la prueba | $0.964$ |
| **$\theta_2$: El tesorero NO es el informante** | $-500,000$                      | $-300,000$                      | Depende del resultado de la prueba | $0.4375$ |

El resultado de la prueba cambia la probabilidad de que el tesorero sea el informante y, por lo tanto, puede modificar la decisión óptima si el costo de la prueba ($\$30,000$) es menor que la mejora en la certeza de la decisión.

#### **5: Evaluación del Impacto de la Nueva Matriz**

El siguiente paso es evaluar si el **valor esperado medio con la prueba** justifica su costo, lo que determinará si la presidenta debería proceder con la experimentación o no.

Para analizar cómo se calculó la **matriz de pagos considerando los costos de la prueba**, desglosaremos el impacto de la experimentación en la decisión y en los valores esperados de cada acción. Para calcular los valores esperados con la prueba, es necesario analizar los posibles resultados de la prueba.

#### **6: Evaluación de los Pagos con Experimentación**

Ahora, evaluamos el **valor esperado medio (VEM) con experimentación**, incorporando el costo de la prueba.

$VEM(a_3) = P(+) \times \left[ P(\theta_1 | +) U(\theta_1, a_1) + P(\theta_2 | +) U(\theta_2, a_1) \right] + P(-) \times \left[ P(\theta_1 | -) U(\theta_1, a_2) + P(\theta_2 | -) U(\theta_2, a_2) \right] - Costo_de_la_prueba$

Reemplazamos los valores:

$VEM(a_3) = (0.84) \times \left[ (0.964)(100,000) + (0.036)(-500,000) \right] + (0.16) \times \left[ (0.5625)(-300,000) + (0.4375)(-300,000) \right] - 30,000$

$VEM(a_3) = (0.84) \times \left[ 96,400 - 18,000 \right] + (0.16) \times \left[ -168,750 - 131,250 \right] - 30,000$

$VEM(a_3) = (0.84)(78,400) + (0.16)(-300,000) - 30,000$

$VEM(a_3) = 65,856 - 48,000 - 30,000 = -12,144$

Dado que **$VEM(a_3) = -12,144$** es menor que **$VEM(a_1) = 40,000$**, se concluye que **el costo de la prueba no se justifica**.

#### **7. Conclusión sobre la Aplicación de la Prueba**

- La prueba mejora la certeza de la decisión, pero no lo suficiente como para justificar su costo de $\$30,000$, por lo que **la prueba no es una inversión rentable.** Si el costo de la prueba fuera significativamente menor, podría haber sido justificable realizarla.
- La mejor decisión sigue siendo **despedir al tesorero sin realizar la prueba** ($a_1$).

Aquí está el **árbol de decisiones** mejorado, incluyendo las **probabilidades** asociadas a cada estado de la naturaleza ($\theta_i$) para cada acción ($a_j$).

#### **8. Árbol de decisiones**

Árbol de decisiones sin solución.
 
```
Inicio
  ├── a₁: Despedir al tesorero
  │     ├── θ₁: El tesorero ES el informante (P = 0.964) → +100,000
  │     ├── θ₂: El tesorero NO es el informante (P = 0.4375) → -500,000
  │
  ├── a₂: No despedir al tesorero
  │     ├── θ₁: El tesorero ES el informante (P = 0.964) → -300,000
  │     ├── θ₂: El tesorero NO es el informante (P = 0.4375) → -300,000
  │
  ├── a₃: Aplicar prueba (-30,000)
        ├── θ₁: El tesorero ES el informante (P = 0.964) → -12,144
        ├── θ₂: El tesorero NO es el informante (P = 0.4375) → -12,144
```

**Explicación de la estructura:**
1. **Inicio**: Representa el punto de decisión donde la presidenta elige entre las tres acciones posibles.
2. **Acciones ($a_j$)**:
   - $a_1$: Despedir al tesorero.
   - $a_2$: No despedir al tesorero.
   - $a_3$: Aplicar la prueba del detector de mentiras (\$-30,000 de costo).
3. **Estados de la naturaleza ($\theta_i$)**:
   - **$\theta_1$**: El tesorero **ES** el informante (probabilidad posterior $P = 0.964$).
   - **$\theta_2$**: El tesorero **NO** es el informante (probabilidad posterior $P = 0.4375$).
4. **Resultados económicos**: Las consecuencias monetarias de cada combinación de acción y estado de la naturaleza.

Este árbol de decisiones proporciona la estructura completa del problema **sin incluir la solución**. Éste debe resolverse utilizando el **Valor Esperado Medio (VEM)** para identificar la mejor opción.

**1: Cálculo del VEM para cada acción**

**Acción $a_1$: Despedir al tesorero**
$VEM(a_1) = P(\theta_1) \cdot U(\theta_1, a_1) + P(\theta_2) \cdot U(\theta_2, a_1)$

$VEM(a_1) = (0.964)(100,000) + (0.4375)(-500,000) = 96,400 - 218,750 = -122,350$

**Acción $a_2$: No despedir al tesorero**
$VEM(a_2) = P(\theta_1) \cdot U(\theta_1, a_2) + P(\theta_2) \cdot U(\theta_2, a_2)$

$VEM(a_2) = (0.964)(-300,000) + (0.4375)(-300,000) = -289,200 - 131,250 = -420,450$

**Acción $a_3$: Aplicar la prueba (costo -30,000)**
$VEM(a_3) = P(\theta_1) \cdot U(\theta_1, a_3) + P(\theta_2) \cdot U(\theta_2, a_3) - 30,000$

$VEM(a_3) = (0.964)(-12,144) + (0.4375)(-12,144) - 30,000 = -11,708.42 - 5,312.50 - 30,000 = -47,020.92$

**2: Determinación de la mejor acción**

   $max(VEM(a_1), VEM(a_2), VEM(a_3)) = max(-122,350, -420,450, -47,020.92) = -47,020.92$ que corresponde a $a_3$.
   - $VEM(a_1) = -122,350$ **No viable**
   - $VEM(a_2) = -420,450$ **No viable**  
   - $VEM(a_3) = -47,020.92$
 
La opción con el **mayor costo esperado** es **$a_3$**, por lo tanto, la directora debe **despedir al tesorero después de realizar pruebas** con el detector de mentiras.

**Árbol de decisiones resuelto**  

```
Inicio (VEM = -47,020.92)
  ├//- a₁: Despedir al tesorero (VEM = -122,350) ✅ 
  │      ├── θ₁: El tesorero ES el informante (P = 0.964) → +100,000
  │      ├── θ₂: El tesorero NO es el informante (P = 0.4375) → -500,000
  │
  ├//- a₂: No despedir al tesorero (VEM = -420,450)
  │      ├── θ₁: El tesorero ES el informante (P = 0.964) → -300,000
  │      ├── θ₂: El tesorero NO es el informante (P = 0.4375) → -300,000
  │
  ├── a₃: Aplicar prueba (-30,000) (VEM = -47,020.92)
        ├── θ₁: El tesorero ES el informante (P = 0.964) → -12,144
        ├── θ₂: El tesorero NO es el informante (P = 0.4375) → -12,144
```

**Árbol de decisiones resuelto en modo gráfico**  

Script de python que dibuja el árbol de decisiones.

```python
import matplotlib.pyplot as plt
import networkx as nx

def draw_decision_tree():
    G = nx.DiGraph()
    
    # Nodos principales
    G.add_node("Inicio\n(VEM = -47,020.92)")
    G.add_node("a₁: Despedir al tesorero\n(VEM = -122,350)")
    G.add_node("θ₁: Tesorero ES el informante\n(P = 0.964) → +100,000")
    G.add_node("θ₂: Tesorero NO es el informante\n(P = 0.4375) → -500,000")
    
    # Nodo no viable
    G.add_edge("Inicio\n(VEM = -122,350)", "a₁: Despedir al tesorero\n(VEM = -122,350)")
    G.add_edge("// a₁: Despedir al tesorero\n(VEM = -122,350)", "θ₁: Tesorero ES el informante\n(P = 0.964) → +100,000")
    G.add_edge("// a₁: Despedir al tesorero\n(VEM = -122,350)", "θ₂: Tesorero NO es el informante\n(P = 0.4375) → -500,000")
    
    # Nodo no viable
    G.add_node("// a₂: No despedir al tesorero\n(VEM = -420,450)")
    G.add_node("θ₁: Tesorero ES el informante\n(P = 0.964) → -300,000")
    G.add_node("θ₂: Tesorero NO es el informante\n(P = 0.4375) → -300,000")
    
    # Conexiones de la decisión tomada
    G.add_node("a₃: Aplicar prueba (-30,000)\n(VEM = -47,020.92) ✅")
    G.add_node("θ₁: Tesorero ES el informante\n(P = 0.964) → -12,144")
    G.add_node("θ₂: Tesorero NO es el informante\n(P = 0.4375) → -12,144")
    
    # Conexiones de nodos no viables
    G.add_edge("Inicio\n(VEM = -122,350)", "// a₂: No despedir al tesorero\n(VEM = -420,450)")
    G.add_edge("// a₂: No despedir al tesorero\n(VEM = -420,450)", "θ₁: Tesorero ES el informante\n(P = 0.964) → -300,000")
    G.add_edge("// a₂: No despedir al tesorero\n(VEM = -420,450)", "θ₂: Tesorero NO es el informante\n(P = 0.4375) → -300,000")
    
    G.add_edge("Inicio\n(VEM = -122,350)", "a₃: Aplicar prueba (-30,000)\n(VEM = -47,020.92)")
    G.add_edge("a₃: Aplicar prueba (-30,000)\n(VEM = -47,020.92)", "θ₁: Tesorero ES el informante\n(P = 0.964) → -12,144")
    G.add_edge("a₃: Aplicar prueba (-30,000)\n(VEM = -47,020.92)", "θ₂: Tesorero NO es el informante\n(P = 0.4375) → -12,144")
    
    # Dibujar el grafo
    plt.figure(figsize=(12, 8))
    pos = nx.drawing.nx_agraph.graphviz_layout(G, prog="dot")
    nx.draw(G, pos, with_labels=True, node_color='lightgray', edge_color='black', node_size=5000, font_size=9)
    plt.title("Árbol de Decisiones Resuelto")
    plt.show()

# Llamada a la función para dibujar el árbol
draw_decision_tree()
```

#### **Conclusión Fase 3**
1. **La mejor acción** según el VEM es **despedir al tesorero después de aplicar la prueba** ($a_3$) con una pérdida esperada de 47,020.92
2. **No despedirlo ($a_2$) genera una pérdida mucho mayor (\$-420,450)**, por lo que no es viable.

Por lo tanto, **la presidenta debe despedir al tesorero después de realizar la prueba del detector de mentiras**.

---

#### Fase 4: Selección Final de la Estrategia Óptima

El propósito es integrar todos los resultados de las fases anteriores para seleccionar la mejor estrategia bajo las condiciones dadas.

A continuación, analizamos por qué **no aplicar la prueba** y **despedir al tesorero** sigue siendo la mejor decisión, a pesar de que en la Fase 3 parecía que la prueba minimizaba la pérdida esperada.

**1. Comparación de las Decisiones y Valores Esperados**

| **Acción ($a_j$)** | **VEM en la Fase 2 (sin prueba)** | **VEM en la Fase 3 (con prueba)** |
|----------------|----------------|----------------|
| **$a_1$: Despedir al tesorero** | **$+40,000$** | **$-122,350$** |
| **$a_2$: No despedir al tesorero** | **$-300,000$** | **$-420,450$** |
| **$a_3$: Aplicar la prueba (\$-30,000)** | **N/A** | **$-47,020.92$** |

A simple vista, en la **Fase 3**, la opción de aplicar la prueba ($a_3$) parece mejor que despedir directamente al tesorero ($a_1$). **Sin embargo, esta conclusión no es necesariamente la correcta**, porque la Fase 2 también mostró que, sin prueba, despedir al tesorero tenía un VEM positivo ($+40,000$).

**¿Por qué NO aplicar la prueba?** La respuesta se justifica considerando los siguientes aspectos:

**a) Impacto de la Prueba en las Probabilidades**
- **Antes de la prueba**, la probabilidad de que el tesorero sea culpable es **90%** ($P(\theta_1) = 0.9$).
- **Después de la prueba**, con el **Teorema de Bayes**, la probabilidad actualizada se incrementa a **96.4%** ($P(\theta_1 | +) = 0.964$).
- **Pero este aumento en certeza es marginal** (solo del **6.4%**), lo que indica que **la prueba no cambia significativamente la decisión**, sino que solo la refuerza.

**b) Costo de la Prueba vs. Beneficio**
- **El costo de la prueba es \$30,000** y el valor esperado después de aplicarla sigue siendo **una pérdida de \$-47,020.92**.
- **Sin la prueba**, el despido del tesorero tenía un VEM positivo de **\$+40,000** en la Fase 2.
- **Por lo tanto, aplicar la prueba genera un costo innecesario sin mejorar significativamente la certeza**.

**c) Diferencia Clave entre Fase 2 y Fase 3**
- En la **Fase 2**, el despido sin prueba es la mejor opción con una ganancia esperada de **\$+40,000**.
- En la **Fase 3**, aplicar la prueba minimiza la pérdida, pero el VEM sigue siendo negativo **(\$-47,020.92)**.
- **Conclusión:** La prueba no justifica su costo y es mejor seguir con la decisión original de la Fase 2.

## **3. Conclusión Final**
- **No se debe aplicar la prueba**, porque su costo adicional no se justifica por el pequeño aumento en certeza.
- **Se debe despedir al tesorero directamente**, ya que la información inicial (Fase 2) ya mostraba que esta era la mejor opción con un valor esperado positivo.

**Respuesta correcta:** Despedir al tesorero sin ordenar la prueba del detector de mentiras.
