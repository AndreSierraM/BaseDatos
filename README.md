# BaseDatos
--  SELECT
SELECT Prod_Color FROM productos ORDER BY Prod_Color DESC;  -- Aqui pedimos los colores de los productos y los organizamos de manera descendente
SELECT Cli_Id FROM clientes; -- Aquí consulatamos el id de los clientes 
-- WHERE CLAUSULAS DE SELECT 
SELECT Ventas_Neto FROM ventas WHERE Ventas_Neto > 50000; -- Muentra el valor de las ventas hecchas que fueron mayor a 50mil
SELECT Ventas_Fecha FROM ventas WHERE Ventas_Fecha < '2018-01-10'; -- muestra las fecha de las ventas realizadas antes del 2018-01-31
-- CONSULTAS COMPUESTAS DE WHERE
SELECT * FROM productos WHERE Prod_Id < 1000  AND Prod_Precio >500; -- muestra los productos que son menores a mil(Pertenecen a la tienda 1) y que su precio sea mayor a 500
SELECT * FROM productos WHERE Prod_ProvId = 1 AND Prod_Status = 1; --  muestra los productos del provedoor 1 que estan disponibles/existencias 
-- WHERE Y LA UNION DE TABLA 
SELECT Prod_Id, Prod_Descripcion, Prov_Id FROM proveedores,productos; -- buscamos los  productos que entrega cada proveedor con su respectivo id 
SELECT Cli_Id, Cli_RazonSocial, Ventas_Id , Ventas_Fecha FROM clientes, ventas; -- muestra el id cliente, nombre, venta id y la fecha de la ventas que ha hecho
-- COLOCAR ALIAS 
SELECT Cli_Id AS 'ID Cliente', Cli_RazonSocial AS 'Nombre Cliente' FROM clientes; -- cambiamos los nombres algo mas comun 
SELECT Ventas_Neto AS 'Total Compra Sin Iva', Ventas_Iva AS 'Iva Calculado',Ventas_Total AS 'Total Precio venta' FROM ventas; -- Le cambiamos los nombres a un nombre mas común y fácil de entender 
