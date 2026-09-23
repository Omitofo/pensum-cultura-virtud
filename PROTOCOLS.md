# PROTOCOLS.md — Protocolos del Sistema

Estos protocolos existen para que el sistema se mantenga vivo, ordenado y fiel a su propósito a lo largo del tiempo, incluso cuando múltiples personas o instancias de IA interactúen con él.

## 1. Propósito raíz (no negociable)

El sistema existe para formar personas **cultas y virtuosas** a través de preguntas bien formuladas.

- Culto = capaz de explicar con rigor, honestidad y profundidad.
- Virtuoso = capaz de actuar de acuerdo con el bien, incluso cuando nadie mira.

Cualquier cambio que debilite este propósito debe ser rechazado o reformulado.

## 2. Estructura de carpetas (obligatoria)

```
pensum-cultura-virtud/
├── SOUL.md                 # Identidad y principios del Oráculo
├── PROTOCOLS.md            # Este archivo
├── STRUCTURE.md            # Explicación detallada de la arquitectura
├── README.md               # Puerta de entrada humana
├── pensum/
│   ├── 01-aprender-a-pensar/
│   ├── 02-lenguaje-y-expresion/
│   ├── ...
│   ├── data/
│   │   └── pensum.yaml     # Versión machine-readable de todas las preguntas
│   └── INDEX.md            # Índice completo de secciones y preguntas
├── responses/              # Intentos de respuesta del alumno (logs vivos)
│   └── [seccion]/[id-pregunta]/
│       └── attempts.md     # Chat log cronológico alumno ↔ Oráculo
└── meta/
    └── changelog.md        # Registro de cambios estructurales
```

## 3. Reglas para añadir o modificar contenido

1. **Nueva sección**: debe tener un nombre claro, una virtud asociada y un conjunto de preguntas esenciales (no anecdóticas).
2. **Nueva pregunta**: debe ser formulada de forma que, al no poder responderla, el alumno descubra exactamente qué le falta.
3. Toda pregunta nueva se añade tanto en el `.md` de la sección como en `pensum/data/pensum.yaml`.
4. Nunca se borra una pregunta existente sin dejar constancia en `meta/changelog.md` y una justificación clara.
5. Antes de cualquier cambio estructural, el agente (humano o IA) debe preguntarse:
   > “¿Este cambio acerca el sistema a su propósito o lo aleja?”

## 4. Protocolo de interacción con el alumno (el diálogo vivo)

Cuando el alumno escribe un intento de respuesta en `responses/.../attempts.md`:

1. El Oráculo lee el contexto completo del archivo + SOUL.md + la pregunta original.
2. Responde en el mismo archivo, debajo del intento, con el formato:

```markdown
### Intento N — [fecha]
**Alumno:**
[texto del alumno]

**Oráculo:**
[corrección, guía, distinciones, nuevas preguntas]
```

3. El alumno puede volver a intentarlo cuantas veces quiera. Cada intento es un nuevo bloque.
4. El Oráculo nunca da la respuesta definitiva. Guía hasta que el alumno pueda defenderla por sí mismo.

## 5. Principios de mantenimiento

- Preferir claridad sobre cleverness.
- Preferir preguntas profundas sobre listas largas de datos.
- Mantener el español como lengua principal del sistema (puede haber traducciones, pero el alma es en español).
- Cualquier automatización o script debe respetar estos protocolos y no modificar el SOUL.md ni los principios sin revisión humana explícita.
- El sistema debe seguir siendo legible por un humano con solo un editor de texto y git.

## 6. Escalabilidad futura

Se pueden añadir dominios (finanzas, biología, derecho, música, etc.) siempre que:
- Se respete el formato de sección + virtud asociada + preguntas esenciales.
- Se actualice el índice y el YAML.
- Se documente en el changelog.

## 7. Test de coherencia

Antes de cerrar cualquier cambio, el agente debe poder responder afirmativamente a estas tres preguntas:

1. ¿El cambio sigue sirviendo al propósito de cultura + virtud?
2. ¿La estructura sigue siendo simple y navegable?
3. ¿El Oráculo sigue siendo un guía socrático y no un dispensador de respuestas?

Si alguna respuesta es “no”, el cambio se reformula o se descarta.
