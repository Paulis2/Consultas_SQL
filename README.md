# Consultas1-SQL

#CONSULTA SQL

## Tabla usuario

![tabla usuario](img/captura.png "Tabla usuario")

## COMANDO SELECT

1. Para visualizar toda la información que contiene la tabla `usuario` se puede incluir con la instrucción SELECT el carcter '*' o cada uno de los campos de la tabla 

`select * from usuario`

![Consulta 1](img/2.png "Consulta 1")

2. Visualzar solamente la identificación del usuario

`select identificación from usuario`

![Consulta 2](img/3.png "Consulta 2")

3. si se desea obtener ls registros cuya identificación sean mayores o iguales a 150; se debe utilizar la clausula WHERE que especifica las condiciones que deben los registros que se van a seleccionar.

`SELECT * FROM Usuario WHERE Identificacion>=150`

![Consulta 3](img/4.png "Consulta 3")

4. Si se desea obtener los rgistros cuyo sus apellidos sean Vanegas o Cetina, se debe utilizar el operador IN que especifica los registros que se quieren visualizar en la tabla

`select apellidos from Usuario where apellidos IN('Vanegas', 'Cetina')`

![Consulta 4](img/5.png "Consulta 4")

O se puede utilizar el operador OR

`select apellido from Usuario where apellido='Vanegas' or apellido='Cetina'`

![Consulta 4](img/5_1.png "Consulta 4")

5. Si se desea obtener los registros cuya identificación sea menor a 110 y la ciudad sea Cali se debe utilizar el operador AND.

`select * from Usuario where identificacion<'150' and ciudad_nac='Cali'`

![Consulta 5](img/6.png "Consulta 5")

6. Si se desa obtener los registros cuyos nombres empiecen por la letra a, sebe utilizar l operador LIKE que utiliza los patrones "%" (todos) y '_' (caracter)

`select * from Usuario where nombre LIKE 'A%'`

![Consulta 6](img/7.png "Consulta 6")

7. Se desea obtener los registros cuyos nombres tengan la letra a 

`select * from Usuario where nombre LIKE '%a%'`

![Consulta 7](img/8.png "Consulta 7")


8. Si se desea obtener los regisro donde la cuarta letra de nomre sea una a

`select * from Usuario where nombre LIKE '___a%'`

![Consulta 8](img/9.png "Consulta 8")

9. Si se desea obtener los registros cuya identificación este entre el intervalo 110 y 150, se debe utilizar la clausula BETWEEN, que sirve para especificr un intervalo de valores

`select * from Usuario where identificacion BETWEEN '110' and '150'`

![Consulta 9](img/10.png "Consulta 9")

## COMANDO DELETE

10. Para eleminar solamente los registros cuya identificación sea mayor de 130 

`delete from Usuario where identficacion>'130'`

![Consulta 10](img/11.png "Consulta 10")

![Consulta 10](img/11_1.png "Consulta 10")

11. Para actualizar la ciudad de nacimiento de Cristian Vanegas cuya identificación es 114

`update Usuario set ciudad_nac = 'Manisalez' where identificacion='114'`

![Consulta 11](img/12.png "Consulta 11")

![Consulta 11](img/12_1.png "Consulta 11")

## Tabla pedidos

![Tabla pedidos](img/13.png "Tabla pedidos")

12. Para visualizar los campos identificación, nombre, appelidos, de la tabla usuario y nropedido,fechacomprar,fechavencimiento  observación de la tabla pedidos se debe realizar la siguiente intrución sql:

`select usuario.identificacion, usuario.nombre, usuario.apellido, pedidos.Nropedido, pedidos.fechacompra, pedidos.fechavence, pedidos.observacion from usuario inner join pedidos on usuario.identificacion = pedidos.identifiacion`

![Consulta 12](img/14.png "Consulta 12")

13. Para visualizar todos los capos de las tablas usuarios y pedidos donde identificacion sea mayor que 100, se debe reaizar la sigueiente instrucción:

`select usuario.*, pedidos.* from usuarios inner join pedidos on usuarios identificacion = pedidos.identificacion where usurio.identificacion > 100`

![Consulta 13](img/15.png "Consulta 13")