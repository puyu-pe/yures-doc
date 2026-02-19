# Fichas del Panel Operativo por paquetes

---

## 00. Inicio de turno y ubicación rápida

**Objetivo:** que el usuario entre, se ubique y no se pierda entre pisos/canales.

1. Ingresar al POS: diferencia entre **Punto de venta** y **Supervisor**.
2. Vista de mesas: **croquis**, cambio de **PISO**, lectura rápida de mesas.
3. Canales rápidos: **CALLE** y **DELIVERY** (qué cambia y cuándo usarlo).
4. Botones base (barra inferior): **CAJA / BÚSQUEDA VENTA / EGRESOS-INGRESOS / LÍMITE** (para qué sirve cada uno).

---

## 01. Mozo: tomar pedidos y enviarlos a cocina

**Objetivo:** dominar el flujo FOH (mesa/salón) sin errores.

1. Seleccionar mesa y **tomar pedido** (agregar ítems por categoría).
2. **Buscar producto** por nombre o código.
3. Ajustar cantidades rápido: **+ / –** y quitar ítem con **X**.
4. Agregar **Instrucción para cocina** (mensaje por ítem).
5. **Combos (simple):** agregar el combo y **completar los ítems requeridos**.
6. **Combos (fijo):** confirmar componentes definidos y aplicar cambios permitidos (si el combo lo permite).
7. **Combos (dinámico desde lista):** escoger **cantidad exacta (N)** desde una lista.
8. **Intercambio de componentes:** reemplazar uno o varios elementos cuando el combo lo permite.
9. **ENVIAR** a cocina: qué confirma que sí se envió.
10. **Precuenta**: cuándo usarla y qué imprime.
11. **Cerrar** vs **Liberar** mesa: diferencias y errores típicos.

---

## 02. Cajero: liquidar venta y cobrar sin descuadres

**Objetivo:** cobrar rápido, registrar medio correcto y evitar errores de caja.

1. Abrir **Liquidar venta**: qué significa **Pendiente** vs **Pagado**.
2. Cobro simple **Efectivo**: **Registrar Pago** + **Guardar** (orden correcto).
3. Cobro **Tarjeta** / **Yape** / **Plin** / **Transferencia** / **Depósito**: elegir medio correcto.
4. **Multi-pagos**: combinar dos o más medios (ej. Yape + efectivo).
5. **Recargo** y **Descuento**: cuándo se usa y qué pasa si está restringido.
6. Tipo de documento: **Ticket / Boleta electrónica / Factura electrónica** (cuándo usar cada uno).
7. Datos de cliente (DNI/RUC, razón social, dirección, correo, celular): mínimo necesario por documento.
8. **Imprimir / Reimprimir** desde liquidación (casos típicos de cliente).

---

## 03. Dividir cuenta y cobrar por partes

**Objetivo:** resolver grupos y pagos separados sin romper el pedido.

1. Dividir cuenta por ítems: mover de **Items pendientes** a **Items a pagar**.
2. Pagar una parte y dejar el resto pendiente: cómo continuar sin perder control.
3. Buenas prácticas: **dividir antes de registrar pagos**.

---

## 04. Solución rápida de problemas (los casos más comunes)

**Objetivo:** que el usuario resuelva incidencias típicas sin llamar a soporte.

1. **Pedido no llega a cocina (impresora): checklist en 60 segundos**

   * Confirmar que se presionó **ENVIAR**.
   * Validar que el **PC servidor de impresión** esté encendido y en red.
   * Validar que **PUKA-HTTP** esté **en ejecución** en Windows (barra de notificaciones).
   * Revisar impresora: encendida, conectada, papel correctamente colocado.

2. **Pedido no llega a cocina (impresora): causas de red y cambios de IP**

   * Caso típico: cambiaron cable/switch/router, o pasaron a Wi‑Fi.
   * Resultado: cambia la **IP del PC servidor** y se rompe la configuración local.
   * Qué hacer: validar IP actual, volver a dejar fija (o reservar IP) y reconfigurar.

3. **KDS no muestra pedidos: checklist rápido (caso KDS)**

   * Validar red del KDS, acceso al sistema y estado de recepción.
   * Diferencia clave: KDS depende de red/app, no de PUKA‑HTTP.

