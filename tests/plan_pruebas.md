# Plan de pruebas

## 1. Pruebas ya ejecutadas — Prototipo de simulación

Estas pruebas se realizaron de forma manual sobre el prototipo interactivo
(`src/trigo_dorado_sistema.html`) para validar los flujos principales del
sistema antes del desarrollo final.

| # | Caso de prueba | Pasos | Resultado esperado | Resultado obtenido |
|---|---|---|---|---|
| CP-01 | Inicio de sesión como Administrador | Seleccionar rol Administrador → Iniciar sesión | Se muestra el panel principal con todos los módulos visibles | ✅ Correcto |
| CP-02 | Inicio de sesión como Vendedor | Seleccionar rol Vendedor → Iniciar sesión | Solo se muestran Panel, Ventas e Inventario | ✅ Correcto |
| CP-03 | Registrar un producto nuevo | Ir a Productos → Nuevo producto → llenar datos → Guardar | El producto aparece de inmediato en el catálogo | ✅ Correcto |
| CP-04 | Registrar una venta | Ir a Ventas → agregar 2 productos → Confirmar venta | El ticket calcula subtotal, IVA y total; el stock del producto disminuye automáticamente | ✅ Correcto |
| CP-05 | Alerta de stock mínimo | Vender un producto hasta que su stock llegue al mínimo configurado | El sistema muestra una notificación visual de stock bajo | ✅ Correcto |
| CP-06 | Restricción de acceso por rol | Iniciar sesión como Vendedor → intentar ver Productos/Proveedores/Reportes/Usuarios | Esos módulos no están disponibles en el menú del Vendedor | ✅ Correcto |

**Conclusión:** el prototipo responde correctamente a los flujos principales
definidos en los requerimientos funcionales (RF-01 a RF-06) y al control de
acceso por roles (RNF-03) del documento SRS.

## 2. Pruebas planificadas — Sistema final (backend + base de datos)

Estas pruebas se ejecutarán una vez desarrollados los módulos reales del
sistema (a partir de la Semana 15 del cronograma), contra la base de datos
definida en el modelo entidad-relación (`/design`).

| # | Caso de prueba planificado | Objetivo |
|---|---|---|
| CP-07 | Registrar un producto y verificar su persistencia en la base de datos | Confirmar que el INSERT en la tabla `productos` se realiza correctamente |
| CP-08 | Registrar una venta y verificar el descuento real de stock en la base de datos | Confirmar la actualización atómica de `productos.stock` al insertar en `ventas`/`detalle_ventas` |
| CP-09 | Autenticación de usuarios contra la tabla `usuarios` | Verificar el cifrado de contraseñas (BCrypt) y el control de acceso por rol a nivel de backend |
| CP-10 | Generación de reportes con datos reales acumulados | Verificar que los reportes diarios/semanales/mensuales reflejen datos reales de la base de datos |
| CP-11 | Pruebas de carga básicas | Verificar que el tiempo de respuesta de registro de venta se mantenga bajo 1.5 segundos (RNF-02) con datos reales |

**Estado actual:** planificado, pendiente de ejecución hasta finalizar el
desarrollo del backend.
