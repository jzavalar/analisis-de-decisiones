# docs/ · Documentación del curso

Documentos de la UEA **Análisis de Decisiones** (clave 2211092), Licenciatura en Administración, División de Ciencias Sociales y Humanidades, UAM Unidad Iztapalapa. Trimestre 26-Otoño, grupo HE57. Profesor: dr. Jesús Zavala Ruiz.

Esta carpeta contiene el **programa analítico del curso**, el **programa de estudios oficial** y las páginas que se derivan del primero. El sitio del curso (<https://jzavalar.github.io/analisis-de-decisiones/>) se construye a partir de estos archivos, según el Anexo B del programa analítico.

## Contenido

| Archivo | Qué contiene | Origen | ¿Se edita? |
|---|---|---|---|
| [`programa-analitico.md`](programa-analitico.md) | Programa analítico completo (revisión del 28 de septiembre de 2026): datos de identificación, presentación, objetivos, temario, estrategia didáctica, proyectos P1 a P3, programación de las sesiones, evaluación, bibliografía y anexos | **Fuente única** | Sí |
| [`programa-oficial.md`](programa-oficial.md) | Programa de estudios oficial de la UAM (clave de seis dígitos 221192), transcrito sin cambios del documento impreso, fechado en 2012 | Documento institucional | No |
| [`calendario.md`](calendario.md) | Sección 7: periodo lectivo, días de descanso y tabla de las 20 sesiones | Generado | No |
| [`evaluacion.md`](evaluacion.md) | Sección 8: ponderaciones, evaluaciones escritas, rúbrica, bitácora de IAG, calificación final y recuperación | Generado | No |
| [`trabajo-de-campo.md`](trabajo-de-campo.md) | Sección 5.4: entrevista con el decisor y sus tres bloques de información | Generado | No |
| [`protocolo-ia.md`](protocolo-ia.md) | Sección 5.7: reglas de uso de asistentes de IA generativa y sus consecuencias | Generado | No |
| `README.md` | Este archivo | Manual | Sí |

### Dónde está cada tema

| Si busca… | Vaya a… |
|---|---|
| Fechas de las sesiones, descansos y holguras | [`calendario.md`](calendario.md) |
| Cómo se califica y con qué ponderación | [`evaluacion.md`](evaluacion.md) |
| Cuándo se permite usar IAG y qué se registra en la bitácora | [`protocolo-ia.md`](protocolo-ia.md) |
| Qué datos se piden al decisor y cuándo | [`trabajo-de-campo.md`](trabajo-de-campo.md) |
| Temario, objetivos, alcance y bibliografía | [`programa-analitico.md`](programa-analitico.md), secciones 3, 4 y 9 |
| Los tres proyectos (P1, P2 y P3) y su rúbrica | [`programa-analitico.md`](programa-analitico.md), sección 6 |
| El programa que la Universidad aprobó | [`programa-oficial.md`](programa-oficial.md) |

## Panorama del curso

Los datos de esta sección se tomaron de los archivos de la carpeta; ante cualquier diferencia, prevalece el programa analítico.

- **Periodo:** trimestre del 17 de septiembre al 11 de diciembre de 2026; clases del 21 de septiembre al 2 de diciembre; evaluaciones globales del 7 al 11 de diciembre.
- **Horario:** lunes y miércoles, de 16:00 a 18:00 h; 20 sesiones de dos horas (40 horas en aula).
- **Método:** aprendizaje basado en proyectos. Tres proyectos sucesivos: P1 «El problema bien planteado», P2 «El precio de la incertidumbre» y P3 «¿Vale la pena averiguar?». Cada alumno analiza la decisión real de una organización.
- **Evaluación:** tres exámenes escritos individuales (12 %, 15 % y 18 %), expediente de decisión (40 %), bitácora individual de uso de IAG (10 %) y participación y exposición (5 %).

## Cómo se relacionan los archivos

```text
programa-analitico.md ──(se genera)──▶ calendario.md        (sección 7)
      fuente única      ──(se genera)──▶ evaluacion.md        (sección 8)
                        ──(se genera)──▶ trabajo-de-campo.md  (sección 5.4)
                        ──(se genera)──▶ protocolo-ia.md      (sección 5.7)

programa-oficial.md      (independiente: transcripción del programa de la UAM)
```

Los cuatro archivos generados llevan al inicio este aviso: *«ARCHIVO GENERADO por programa-sitio a partir de docs/curso/programa-analitico.md y curso.yml. No lo edite: edite la fuente (o curso.yml y sus datos) y vuelva a generar.»*

**Regla de edición:** todo cambio de contenido se hace en `programa-analitico.md`; los archivos generados no se editan a mano, para que no diverjan de la fuente.

### Estado actual del repositorio

Verificado el 5 de octubre de 2026 sobre el commit `4351d86`:

- Los cuatro archivos generados **coinciden** con sus secciones en `programa-analitico.md` (comparación automática; véase abajo).
- El aviso de los archivos generados y el Anexo B del programa analítico mencionan rutas `docs/curso/…`, pero los archivos están hoy directamente en `docs/`.
- El Anexo B describe además `docs/index.md`, `docs/proyectos/p1…`, `p2…` y `p3…/index.md`, y una compilación con MkDocs y GitHub Actions. En este repositorio **no** existen esas páginas, ni el generador `programa-sitio`, ni `curso.yml`, ni `mkdocs.yml`, ni flujos de trabajo en `.github/`.

Mientras no estén en el repositorio, un cambio en `programa-analitico.md` que afecte las secciones 5.4, 5.7, 7 u 8 exige actualizar a mano el archivo generado correspondiente, conservando su aviso inicial. Conviene también decidir si se actualizan las rutas del Anexo B o se restituye la estructura `docs/curso/`.

## Cómo actualizar la documentación

1. Edite `programa-analitico.md`. Para datos del curso no repita fechas, ponderaciones ni claves en otros lugares: remita a la sección correspondiente.
2. Regenere los archivos derivados con `programa-sitio` si dispone de él; en caso contrario, actualice a mano la sección afectada en su archivo.
3. Compruebe que no hay divergencias (véase la siguiente sección).
4. Confirme los cambios en un solo commit, con un mensaje que nombre la sección modificada.

### Comprobar que los archivos generados están al día

Desde la raíz del repositorio, guarde el script siguiente (por ejemplo, como `check_docs_sync.py`) y ejecútelo con Python 3.9 o posterior. Termina con código 0 si los cuatro archivos coinciden con el programa analítico y con código 1 si alguno difiere. Ignora el aviso inicial, el nivel de los encabezados y el formato de las tablas.

```python
#!/usr/bin/env python3
"""Compara cada archivo generado de docs/ con su sección en docs/programa-analitico.md."""
import re, sys
from pathlib import Path

DOCS = Path("docs")                # se ejecuta desde la raíz del repositorio
SECCIONES = {                      # archivo generado -> (encabezado de origen, nivel)
    "calendario.md":       ("7.", 2),
    "evaluacion.md":       ("8.", 2),
    "trabajo-de-campo.md": ("5.4", 3),
    "protocolo-ia.md":     ("5.7", 3),
}

def extraer(fuente: str, prefijo: str, nivel: int) -> str:
    salida, dentro = [], False
    for linea in fuente.splitlines():
        m = re.match(r"^(#+) (.*)", linea)
        if m:
            if dentro and len(m.group(1)) <= nivel:
                break
            if not dentro and len(m.group(1)) == nivel and m.group(2).startswith(prefijo):
                dentro = True
        if dentro:
            salida.append(linea)
    return "\n".join(salida)

def normalizar(texto: str) -> list[str]:
    texto = re.sub(r"<!--.*?-->", "", texto, flags=re.S)           # encabezado «ARCHIVO GENERADO»
    lineas = []
    for l in texto.splitlines():
        l = re.sub(r"^#+ ", "", l)                                  # el nivel del encabezado cambia
        l = re.sub(r"\s*\|\s*", "|", re.sub(r"\s+", " ", l)).strip()
        if not l or re.fullmatch(r"-{3,}|\|?[-:|]+\|?", l):         # vacías, reglas y separadores de tabla
            continue
        lineas.append(l)
    return lineas

fuente = (DOCS / "programa-analitico.md").read_text(encoding="utf-8")
fallos = 0
for archivo, (prefijo, nivel) in SECCIONES.items():
    esperado = normalizar(extraer(fuente, prefijo, nivel))
    real = normalizar((DOCS / archivo).read_text(encoding="utf-8"))
    estado = "OK " if esperado == real else "DIFIERE"
    fallos += esperado != real
    print(f"{estado}  {archivo:<22} ← sección {prefijo}")
sys.exit(1 if fallos else 0)
```

Salida esperada:

```text
OK   calendario.md          ← sección 7.
OK   evaluacion.md          ← sección 8.
OK   trabajo-de-campo.md    ← sección 5.4
OK   protocolo-ia.md        ← sección 5.7
```

## Otras carpetas del repositorio

| Ruta | Contenido |
|---|---|
| `docs/` | Esta carpeta: documentación vigente del trimestre 26-Otoño |
| [`../archivo/`](../archivo/) | Material anterior a la reorganización del 5 de octubre de 2026 (README previo, programa y programación semanal, ejemplos, cuestionarios, materiales de Rangel e imágenes). Se conserva como referencia y no es fuente del curso vigente. La etiqueta Git `pre-archivo-2026-10-05` marca el estado previo |
| [`../LICENSE`](../LICENSE) | Licencia del repositorio: CC0 1.0 Universal |

## Notas y pendientes

- **Licencias.** El repositorio declara CC0 1.0. El programa analítico (sección 9.1) anuncia que las lecturas se publicarán bajo *Creative Commons Atribución-CompartirIgual 4.0*. Conviene dejar por escrito qué licencia aplica a cada tipo de contenido cuando se publiquen las lecturas.
- **Datos de las organizaciones.** Según la sección 5.4, los datos de las organizaciones y de los decisores no se publican en el sitio del curso ni en este repositorio. No los incluya en commits ni en ejemplos.
- **Claves de la UEA.** El programa oficial usa claves de seis dígitos (221192 y 213244); las actuales, de siete dígitos, son 2211092 (Análisis de Decisiones) y 2132044 (Estadística I, la UEA seriada). Véase el Anexo A del programa analítico.
- **Contacto.** [jzr@xanum.uam.mx](mailto:jzr@xanum.uam.mx).


