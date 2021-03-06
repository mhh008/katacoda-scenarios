Um die Datenbank auch erreichen zu können, wird deren IP-Adresse benötigt. Diese speichern wir in einer Variablen **DB_IP**. `DB_IP=$(docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' mariaDbContainer)`{{execute}} (vgl. [3] Setting up MariaDB Docker Deployment)  
Für unser späteres Skript müssen wir diese Information noch in einer Datei sichern. `echo $DB_IP\" >> db_credentials.env`{{execute}}  
Mit `apt install mariadb-client-core-10.1 -y`{{execute}} installieren wir einen Command Line Client um auf den Datenbankserver (mariaDB) zugreifen zu können.  
Für eine bessere Übersicht leeren wir den Inhalt des Terminals. `clear`{{execute}}  
Nun muss noch eine Datenbank erstellt werden, in der die Informationen gespeichert werden sollen.  
Mit `mysql -h $DB_IP -u root -p`{{execute}} gelangen wir auf die MariaDB Konsole, um mit der Datenbank zu kommunizieren.  
Wenn zur Passworteingabe aufgefordert wird, muss das Passwort **eingegeben** werden, dies ist: **pass**  
Nun zeigen wir uns alle aktuellen Datenbanken an. `SHOW DATABASES;`{{execute}}  
Um die Daten speichern zu können erstellen wir eine neue Datenbank. `CREATE DATABASE daten;`{{execute}}  
`SHOW DATABASES;`{{execute}} Jetzt sehen wir in der Liste unsere neu erstellte Datenbank "daten".

Wir verlassen die mariaDB Konsole wieder mit `\q`{{execute}} (vgl. [4] Connecting to MariaDB)  