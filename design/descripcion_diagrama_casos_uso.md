# Diagrama de casos de uso

El diagrama (`diagrama_casos_uso_final.drawio`) representa los 7 casos de uso
principales del sistema:

1. **CU-01 Iniciar sesión**
2. **CU-02 Gestionar productos**
3. **CU-03 Registrar venta** (con actualización automática de inventario)
4. **CU-04 Consultar inventario**
5. **CU-05 Gestionar proveedores**
6. **CU-06 Generar reportes**
7. **CU-07 Administrar usuarios**

## Actores y permisos

- **Administrador / Dueño**: tiene acceso completo al sistema. Además de iniciar
  sesión, registrar ventas y consultar inventario, es el único que puede
  **gestionar productos, gestionar proveedores, generar reportes y administrar
  usuarios** (RNF-03 — control de acceso por roles).

- **Empleado / Cajero (Vendedor)**: tiene acceso limitado a las operaciones del
  día a día. Puede **iniciar sesión, registrar ventas y consultar inventario y
  productos**, pero no tiene acceso a la gestión de proveedores, reportes ni
  administración de usuarios, ya que esas son funciones administrativas.

Esta distribución de permisos es consistente con la matriz de trazabilidad y
los requerimientos funcionales definidos en el documento SRS (sección 5).
