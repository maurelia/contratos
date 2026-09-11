# NexOre ContractMineOre

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

## Comparador: comprador directo vs. ENAMI

`comparador-enami.html` es una calculadora de un solo archivo que toma un
despacho de mineral (tonelaje, ley de Cu, Au y opcionalmente Ag) y compara:

- **Comprador directo**: valor bruto = precio de mercado × ley × recuperación
  pactada, sin descuentos (la misma lógica que la cotización de ejemplo de
  500 t al 0,8% Cu / 0,5 g/t Au, US$ 73.276 brutos).
- **ENAMI (estimado)**: la misma fórmula pública de ENAMI
  (`Valor Cu = precio × 2.204,6223 × ley × recuperación`), con recuperación,
  maquila, castigos y ley mínima de recepción (0,8% CuS) como campos
  editables.

**Importante**: los valores de la tabla ENAMI son de ejemplo, no la tarifa
oficial de septiembre 2026 — el entorno donde se generó esta calculadora no
tuvo acceso a `enami.cl` para leer el PDF de tarifas del mes. Ábrelo tú
mismo en `enami.cl/EnamiTransparente/B_HistoricoTarifas/` y actualiza
recuperación/maquila/castigos en el panel "Tarifa ENAMI" — el resto del
cálculo se recalcula solo. Igual que el resto de la suite, guarda tus
cambios en `localStorage` y no constituye asesoría comercial ni legal.
