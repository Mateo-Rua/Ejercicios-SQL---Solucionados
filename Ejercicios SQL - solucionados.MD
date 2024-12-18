# Ejercicios - Departamentos, empleados

# Departamentos: Contiene información sobre las áreas o divisiones dentro de una organización.

# Empleados: Almacena los detalles de las personas que trabajan en los distintos departamentos



## <span style="color:aqua">Desarrollo</span>

Creamos la base de datos con nombre EMPRESA
```sql
 create database EMPRESA
```

indicamos que vamos a usar la base de datos llamada EMPRESA
```sql
 USE  EMPRESA
```

Creamos  la tabla departamentos
```sql
CREATE TABLE departamentos (
  codDepto varchar(4),
  nombreDpto varchar(20) ,
  ciudad varchar(15) ,
  codDirector varchar(12),

) 
```


Agregamos la infrmacion de los departamentos a la taba departamentos 
```sql
INSERT INTO departamentos VALUES ('1000','GERENCIA','CIUDAD REAL','31.840.269');
INSERT INTO departamentos VALUES ('1500','PRODUCCIÓN','CIUDAD REAL','16.211.383');
INSERT INTO departamentos VALUES ('2000','VENTAS','CIUDAD REAL','31.178.144');
INSERT INTO departamentos VALUES ('2100','VENTAS','BARCELONA','16.211.383');
INSERT INTO departamentos VALUES ('2200','VENTAS','VALENCIA','16.211.383');
INSERT INTO departamentos VALUES ('2300','VENTAS','MADRID','16.759.060');
INSERT INTO departamentos VALUES ('3000','INVESTIGACIÓN','CIUDAD REAL','16.759.060');
INSERT INTO departamentos VALUES ('3500','MERCADEO','CIUDAD REAL','22.222.222');
INSERT INTO departamentos VALUES ('4000','MANTENIMIENTO','CIUDAD REAL','333.333.333');
INSERT INTO departamentos VALUES ('4100','MANTENIMIENTO','BARCELONA','16.759.060');
INSERT INTO departamentos VALUES ('4200','MANTENIMIENTO','VALENCIA','16.759.060');
INSERT INTO departamentos VALUES ('4300','MANTENIMIENTO','MADRID','16.759.060');
```

Creamos la tabla empleados
```sql
CREATE TABLE empleados (
  nDIEmp varchar(12),
  nomEmp varchar(30),
  sexEmp char(1) ,
  fecNac date ,
  fecIncorporacion date ,
  salEmp float ,
  comisionE float ,
  cargoE varchar(15) ,
  jefeID varchar(12) ,
  codDepto varchar(4) ,
) 
```

