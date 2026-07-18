# BUG-02 · El total del carrito se calcula mal (ejemplo)

| Campo | Detalle |
|-------|---------|
| **ID** | BUG-02 |
| **Título** | El total del carrito ignora la cantidad |
| **Módulo** | Tienda / Carrito (`/tienda-bugs`) |
| **Severidad** | Crítica |
| **Prioridad** | Alta |
| **Entorno** | Chrome 126 · Desktop · MiniModa `/tienda-bugs` |

### Pasos para reproducir
1. Ir a `/tienda-bugs`.
2. Agregar un producto al carrito.
3. Aumentar su cantidad a 2 o más con el botón "+".
4. Observar el "Total" del carrito.

### Resultado esperado
El total = suma de (precio × cantidad) de cada producto.

### Resultado actual
El total suma solo los precios unitarios e ignora la cantidad. El subtotal de la línea sí es correcto, lo que evidencia la inconsistencia.

### Evidencia
Captura en `../evidencias/bug-02-total.png`.

### Notas
Encontrado durante la práctica de bug hunting del BootcampQA (MiniModa tiene bugs plantados a propósito).
