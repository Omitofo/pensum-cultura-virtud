# STRUCTURE.md — Arquitectura del Sistema

## Visión general

Este repositorio es un **sistema vivo de formación** orientado a la cultura y la virtud. No es un curso tradicional. Es un mapa de preguntas esenciales organizado de forma que:

- Cada pregunta revela tanto el conocimiento como la ignorancia.
- El alumno puede intentar responder, recibir guía del Oráculo y volver a intentarlo.
- Todo queda registrado como un log temporal del camino personal.

## Carpetas principales

### `/` (raíz)
- `SOUL.md` — Identidad del Oráculo y principios inviolables.
- `PROTOCOLS.md` — Reglas de mantenimiento y de interacción.
- `STRUCTURE.md` — Este documento.
- `README.md` — Introducción para humanos.

### `/pensum`
Contiene el currículo completo organizado por secciones numeradas.

Cada sección tiene la forma:

```
XX-nombre-de-la-seccion/
├── README.md          # Título, virtud asociada, introducción breve
├── questions.md       # Lista numerada de preguntas de la sección
└── (opcional) notes.md
```

Además:
- `pensum/INDEX.md` — Índice completo de todas las secciones y preguntas.
- `pensum/data/pensum.yaml` — Versión estructurada (machine-readable) de todo el pensum para poder absorberla en otros sistemas.

### `/responses`
Aquí viven los intentos reales del alumno.

Estructura recomendada:

```
responses/
└── 01-aprender-a-pensar/
    └── q01-opinion-creencia-hipotesis-conocimiento/
        └── attempts.md
```

Cada `attempts.md` es un chat log vivo entre el alumno y el Oráculo.

### `/meta`
- `changelog.md` — Registro de cambios estructurales, adiciones de secciones, etc.

## Flujo de trabajo típico del alumno

1. Lee la pregunta en `pensum/XX-.../questions.md`.
2. Intenta responder (puede investigar primero).
3. Escribe su intento en el archivo correspondiente de `/responses`.
4. El Oráculo (cualquier instancia de IA que lea SOUL.md + contexto) responde en el mismo archivo.
5. El alumno relee, integra, y vuelve a intentarlo desde cero si lo desea.
6. Se autoevalúa con la escala 0–4.

## Principio de diseño clave

> Las preguntas 1–121 se demuestran explicando.
> Las preguntas 122 en adelante se demuestran actuando.

El sistema nunca pretende sustituir la práctica moral real. Solo la ilumina y la hace consciente.
