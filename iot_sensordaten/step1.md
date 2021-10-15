Zunächst wird eine Datenbank benötigt, in der die Daten gespeichert werden.  
Hierzu werden wir einen Docker Container erstellen, in welchem ein mariaDB Datenbankserver erstellt wird.  
Dazu erstellen wir einen Container mit folgendem Command: `docker run --name mariadbContainer -e MYSQL_ROOT_PASSWORD=pass -p 3308:3308 -d docker.io/library/mariadb:10.4`{{execute}}  
Nun haben wir einen Container mit einem laufenden Relationalen Datenbank Management System. 
Mit `docker ps`{{execute}} sehen wir den laufenden Container.

## RDBMS - Relationales Datenbank Management System
Ein RDBMS ist ein System mit dem sich relationale Datenbanken erstellen, administrieren und verwalten lassen.  
Eine relationale Datenbank ist speichert Daten auf einem relationalen Modell. Dies entspricht einer tabellarischen Form.


https://www.oracle.com/de/database/what-is-a-relational-database/
https://www.storage-insider.de/was-ist-ein-relational-database-management-system-rdbms-a-973087/