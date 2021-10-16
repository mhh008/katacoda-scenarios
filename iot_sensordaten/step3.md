Um die Datenbank auch erreichen zu können benötigen wir deren IP Adresse. Diese speichern wir in einer Variablen **DB_IP**. `DP_IP=$(docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' mariaDbContainer)`{{execute}}  
Für unser späteres Skript schreiben wir diese Variable noch in eine Datei: `echo DB_HOST="$(DP_IP)" >> .env`{{execute}}
Mit `apt install mariadb-client-core-10.3 -y`{{execute}} installieren wir einen Command Line Client um auf den Datenbankserver (mariaDB) zugreifen zu können.  
Nun muss noch eine Datenbank erstellt werden, in der die Informationen gespeichert werden sollen.  
Mit `mysql -h $DP_IP -u root -p`{{execute}} gelangen wir auf die MariaDB Konsole um mit der Datenbank zu kommunizieren.  
Wenn zur Passworteingabe aufgefordert wird muss das Passwort **eingegeben** werden, dies ist: **pass**  
Nun zeigen wir uns alle aktuellen Datenbanken an. `SHOW DATABASES \g`{{execute}}  
Um die Daten speichern zu können erstellen wir eine neue Datenbank. `CREATE DATABASE daten \g`{{execute}}  
`SHOW DATABASES \g`{{execute}} Jetzt sehen wir in der Liste unsere neu erstellte Datenbank "daten".

Wir verlassen die mariaDB Konsole wieder mit `\q`{{execute}}