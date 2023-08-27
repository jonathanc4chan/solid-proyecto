# solid-proyecto

+-------------------+        +-----------------+       +--------------+ 
|     Material      |        |      producti   |       |     Venta    |
+-------------------+        +-----------------+       +--------------+
| - nombre          |        | - material      |       | - silla      |
| - tipo            |        | - precio        |       | - fecha      |
| - precio          |        |  - cantidadStock|       | - precio     |
+-------------------+        +-----------------+       +--------------+
| + getNombre()     |       | + getMaterial() |       | + getSilla() |
| + getTipo()       |       | + getPrecio()   |       | + getFecha() |
| + getPrecio()     |       | + vender()      |       | + getPrecio()|
+-------------------+       +-----------------+       +--------------+
+-------------------+       +-----------------+       
|       factura      |       |  fabrica de si  |     
+-------------------+       +-----------------+       
| - nombre          |       | - nombre        |       
| - nit             |       | - direccion     |     
| - numero de venta |       |  |     
+-------------------+       +-----------------+       
| + getNombre()     |       | + getdirrecion() |       
| + getnit ()       |       | + getnombre()   |      
| + getnumventa()   |       |                 |       
+-------------------+       +-----------------+   
Diagrama UML después de aplicar SOLID:

+-----------------+       +-----------------+
|   IVendible     |       |     Material    |
+-----------------+       +-----------------+
| + getPrecio()   |       | - nombre        |
| + getDescripcion|       | - tipo          |
+-----------------+       | - precio        |
                          +-----------------+
                                ^      ^
                                |      |
                  +----------------+   +-----------------+
                  |                |   |      Silla      |
                  v                |   +-----------------+
          +-----------------+       |   | - material      |
          |     Venta       |       |   | - precio        |
          +-----------------+       |   | - cantidadStock |
          | - vendible      |       |   +-----------------+
          | - fecha         |       |   | + getMaterial() |
          +-----------------+       |   | + getPrecio()   |
          | + getVendible() |       |   | + vender()      |
          | + getFecha()    |       |   +-----------------+
          +-----------------+
                  ^
                  |
          +-----------------+      
          |    SillaVenta  |
          +-----------------+
          | - silla         |
          +-----------------+
          | + getSilla()    |    
          +-----I------------+ ---------I
               I                        I
+---------------I----+       +-----------------+       
|       factura      |       |  fabrica de si  |     
+-------------------+       +-----------------+       
| - nombre          |       | - nombre        |       
| - nit             |       | - direccion     |     
| - numero de venta |       |  |     
+-------------------+       +-----------------+       
| + getNombre()     |       | + getdirrecion() |       
| + getnit ()       |       | + getnombre()   |      
| + getnumventa()   |       |                 |       
+-------------------+       +-----------------+ 