Agregamos la infrmacion de los empleados a la taba empleados
```sql
INSERT INTO empleados VALUES ('1.130.222','José Giraldo','M','1985-01-20','2000-11-01',1200000,400000,'Asesor','22.222.222','3500');
INSERT INTO empleados VALUES ('1.130.333','Pedro Blanco','M','1987-10-28','2000-10-01',800000,3000000,'Vendedor','31.178.144','2000');
INSERT INTO empleados VALUES ('1.130.444','Jesús Alfonso','M','1988-03-14','2000-10-01',800000,3500000,'Vendedor','31.178.144','2000');
INSERT INTO empleados VALUES ('1.130.555','Julián Mora','M','1989-07-03','2000-10-01',800000,3100000,'Vendedor','31.178.144','2200');
INSERT INTO empleados VALUES ('1.130.666','Manuel Millán','M','1990-12-08','2004-06-01',800000,3700000,'Vendedor','31.178.144','2300');
INSERT INTO empleados VALUES ('1.130.777','Marcos Cortez','M','1986-06-23','2000-04-16',2550000,500000,'Mecánico','333.333.333','4000');
INSERT INTO empleados VALUES ('1.130.782','Antonio Gil','M','1980-01-23','2010-04-16',850000,1500000,'Técnico','16.211.383','1500');
INSERT INTO empleados VALUES ('1.751.219','Melissa Roa','F','1960-06-19','2001-03-16',2250000,2500000,'Vendedor','31.178.144','2100');
INSERT INTO empleados VALUES ('11.111.111','Irene Díaz','F','1979-09-28','2004-06-01',1050000,200000,'Mecánico','333.333.333','4200');
INSERT INTO empleados VALUES ('16.211.383','Luis Pérez','M','1956-02-25','2000-01-01',5050000,0,'Director','31.840.269','1500');
INSERT INTO empleados VALUES ('16.759.060','Darío Casas','M','1960-04-05','1992-11-01',4500000,500000,'Investigador','31.840.269','3000');
INSERT INTO empleados VALUES ('19.709.802','William Daza','M','1982-10-09','1999-12-16',2250000,1000000,'Investigador','16.759.060','3000');
INSERT INTO empleados VALUES ('22.222.222','Carla López','F','1975-05-11','2005-07-16',4500000,500000,'Jefe Mercadeo','31.840.269','3500');
INSERT INTO empleados VALUES ('22.222.333','Carlos Rozo','M','1975-05-11','2001-09-16',750000,500000,'Vigilante','31.840.269','3500');
INSERT INTO empleados VALUES ('31.174.099','Diana Solarte','F','1957-11-19','1990-05-16',1250000,500000,'Secretaria','31.840.269','1000');
INSERT INTO empleados VALUES ('31.178.144','Rosa Angulo','F','1957-03-15','1998-08-16',3250000,3500000,'Jefe Ventas','31.840.269','2000');
INSERT INTO empleados VALUES ('31.840.269','María Rojas','F','1959-01-15','1990-05-16',6250000,1500000,'Gerente',NULL,'1000');
INSERT INTO empleados VALUES ('333.333.333','Elisa Rojas','F','1979-09-28','2004-06-01',3000000,1000000,'Jefe Mecánicos','31.840.269','4000');
INSERT INTO empleados VALUES ('333.333.334','Marisol Pulido','F','1979-10-01','1990-05-16',3250000,1000000,'Investigador','16.759.060','3000');
INSERT INTO empleados VALUES ('333.333.335','Ana Moreno','F','1992-01-05','2004-06-01',1200000,400000,'Secretaria','16.759.060','3000');
INSERT INTO empleados VALUES ('333.333.336','Carolina Ríos','F','1992-02-15','2000-10-01',1250000,500000,'Secretaria','16.211.383','1500');
INSERT INTO empleados VALUES ('333.333.337','Edith Muñoz','F','1992-03-31','2000-10-01',800000,3600000,'Vendedor','31.178.144','2100');
INSERT INTO empleados VALUES ('444.444','Abel Gómez','M','1939-12-24','2000-10-01',1050000,200000,'Mecánico','333.333.333','4300');
INSERT INTO empleados VALUES ('737.689','Mario Llano','M','1945-08-30','1990-05-16',2250000,2500000,'Vendedor','31.178.144','2300');
INSERT INTO empleados VALUES ('768.782','Joaquín Rosas','M','1947-07-07','1990-05-16',2250000,2500000,'Vendedor','31.178.144','2200');
INSERT INTO empleados VALUES ('888.888','Iván Duarte','M','1955-08-12','1998-05-16',1050000,200000,'Mecánico','333.333.333','4100');
```

# Después de crear la base de datos y las tablas, avanzamos a la escritura de consultas, manipulación de datos y administración de estructuras de bases de datos, todo ello a través de una serie de ejercicios diseñados para poner en práctica y consolidar estos conceptos.



1. Obtener los datos completos de los empleados.
```sql
select * from empleados
```


2. Obtener los datos completos de los departamentos
```sql
SELECT * FROM departamentos 
```


3. Obtener los datos de los empleados con cargo 'Secretaria'.
```sql
select * from empleados where cargoE = 'Secretaria'
```



