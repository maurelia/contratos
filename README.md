# contratos

Auto generador de contratos.

## Relaves Cu·Au·Ag

`relaves-cu-au-ag.html` es un borrador interactivo de **Contrato de compraventa
de relaves mineros**, pensado para relaves con cobre, oro y plata. Es un único
archivo HTML autocontenido (sin dependencias de build): se abre directo en el
navegador o se sirve con GitHub Pages.

Qué hace:

- **Ficha de parámetros editable**: partes del contrato, antecedentes del
  acopio, cubicación, tablas de precio y todos los supuestos de la planta
  compradora. Cada cambio recalcula el documento y la calculadora al instante.
- **Precio por tramos**:
  - Tabla A — precio base según ley de cobre total (%).
  - Tabla B — ajuste según ley de oro (g/t).
  - Tabla C — ajuste según ley de plata (g/t).
- **Ley de cobre separada en insoluble (sulfuros) y soluble (óxidos)**, porque
  la flotación las recupera de forma muy distinta: el cobre insoluble
  (calcopirita, calcosina, covelina) flota bien (~85–95%), mientras que el
  cobre soluble (crisocola, malaquita, atacamita) flota mal incluso con
  sulfidización (~20–50%). Los valores por defecto están tomados de
  literatura metalúrgica y quedan documentados y editables en la propia
  herramienta.
- **Calculadora de margen del comprador (netback/NSR)**: a partir de leyes,
  recuperaciones, payability, precios de mercado, TC/RC y costos de planta,
  estima el precio máximo que el comprador puede pagar por tonelada de
  relave.
- **Contrato en español**, con cláusulas que se completan solas con los
  parámetros ingresados, botones para copiar el texto o imprimir/guardar
  como PDF, y guardado automático en el navegador (localStorage).

No constituye asesoría legal — es un borrador de trabajo para acelerar la
negociación, sujeto siempre a revisión de un abogado con experiencia en
derecho minero chileno.

### Cómo verla

- **Local**: descarga `relaves-cu-au-ag.html` y ábrelo con cualquier
  navegador.
- **GitHub Pages**: en *Settings → Pages*, elige la rama `main` y la raíz
  `/` como fuente. Queda disponible en
  `https://<usuario>.github.io/contratos/relaves-cu-au-ag.html`.
