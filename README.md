# Warehouse Management System
Sistema de Gestión de Depósito, Stock y Órdenes de Compra

# Integrantes del proyecto
- Morici, Matías
- Dominguez, Dolores
- Rufine, Tadeo

# Descripción general del sistema
Sistema orientado a la gestión integral de un depósito de productos. Permite administrar el stock, organizar la ubicación física de los productos dentro del almacén, gestionar proveedores y registrar órdenes de compra y órdenes de retiro. 
El sistema modela el flujo completo de abastecimiento: desde la carga de órdenes de compra a proveedores, hasta la recepción de mercadería, actualización automática del stock y control de movimientos internos dentro del depósito. Permite el seguimiento del stock solicitado y la generación de reportes respecto a los proveedores para la toma de decisiones.
El objetivo del sistema es digitalizar y centralizar la gestión logística de un depósito, mejorando el control de inventario, la trazabilidad de los productos y la eficiencia operativa.

# Diagrama de Clases
<img width="1336" height="1046" alt="DER-GestorAlmacen" src="https://github.com/user-attachments/assets/aea2b73a-705d-409c-b45e-547df878cc33" />


# Regularidad
ABMC (Alta, Baja, Modificación, Consulta)
- Productos
- Proveedores
- Usuarios
- Ubicación

ABMC Dependiente
- MovimientoFisico de Producto y Ubicación.
- Stock dependiente de Producto.

Caso de uso NO-ABMC
- Registrar orden de compra.
- Valoración del proveedor.

Listados
- Listado de productos y stock (complejo).
- Listado de ordenes de compra.
- Listado ubicaciones fisicas.


# Aprobación Directa
ABMC
- OrdenRetiro
- LineaRetiro dependiente de OrdenRetiro y Producto
  
Casos de uso complejos
- Gestión de Orden de compra:
1. Operario carga Orden de compra con estado pendiente.
2. Actualizacion del stock en atributo cantidadPendiente.
3. Una vez llegada la mercaderia, Operario carga la orden con estado recibida.
4. Actualización automática de stock, se quita de cantidadPendiente y pasa a cantidadDisponible.
5. Posteriormente, se realiza la valoración al proveedor.
- Gestión de Orden de Retiro:
1. Operario carga el Orden de Retiro seleccionando productos y cantidad.
2. Se actualiza el stock de los productos.

Listados complejos
- Movimientos fisico de productos filtrados por fecha.
- Listado de proveedores para toma de decisiones (filtro por producto).

Roles del sistema
- Administrador: Acceso total al sistema.
- Operario: Gestión de movimientos fisico, ordenes de compra y de retiro y operaciones diarias.


Requerimientos extra - AD
- Mail: alerta baja stock.