4. **Cobran mal: cómo corregir antes de finalizar**

   * Confirmar **medio de pago**.
   * Si hay mezcla: usar **Multi‑pagos**.
   * Validar **Pendiente / Paga / Vuelto** antes de Guardar.

5. **“Pedido duplicado” al cambiar de mesa: explicación real**

   * No es duplicado: la acción **Mover a mesa** también permite **Juntar mesa**.
   * Qué ocurre: el mismo pedido puede quedar visible en dos mesas por la unión.

6. **Mover a mesa vs Juntar mesa: cuándo usar cada uno**

   * Mover: traslado del pedido.
   * Juntar: dos mesas comparten el mismo pedido/cuenta.
   * Señal de error: “veo el pedido en ambas mesas”.

7. **Deshacer una mesa juntada (sin perder ítems)**

   * Flujo correcto para separar y dejar cada mesa consistente.
   * Evitar: borrar ítems o anular por desesperación.

8. **Movimientos de mesa(s): auditar qué pasó y dejar razón**

   * Revisar comandas, usuario y momento.
   * Usar el campo **Razón** y luego **Liberar** cuando corresponde.

9. **Liberar mesa: cuándo sí y cuándo no**

   * Sí: mesa quedó “colgada” por error y ya no hay consumo real.
   * No: cuando aún hay consumo por cobrar o la mesa está juntada.

10. **Combo mal armado: cómo corregir antes de enviar a cocina**

* Caso A: no completaron los datos del combo.
* Caso B: eligieron un intercambio incorrecto.
* Caso C: no respetaron la **cantidad exacta (N)** en combos dinámicos.
* Regla: corregir antes de **ENVIAR**; si ya se envió, seguir el procedimiento permitido por configuración (supervisor/corrección/anulación parcial).

---

## 05. Buscar venta y corregir desde operativo (acciones rápidas)

**Objetivo:** resolver reimpresión, canje y anulación sin entrar al panel administrativo.

1. Entrar a **Búsqueda venta** (barra inferior).
2. **Buscar documento** por tipo + serie + correlativo y previsualizar.
3. **Imprimir** desde búsqueda (casos típicos).
4. **Canjear** desde operativo: cuándo aplica y qué validar antes.
5. **Anular** desde operativo: cuándo aplica y por qué requiere control.
6. Ver/validar documento desde búsqueda: evitar anular/canjear el documento equivocado.

---

## 06. Canales de venta (variantes cortas)

**Objetivo:** cubrir el POS mixto sin videos largos ni confusos.

1. Venta en **Mesa (croquis)**: seleccionar mesa → tomar pedido → enviar → precuenta → liquidar.
2. Venta en **Salón / lista** (si aplica): flujo equivalente al croquis.
3. Venta **CALLE (mostrador/rápido)**: pedido directo → liquidación.
4. Venta **DELIVERY**: creación de pedido → control de entrega.
5. **Para llevar**: flujo de venta y entrega.
6. Botones laterales: **ESTADO** y **ENTREGAS** (qué resuelven en la operación).

---

## 07. Supervisor: control y corrección segura

**Objetivo:** concentrar acciones críticas para reducir fraudes y errores.

1. Entrar como **Supervisor**: qué habilita y qué no.
2. Política operativa recomendada: qué acciones deben ser solo de supervisor (anular/canjear/descuentos/liberar).
3. Resolver “mesa pegada / pedido en dos mesas”: auditar y corregir sin perder consumo.
4. Cierre operativo rápido: checklist de supervisor antes de entregar caja.

---

## 08. Impresión y dispositivos (hardware real)

**Objetivo:** bajar tickets de impresión y soportar escenarios multi-dispositivo.

1. Impresión de **ticket** en caja: validaciones mínimas.
2. Impresión de **comanda** a cocina (impresora asignada).
3. **Precuenta desde celular/tablet Android** con ticketera bluetooth.
4. PUKA-HTTP: qué es, cómo saber si está activo y por qué afecta la impresión.
5. Buenas prácticas de red: evitar que el PC servidor cambie de IP (router/switch/Wi‑Fi).

---

## 09. Límites y control de disponibilidad

**Objetivo:** evitar vender productos sin stock/disponibilidad.

1. Registrar **límite de ítems**: editar totales y **Guardar**.
2. Revisar pestaña **Reporte** (si se usa para control diario).
3. Caso práctico: qué hacer cuando un ítem llega a su límite (evitar reclamos en cocina).
