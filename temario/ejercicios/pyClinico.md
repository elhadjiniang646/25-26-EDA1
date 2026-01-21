# Sistema de gestión de emergencias hospitalarias

Un hospital necesita gestionar el flujo de pacientes en el servicio de urgencias. El sistema debe soportar múltiples operaciones:

1. **Admisión de pacientes**: Llegada continua con datos (nombre, síntomas, nivel de gravedad 1-5).
1. **Atención por prioridad**: El médico disponible debe atender al paciente más grave pendiente.
1. **Seguimiento cronológico**: Auditoría debe poder listar pacientes en orden de llegada.
1. **Búsqueda por identificador**: Enfermería necesita localizar pacientes específicos rápidamente.
1. **Reagravación**: Un paciente ya ingresado puede empeorar, requiriendo actualización de prioridad.
1. **Cancelación**: Pacientes pueden ser derivados a otros servicios o dados de alta.
1. **Estadísticas**: Número de pacientes por nivel de gravedad.

## Restricciones explícitas

### Contexto operativo

- Volumen esperado: 200-500 pacientes simultáneos en urgencias

### De recursos

- El sistema funcionará en entornos de memoria limitada, por lo que se requiere optimizar este recurso
- Por contra, la capacidad de procesamiento es razonablemente alta

### De operación

- La reagravación debe reflejarse inmediatamente en el orden de atención

## Entregable

1. **Diagramas**: Representación visual UML de qué estructuras se utilizan y cómo se conectan
1. **Justificación**: Para cada operación, explicar **qué** estructura soporta esa operación y **por qué**.
1. **Compromisos**: Identificar de modo claro qué operaciones se sacrifican (si alguna) y el coste aceptado
1. **Casos límite**: Describa cómo el diseño que propone maneja:
     - Paciente con mismo nivel de gravedad que otros
     - Reagravación de paciente ya atendido parcialmente
     - Búsqueda de paciente no existente

## Operaciones adicionales (opcional)

**Deshacer última admisión**: En caso que un paciente sea registrado por error, se requiere poder anular su registro.

> *Si se implementa esta operación, debe incluirse en la justificación y análisis de compromisos.*