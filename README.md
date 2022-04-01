# Cafeteria
Prueba en java para la empresa Konecta

La prueba esta en un archivo comprimido, solo hay que extraerlo y se puede subir a netbeans o ha eclipse.
Dentro del archivo comprimido esta la base de datos y el conector mysql de java (Driver).

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
