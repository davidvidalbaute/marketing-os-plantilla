---
name: auditar-brief
description: Audita un brief contra el brief maestro del equipo, calcula su puntaje de suficiencia y devuelve los vacíos como agenda. Úsalo cuando pidan revisar, calificar o completar un brief.
---

# Auditar un brief

## Entradas
- El brief a revisar (texto pegado o archivo).
- `02-research-brief/brief-maestro.md` con los pesos y mínimos del equipo.
- `01-contexto/` para verificar coherencia con la marca.

## Pasos
1. Lee el brief maestro. Si los pesos no suman 100 o faltan mínimos, detente y dilo.
2. Recorre los ocho bloques. Para cada uno, cita la frase del brief que lo responde o escribe "ausente".
3. Califica cada bloque de 0 al peso asignado. Una respuesta sin dato ni fuente vale como máximo la mitad.
4. Trata "no tenemos ese dato" como vacío declarado: no suma puntos, pero entra a la agenda.
5. Suma el puntaje y compáralo con el mínimo del equipo.
6. Revisa contradicciones con `01-contexto/` y con `no-hacemos.md`.

## Salida
Entrega exactamente esto:

- **Veredicto:** listo para producción / necesita trabajo / se devuelve, con el puntaje sobre 100.
- **Tabla:** bloque · puntaje · evidencia citada · qué falta.
- **Agenda:** las preguntas que la persona responsable debe cerrar, ordenadas por impacto.
- **Riesgos:** contradicciones con el contexto o con las renuncias de la marca.

## Lo que no haces
- No completas el brief con datos inventados.
- No apruebas un brief por debajo del mínimo: lo escalas a quien indique el brief maestro.
