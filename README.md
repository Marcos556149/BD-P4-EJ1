# BD-P4-EJ1
TENIENDO EN CUENTA LA TABLA A:
Create table CIU(
    ciudadid integer NOT NULL,
    ciudadNom VARCHAR(30) NOT NULL,
    PRIMARY KEY(ciudadid)
);
Create table PERS(
    id integer NOT NULL,
    nom VARCHAR(30) NOT NULL,
    idC integer NOT NULL,
    edad integer NOT NULL,
    PRIMARY KEY(id),
    FOREIGN KEY(idC) REFERENCES CIU(ciudadid) on update cascade on delete restrict  
);
Insertar ciudades con los siguientes datos:
< 1,'Estambul' >
< 2,'Roma' >
< 3,'Barcelona' >
< 4,'Praga' >
  
INSERT INTO CIU VALUES
(1,'Estambul');
INSERT INTO CIU VALUES
(2,'Roma');
INSERT INTO CIU VALUES
(3,'Barcelona');
INSERT INTO CIU VALUES
(4,'Praga');

Insertar tuplas en la tabla Personas con los siguientes datos:
< 1,'Juan Manuel Ariza',1,16 >
< 2,'Santiago Manrique',2, 25>
< 3,'Luciano Perez',5, 50 >
< 4,'Andrea Hernández',1 >
< 5,'Ana Perez',1,30 >

INSERT INTO PERS VALUES
(1,'Juan Manuel Ariza',1,16);
INSERT INTO PERS VALUES
(2,'Santiago Manrique',2,25);
INSERT INTO PERS VALUES
(3,'Luciano Perez',5,50);
INSERT INTO PERS VALUES
(4,'Andrea Hernandez',1);
INSERT INTO PERS VALUES
(5,'Ana Perez',1,30);

Ejecutar las siguientes consultas:

a. Muestre el nombre de las ciudades ordenadas alfabéticamente.
b. Muestre las personas (todos los datos) mayores de edad.
c. Muestre la cantidad de personas.
d. Muestre la cantidad de ciudades.
e. Eliminar la ciudad con identificador igual a 1.
f. Muestre la cantidad de ciudades donde viven personas. 

a)- SELECT ciudadnom from CIU order by ciudadnom
b)- SELECT * from PERS WHERE edad >= 18
c)- SELECT count(*) from PERS
d)- SELECT count(*) from CIU
e)- DELETE from CIU WHERE ciudadid=1
f)- SELECT count(distinct idc) from pers
TENIENDO EN CUENTA LA TABLA B:
Create table CIU(
    ciudadid integer NOT NULL,
    ciudadNom VARCHAR(30) NOT NULL,
    PRIMARY KEY(ciudadid)
);
create table pers(
	id integer NOT NULL,
	nom VARCHAR(30) NOT NULL,
	idc integer NOT NULL,
	edad integer NOT NULL,
	PRIMARY KEY(id),
	FOREIGN KEY(idc) REFERENCES ciu(ciudadid) on delete set null on update restrict
);

Insertar ciudades con los siguientes datos:
< 1,'Estambul' >
< 2,'Roma' >
< 3,'Barcelona' >
< 4,'Praga' >

INSERT INTO CIU VALUES
(1,'Estambul');
INSERT INTO CIU VALUES
(2,'Roma');
INSERT INTO CIU VALUES
(3,'Barcelona');
INSERT INTO CIU VALUES
(4,'Praga');

Insertar tuplas en la tabla Personas con los siguientes datos:
< 1,'Juan Manuel Ariza',1,16 >
< 2,'Santiago Manrique',2, 25>
< 3,'Luciano Perez',5, 50 >
< 4,'Andrea Hernández',1 >
< 5,'Ana Perez',1,30 >

INSERT INTO PERS VALUES
(1,'Juan Manuel Ariza',1,16);
INSERT INTO PERS VALUES
(2,'Santiago Manrique',2,25);
INSERT INTO PERS VALUES
(3,'Luciano Perez',5,50);
INSERT INTO PERS VALUES
(4,'Andrea Hernandez',1);
INSERT INTO PERS VALUES
(5,'Ana Perez',1,30);

Ejecutar las siguientes consultas:

a. Muestre el nombre de las ciudades ordenadas alfabéticamente.
b. Muestre las personas (todos los datos) mayores de edad.
c. Muestre la cantidad de personas.
d. Muestre la cantidad de ciudades.
e. Eliminar la ciudad con identificador igual a 1.
f. Muestre la cantidad de ciudades donde viven personas. 

a)- select ciudadnom from ciu order by ciudadnom
b)- select * from pers where edad >= 18
c)- select count(*) from pers
d)- select count(*) from ciu
e)- delete from ciu where ciudadid=1;
f)- select count(distinct idc) from pers
