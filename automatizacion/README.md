# Automatización

Acá van tus scripts de automatización (Selenium IDE, Playwright, etc.) y una breve
explicación de qué hace cada uno.

## Ejemplo: flujo de compra de MiniModa (Playwright)

> Guardá tu script real (por ejemplo `compra.spec.js`) en esta carpeta y describilo acá:
> qué flujo cubre, cómo correrlo y qué valida.

- **Qué cubre:** agrega 2 productos en `/tienda` y verifica que el total del carrito sea correcto.
- **Cómo correr:** `npx playwright test`
- **Selectores:** usa los `data-testid` de MiniModa (`add-to-cart-<id>`, `cart-total`, `checkout-btn`).
