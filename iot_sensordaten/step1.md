Zunächst wird eine Datenbank benötigt. Hierfür wird ein RDBMS (Relationales Datenbank Management System) installiert.
Mit einem RDBMS können relationale Datenbanken erstellt, administriert und verwaltet werden.
Dabei speichert eine relationale Datenbank Daten auf einem relationalen Modell. Dies entspricht einer tabellarischen Form.

### Docker
Um ein solches RDBMS zu installieren, verwenden wir einen Docker Container.
![Docker ]


Abb. https://www.cloudsavvyit.com/490/what-does-docker-do-and-when-should-you-use-it/

Zunächst wird eine Datenbank benötigt, in der die Daten gespeichert werden.  
Hierzu werden wir einen Docker Container erstellen, in welchem ein mariaDB Datenbankserver erstellt wird.  
Dazu erstellen wir einen Container mit folgendem Command: `docker run --name mariadbContainer -e MYSQL_ROOT_PASSWORD=pass -p 3308:3308 -d docker.io/library/mariadb:10.4`{{execute}}  
Nun haben wir einen Container mit einem laufenden Relationalen Datenbank Management System. 
Mit `docker ps`{{execute}} sehen wir den laufenden Container.


https://www.oracle.com/de/database/what-is-a-relational-database/
https://www.storage-insider.de/was-ist-ein-relational-database-management-system-rdbms-a-973087/