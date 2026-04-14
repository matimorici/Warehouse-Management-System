# Gestor Almacen
Sistema de Gestión de Depósito, Stock y Órdenes de Compra

# Integrantes del proyecto
- Morici, Matías
- Dominguez, Dolores
- Rufine, Tadeo

# Descripción general del sistema
Sistema orientado a la gestión integral de un depósito de productos. Permite administrar el stock, organizar la ubicación física de los productos dentro del almacén, gestionar proveedores y registrar órdenes de compra. 
El sistema modela el flujo completo de abastecimiento: desde la creación de órdenes de compra a proveedores, hasta la recepción de mercadería, actualización automática del stock y control de movimientos internos dentro del depósito. Además, permite el seguimiento de pedidos y la generación de reportes para la toma de decisiones.
El objetivo del sistema es digitalizar y centralizar la gestión logística de un depósito, mejorando el control de inventario, la trazabilidad de los productos y la eficiencia operativa.

# Diagrama de Clases
Producto
Categoria
Ubicacion
Stock
Movimiento
Pedido
DetallePedido
Usuario

# Casos de Uso para Regularidad
ABMC (Alta, Baja, Modificación, Consulta)
- Gestión de productos
- Gestión de proveedores
- Gestión de ubicaciones
- Gestión de usuarios
ABMC dependiente
- Gestión de pedidos
- Gestión de Stock
Caso de uso NO-ABMC
- Movimiento fisico de stock
- Valoracion de proveedores
Listados
- Listado de productos y stock (complejo)
- Listado de órdenes de compra
- Listado ubicaciones fisica

# Casos de Uso para AD
ABMC
- Gestión de movimientos
- Gestión de detallePedido

Casos de uso complejos

Gestión de órdenes de compra:
Carga de orden estado pendiente.
Carga de orden recibida, cambio de estado a RECIBIDO
Actualización automática de stock
Registro de movimientos de stock

Gestión de uso de stock:
Creación de Formulario de pedido
Selección de productos y cantidad
Descuento de stock

Listados complejos
Movimientos de stock filtrados por fecha y producto
Listado de proveedores para toma de decisiones (filtro por producto)

Roles del sistema
Administrador: Acceso total al sistema
Operario: Gestión de movimientos, pedidos y operaciones diarias

Requerimientos extra - AD
Mail: alerta baja stock
