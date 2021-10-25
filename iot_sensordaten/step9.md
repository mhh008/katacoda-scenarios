Nachdem nun der Import abgeschlossen ist, wollen wir prüfen, ob die Daten auch tatsächlich in der Datenbank gespeichert wurden.  
Dazu wieder die mariaDB Konsole starten `mysql -h $DB_IP -u root -p`{{execute}} und das Passwort **pass** eingeben.  
Dann wählen wir die Datenbank aus `use daten`{{execute}}.  
Zeigen alle darin bestehenden Tabellen an `SHOW TABLES;`{{execute}} und sehen die automatisch erstellte Tabelle **data**.  
Nun führen wir einen SQL Query aus, um den Inhalt der Tabelle zu sehen `SELECT * FROM data;`{{execute}}.  
Wie zu sehen ist, wurde die Tabelle mit unseren Daten gefüllt.  
Nun wieder die Konsole verlassen `\q`{{execute}}. (vgl.[4] Connecting to MariaDB)