# Cafeteria
Prueba en java para la empresa Konecta 

Consultas SQL.

#Producto con mayor Stock
SELECT id, stock, nombre_producto
FROM productos
WHERE stock = ( 
SELECT MAX( stock )  FROM productos);


#Producto más vendido

SELECT id, cantidad, id_producto
FROM ventas
WHERE id_producto = ( 
SELECT MAX( id_producto )  FROM ventas);
