---
name: Bug report
about: Create a report to help us improve
title: ''
labels: ''
assignees: ''

---

name: Reporte de Bug
description: Reporta un problema o error encontrado en el sistema.
title: "[BUG] Breve descripción del problema"
labels: ["bug", "pendiente de revisión"]
assignees: ["tu-usuario-o-equipo"]

body:
  - type: markdown
    attributes:
      value: "Gracias por tomarte el tiempo de reportar un bug. Por favor, completa la información de manera detallada."

  - type: input
    id: resumen
    attributes:
      label: "Descripción breve"
      description: "Explica en una línea el problema encontrado."
      placeholder: "Ejemplo: Error en el módulo de pagos al procesar tarjetas Visa"
    validations:
      required: true

  - type: textarea
    id: descripcion
    attributes:
      label: "Descripción detallada del problema"
      description: "Describe el problema con la mayor cantidad de detalles posible. ¿Qué está pasando y qué debería ocurrir?"
      placeholder: "Cuando intento pagar con tarjeta Visa, la transacción se cancela sin motivo..."
    validations:
      required: true

  - type: textarea
    id: pasos
    attributes:
      label: "Pasos para reproducirlo"
      description: "Describe cómo replicar el error paso a paso."
      placeholder: |
        1. Ir a la página de pagos.
        2. Ingresar los datos de una tarjeta Visa.
        3. Presionar el botón de pagar.
        4. Se muestra un mensaje de error inesperado.
