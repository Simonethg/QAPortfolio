# Casos de prueba — Checkout de MiniModa (ejemplo)

Funcionalidad: pago en `/checkout`. Envíos a cualquier país + tarjetas de prueba.

| ID | Título | Tipo | Prioridad |
|----|--------|------|-----------|
| CP-01 | Compra válida con tarjeta aprobada | Positivo | Alta |
| CP-02 | Tarjeta con menos de 16 dígitos | Negativo | Alta |
| CP-03 | Tarjeta rechazada (fondos insuficientes) | Negativo | Alta |
| CP-04 | Email con formato inválido | Negativo | Media |
| CP-05 | Vencimiento en formato incorrecto | Borde | Media |

---

### CP-01 · Compra válida con tarjeta aprobada
- **Precondiciones:** estar en `/checkout`.
- **Pasos:** completar nombre, dirección, email válido; país = Chile; tarjeta `4111111111111111`; vencimiento `12/28`; CVV `123`; confirmar.
- **Datos:** tarjeta de prueba aprobada.
- **Esperado:** mensaje "Compra confirmada" con número de orden `MM-XXXXXX` y costo de envío mostrado.
- **Obtenido:** _(Pass/Fail + captura en `../evidencias/`)_

### CP-03 · Tarjeta rechazada
- **Pasos:** igual a CP-01 pero tarjeta `4000000000009995`.
- **Esperado:** error "Fondos insuficientes"; NO se confirma la compra.
- **Obtenido:** _(completar)_

> Estos casos salen de practicar sobre MiniModa en el BootcampQA.
