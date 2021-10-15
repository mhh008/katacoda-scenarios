Nun muss noch eine Datenbank erstellt werden, in der die Informationen gespeichert werden sollen.  
Mit `docker exec -it mariaDbContainer bash`{{execute}} gelangen wir auf die Konsole innerhalb des Containers.  
Dann gelangen wir mit `mysql -h localhost -u root -p=pass`{{execute}} auf die MariaDB Console um mit der Datenbank zu kommunizieren.  
Wenn zur Passworteingabe aufgefordert wird muss das Passwort *eingegeben* werden, dies ist: *pass*
Nun zeigen wir uns alle aktuellen Datenbanken an. `SHOW DATABASES \g`{{execute}}  
Um die Daten speichern zu können erstellen wir eine neue Datenbank. `CREATE DATABASE daten \g`{{execute}}