# Diagrama-ER
Diagrama ER con las relaciones entre tablas


+------------------+      +------------------+      +------------------+
|     Categoria    |      |     Producto     |      |     Sucursal     |
+------------------+      +------------------+      +------------------+
| id (PK)          |      | id (PK)          |      | id (PK)          |
| nombre           |      | nombre           |      | nombre           |
|                  |      | marca            |      | direccion        |
|                  |      | categoria_id (FK)|      |                  |
|                  |      | precio_unitario  |      |                  |
+------------------+      +------------------+      +------------------+
        |                           |                           |
        |                           |                           |
        |                           |                           |
        |                           |                           |
        |                           |                           |
        |                           |                           |
        V                           V                           V
+------------------+      +------------------+      +------------------+
|      Stock       |      |      Cliente     |      |      Orden       |
+------------------+      +------------------+      +------------------+
| id (PK)          |      | id (PK)          |      | id (PK)          |
| sucursal_id (FK)|       | nombre           |      | cliente_id (FK)  |
| producto_id (FK) |      | telefono         |      | sucursal_id (FK) |
| cantidad         |      |                  |      | fecha            |
|                  |      |                  |      | total            |
+------------------+      +------------------+      +------------------+
                                  |
                                  |
                                  |
                                  |
                                  |
                                  V
                           +------------------+
                           |       Item       |
                           +------------------+
                           | id (PK)          |
                           | orden_id (FK)    |
                           | producto_id (FK) |
                           | cantidad         |
                           | monto_venta      |
                           +------------------+
