# Requerimientos del sistema

## Requisitos funcionales
- RF-01: El sistema debe permitir el registro CRUD de productos (panes, dulces,
  bocaditos, snacks, bebidas), incluyendo precio, categoria y stock minimo.
- RF-02: El sistema debe permitir registrar ventas de forma agil, calculando
  automaticamente subtotal, IVA y total, y generando un comprobante digital.
- RF-03: El sistema debe restar automaticamente del stock las unidades vendidas
  y alertar visualmente cuando un producto llegue al stock minimo.

## Requisitos no funcionales
- RNF-01 (Usabilidad): Interfaz web responsiva, con curva de aprendizaje baja,
  permitiendo registrar una venta en menos de 5 clics.
- RNF-03 (Seguridad): Control de acceso por roles (Administrador/Vendedor) con
  contrasenas encriptadas mediante BCrypt.
