# Guía de colaboración

Gracias por participar en el Iberian Strategic Simulator. Este documento explica cómo trabajamos, qué se espera de cada rol y cómo desarrollar un módulo nuevo.

## 1. Condiciones de participación

- La participación es **voluntaria**.
- Al enviar una contribución aceptas que se publique bajo la **misma licencia del proyecto (CC BY-NC-SA 4.0)** y que tu autoría quede reconocida en el repositorio.
- Tu nombre aparece en el listado de colaboradores solo si lo has autorizado. Puedes usar un **alias**; en ese caso, usa el mismo alias en tus commits (`git config user.name`) y no uses un correo personal que te identifique si prefieres anonimato.
- No subas datos personales de nadie, ni claves, ni contraseñas.

## 2. Roles

| Rol | Funciones |
|---|---|
| Coordinación general | Dirección del proyecto, decisiones finales, versiones publicadas |
| Co-coordinación docente | Implantación en el aula, recogida de feedback, seguimiento del grupo |
| Responsable técnico | Revisión de código, gestión de ramas y versiones, publicación |
| Desarrollo | Implementación de módulos y corrección de errores |
| Contenido histórico | Investigación y redacción de escenarios, fuentes y desenlaces |
| Pruebas y documentación | Testeo, informes de errores, manual de uso |

Una persona puede tener más de un rol.

## 3. Flujo de trabajo

1. Elige una *issue* libre (cada módulo pendiente tiene la suya) y asígnatela.
2. Crea una rama: `modulo-XX-nombre` (por ejemplo, `modulo-04-crisis-colon`).
3. Trabaja en `src/iss.twee` y comprueba que el módulo funciona de principio a fin.
4. Abre una *pull request* explicando qué has hecho.
5. Pasa la revisión técnica (responsable técnico) y la revisión histórica (profesorado).
6. Una vez aprobada, se fusiona en `main` y se regenera `index.html`.

Reuniones breves cada dos semanas para revisar el tablero de tareas.

## 4. Plantilla de módulo

Cada módulo sigue la estructura del módulo 12 (P.O.4). Con `XXn` el código del módulo (por ejemplo `PT4`):

| Pasaje | Contenido |
|---|---|
| `XXn-Intro` | Título, micro-lección contextual y enlace para empezar |
| `XXn-Escenario` | Rol del jugador, situación y tres opciones estratégicas |
| `XXn-Resultado-A/B/C` | Consecuencias de cada opción, puntuación y análisis de los cinco pilares |
| `XXn-Informe` | Informe final con estrategia elegida, puntuación y base investigadora |

Convenciones:
- Variables: `$puntuacion` y `$estrategia`.
- Cada módulo enlaza de vuelta a `Menu-Principal`.
- Los comentarios de desarrollo van **dentro de un pasaje**, nunca sueltos entre pasajes.
- Condicionales: `(if:)`, `(else-if:)`, `(else:)`; revisa la sintaxis de Harlowe antes de enviar.

## 5. Criterios de calidad ("definición de hecho")

- [ ] El módulo se puede jugar completo sin errores y se probó al menos con una persona ajena al desarrollo.
- [ ] El desenlace histórico indica sus fuentes (bibliografía en la ficha de la *pull request*).
- [ ] Las tres opciones son razonables y las consecuencias son coherentes con la teoría de referencia.
- [ ] No hay textos pendientes ni enlaces rotos.
- [ ] Ortografía revisada.
- [ ] El módulo aprobado se marca como "operativo" en el README.

## 6. Cómo informar de un error

Abre una *issue* con: módulo afectado, pasos para reproducirlo, lo que esperabas que pasara y lo que pasó, y navegador o dispositivo.

## 7. Respeto y convivencia

Trabajamos con respeto, damos feedback constructivo y reconocemos el trabajo de los demás. Cualquier problema se comenta con la coordinación del proyecto.
