# Gestor Almacen
Sistema de Gestión de Depósito, Stock y Órdenes de Compra

# Integrantes del proyecto
Morici, Matías
Dominguez, Dolores
Rufine, Tadeo

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
Gestión de productos
Gestión de categorías
Gestión de proveedores
Gestión de ubicaciones
ABMC dependiente
Productos (dependen de categoría)
Ubicaciones (dependen de estructura del depósito)
Caso de uso NO-ABMC
Creación de orden de compra a proveedor con validación de reglas de negocio
Selección de proveedor
Agregado de productos y cantidades
Generación de orden en estado PENDIENTE
Listados
Listado de productos con categorías y stock
Listado de órdenes de compra

# Casos de Uso para AD
Casos de uso complejos
Gestión completa de órdenes de compra:
Creación de orden
Validación de datos
Cambio de estado a RECIBIDO
Actualización automática de stock
Registro de movimientos de stock
Gestión de pedidos (picking):
Creación de pedido
Selección de productos
Descuento de stock
Registro de preparación
Listados complejos
Stock actual con filtros por producto/categoría
Movimientos de stock filtrados por fecha y producto
Roles del sistema
Administrador
Acceso total al sistema
Operario
Gestión de movimientos, pedidos y operaciones diarias

Requerimientos extra - AD
