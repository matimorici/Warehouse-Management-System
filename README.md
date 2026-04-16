# Gestor Almacen
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
Producto.
Ubicacion.
Stock.
MovimientoFisico.
OrdenCompra.
LineaCompra.
Usuario.
OrdenRetiro.
LineaRetiro.
Proveedor.
ValoraciónProveedor.

# Casos de Uso para Regularidad
ABMC (Alta, Baja, Modificación, Consulta)
- Productos
- Proveedores
- Usuarios
- Ubicación

ABMC Dependiente
- OrdenCompra dependiente de Proveedor
- LineaCompra dependiente de OrdenCompra y Producto
- Stock dependiente de Producto
- MovimientoFisico dependiente de Ubicacion

Caso de uso NO-ABMC
- Movimiento fisico de stock
- Valoracion de proveedores

Listados
- Listado de productos y stock (complejo)
- Listado de ordenes de compra.
- Listado ubicaciones fisicas.

# Casos de Uso para AD
ABMC
- OrdenRetiro
- LineaRetiro dependiente de OrdenRetiro y Producto
- ValoraciónProveedor
  
Casos de uso complejos
+ Gestión de Orden de compra:
Operario carga Orden de compra con estado pendiente.
Actualizacion del stock en atributo stockPendiente.
Una vez llegada la mercaderia, Operario carga la orden con estado recibida.
Actualización automática de stock, se quita de stockPendiente y pasa a stockDisponible.
Posteriormente, se realiza la valoración al proveedor.
+ Gestión de Orden de Retiro:
Operario carga el Orden de Retiro seleccionando productos y cantidad.
Se actualiza el stock de los productos.

Listados complejos
- Movimientos fisico de productos filtrados por fecha.
- Listado de proveedores para toma de decisiones (filtro por producto).

Roles del sistema
- Administrador: Acceso total al sistema.
- Operario: Gestión de movimientos fisico, ordenes de compra y de retiro y operaciones diarias.


Requerimientos extra - AD
- Mail: alerta baja stock.