4. Obtener el nombre y salario de los empleados.
```sql
select * from empleados
select nomEmp ,salEmp from empleados 
```



5. Obtener los datos de los empleados vendedores, ordenado por nombre.
```sql
select * from empleados where cargoE = 'Vendedor' ORDER BY nomEmp asc 
```



6. Listar el nombre de los departamentos
```sql
SELECT * FROM departamentos 
select  nombreDpto from departamentos 
select distinct nombreDpto from departamentos -- los  lista sin repetir departamento
```



7. Obtener el nombre y cargo de todos los empleados, ordenado por salario
```sql
select * , (salEmp  + comisionE) as pago_total from empleados 
```



8. Listar los salarios y comisiones de los empleados del departamento 2000, ordenado por comisión
```sql
select salEmp,comisionE from empleados where codDepto = 2000 order by comisionE
```



9. Listar todas las comisiones
```sql
select  distinct comisionE from empleados 
``` 



10. Obtener el valor total a pagar que resulta de sumar a los empleados del departamento 3000 una
bonificación de 500.000, en orden alfabético del empleado
```sql
select nomEmp,salEmp,500.00 as bonificacion ,(salEmp+500000) as Total_a_pagar from empleados where codDepto = 3000 order by nomEmp
```



11. Obtener la lista de los empleados que ganan una comisión superior a su sueldo.
```sql
select nomEmp,salEmp,comisionE from empleados where comisionE > salEmp
```



12. Listar los empleados cuya comisión es menor o igual que el 30% de su sueldo.
```sql
select nomEmp,salEmp,comisionE,(salEmp * 0.3) as porcentaje30_salario from empleados where comisionE <= (salEmp * 0.3)
```


13. Elabore un listado donde para cada fila, figure ‘Nombre’ y ‘Cargo’ antes del valor respectivo para cada empleado.
```sql
select nomEmp as empleado,cargoE as cargo from empleados
```



14. Hallar el salario y la comisión de aquellos empleados cuyo número de documento de identidad es superior al '19.709.802'
```sql
select salEmp, comisionE, nDiEmp from empleados where nDiEmp > '19.709.802'
```


15. Muestra los empleados cuyo nombre empiece entre las letras J y Z (rango).
Liste estos empleados y su cargo por orden alfabético.
```sql
select nomEmp,cargoE from empleados where nomEmp   between 'J%' and   'Z%'   order by nomEmp asc
```


16. Listar el salario, la comisión, el salario total (salario + comisión), documento de identidad del
empleado y nombre, de aquellos empleados que tienen comisión superior a 1.000.000, ordenar el
informe por el número del documento de identidad
```sql
 select salEmp, comisionE,(salEmp+comisionE) as salario_total, nDiEmp,nomEmp from empleados where comisionE > 1000000  order by nDiEmp asc
```


 17. Obtener un listado similar al anterior, pero de aquellos empleados que NO tienen comisión
 ```sql
 select salEmp, comisionE,(salEmp+comisionE) as salario_total, nDiEmp,nomEmp from empleados where comisionE = 0 order by nDiEmp asc
```


 18. Hallar los empleados cuyo nombre no contiene la cadena "MA"
 ```sql
 select nomEmp from empleados  where  nomEmp   not like  '%MA%'   
```


 19. Obtener los nombres de los departamentos que no sean “Ventas” ni “Investigación” NI
'MANTENIMIENTO', ordenados por ciudad.
```sql
 select nombreDpto,ciudad from departamentos where nombreDpto not in ('Ventas','Investigación','MANTENIMIENTO') order by ciudad
```



20. Obtener el nombre y el departamento de los empleados con cargo 'Secretaria' o 'Vendedor', que
no trabajan en el departamento de “PRODUCCION”, cuyo salario es superior a $1.000.000,
ordenados por fecha de incorporación.
```sql
select nomEmp , codDepto,cargoE, fecIncorporacion, salEmp  from empleados 
where cargoE in ('Secretaria','Vendedor') and  codDepto not in  (1500)  and salEmp > 1000000 
order by fecIncorporacion
```


