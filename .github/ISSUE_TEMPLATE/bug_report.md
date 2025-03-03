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
    validations:
      required: true

  - type: textarea
    id: esperado
    attributes:
      label: "Resultado esperado"
      description: "¿Qué debería suceder en condiciones normales?"
      placeholder: "El pago debería procesarse exitosamente y mostrar la confirmación."

  - type: textarea
    id: obtenido
    attributes:
      label: "Resultado obtenido"
      description: "¿Qué sucede realmente?"
      placeholder: "Se muestra un mensaje de error: 'Error desconocido'."

  - type: textarea
    id: evidencia
    attributes:
      label: "Evidencia (capturas, logs, videos, etc.)"
      description: "Adjunta imágenes, videos o logs del error si es posible."

  - type: dropdown
    id: prioridad
    attributes:
      label: "Prioridad"
      description: "Selecciona el nivel de urgencia del problema."
      options:
        - "🟢 Baja (no bloquea el funcionamiento)"
        - "🟡 Media (afecta algunas funciones)"
        - "🔴 Alta (bloquea el uso del sistema)"
    validations:
      required: true

  - type: input
    id: entorno
    attributes:
      label: "Entorno afectado"
      description: "¿Dónde ocurre el problema?"
      placeholder: "Producción / Staging / Desarrollo"

  - type: input
    id: dispositivo
    attributes:
      label: "Dispositivo y navegador/SO"
      description: "Ejemplo: Windows 10, Google Chrome v120, iPhone 14 con iOS 17."
      placeholder: "Windows 11, Edge 120.0.0"

  - type: textarea
    id: comentarios
    attributes:
      label: "Comentarios adicionales"
      description: "Cualquier otra información que pueda ser útil."
