Nun muss noch eine Datenbank erstellt werden, in der die Informationen gespeichert werden sollen.  
Mit `docker exec -it mariaDbContainer bash`{{execute}} gelangen wir auf die Konsole innerhalb des Containers.  
Dann gelangen wir mit `mysql -h localhost -u root -p`{{execute}} auf die MariaDB Console um mit der Datenbank zu kommunizieren. Zunächst wird aber zur Eingabe des Passworts aufgefordert `pass`{{execute}}.  
Nun zeigen wir uns alle aktuellen Datenbanken an. `SHOW DATABASES \g`{{execute}}  
Um die Daten speichern zu können erstellen wir eine neue Datenbank. `CREATE DATABASE daten \g`{{execute}}