21. Obtener información de los empleados cuyo nombre tiene exactamente 11 caracteres
```sql
select nomEmp, len(nomEmp) as cant_caracteres from empleados where len(nomEmp) = 11 
```


22. Obtener información de los empleados cuyo nombre tiene menos de 11 caracteres
```sql
select nomEmp, len(nomEmp) as cant_caracteres from empleados where len(nomEmp) < 11
```


23. Listar los datos de los empleados cuyo nombre inicia por la letra 'M', su salario es mayor a $800.000
o reciben comisión y trabajan para el departamento de 'VENTAS'
```sql
select * from empleados where nomEmp like 'M%' and  (salEmp > 800000 or comisionE > 0) and codDepto between 2000 and 2300 
```


24. Obtener los nombres, salarios y comisiones de los empleados que reciben un salario situado entre la
mitad de la comisión la propia comisión
```sql
select nomEmp, salEmp,comisionE from empleados where salEmp between  (comisionE/2) and comisionE
```


25. Mostrar el salario más alto de la empresa.
```sql
select max(salEmp) as salario_maximo from empleados 
SELECT nomEmp,salEmp from empleados  where salEmp = 6250000
```


26. Mostrar cada una de las comisiones y el número de empleados que las reciben. Solo si tiene comision.
```sql
select comisionE,count(*) as cant_empleados  from empleados   group by comisionE having  comisionE > 0 
```


27. Mostrar el nombre del último empleado de la lista por orden alfabético.
```sql
select nomEmp from empleados order by nomEmp desc 
```


28. Hallar el salario más alto, el más bajo y la diferencia entre ellos.
```sql
select min(salEmp) as salario_minimo,max(salEmp) as salario_maximo, (max(salEmp) -min(salEmp)) as diferencia   from empleados 
```


29. Mostrar el número de empleados de sexo femenino y de sexo masculino, por departamento.
```sql
select d.nombreDpto,e.sexEmp, count(e.sexEmp) as cantidad from empleados e, departamentos d where e.codDepto = d.codDepto group by d.nombreDpto,e.sexEmp
```


30. Hallar el salario promedio por departamento.
```sql
select codDepto , avg(salEmp) as sal_promedio  from empleados   group by codDepto -- este da el valor promedio de cada departamento en cada ciudad
```


31. Mostrar la lista de los empleados cuyo salario es mayor o igual que el promedio de la empresa.
Ordenarlo por departamento.
calculando el promedio
```sql
select  avg(salEmp) from empleados
select  nomEmp, salEmp,codDepto  from empleados where 2115384 < salEmp order by codDepto
```



32. Hallar los departamentos que tienen más de tres empleados. Mostrar el número de empleados de
esos departamentos.
```sql
select  codDepto,  count(nDIEmp) as cant  from empleados group by codDepto having count(nDIEmp) >= 3
```



33. Mostrar el código y nombre de cada jefe, junto al número de empleados que dirige. Solo los que tengan mas de dos empleados (2 incluido)
```sql
select j.nDIEmp,j.nomEmp, count(*) as N_emple
from empleados j join empleados e
on e.jefeID = j.nDIEmp
group by j.nomEmp, j.nDIEmp
order by N_emple desc 
```



34. Hallar los departamentos que no tienen empleados
```sql
select codDepto, count(nomEmp) as cant  from empleados group by codDepto having count(nomEmp) = 1

select d.nombreDpto, e.nomEmp from empleados e join departamentos d
on e.codDepto = d.codDepto group by d.nombreDpto, e.nomEmp having count(e.nomEmp) = 0
```


35. Mostrar el nombre del departamento cuya suma de salarios sea la más alta,
indicando el valor de la suma.
```sql
select top 1 d.nombreDpto, sum(salEmp) as sum_salario  from empleados e join departamentos d
on e.codDepto = d.codDepto group by d.nombreDpto order by  sum(salEmp) desc 
```

