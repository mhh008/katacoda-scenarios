Zunächst wird eine Datenbank benötigt, in der die Daten gespeichert werden.  
Hierzu werden wir einen docker Conteiner erstellen, in welchem ein mariaDB Datenbankserver erstellt wird.  
Dazu erstellen wir einen Container mit folgendem Command: `docker run --name mariadbContainer -e MYSQL_ROOT_PASSWORD=pass -p 3308:3308 -d docker.io/library/mariadb:10.4`{{execute}}  
Nun haben wir einen Container mit einem laufenden Relationalen Datenbank management System. Mit `docker ps`{{execute}} sehen wir den laufenden Container.