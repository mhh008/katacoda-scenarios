Nachdem nun der Import abgeschlossen ist, wollen wir prüfen, ob die Daten auch tatsächlich in der Datenbank gespeichert wurden.  
Dazu wieder die mariaDB Konsole starten `mysql -h $DB_IP -u root -p`{{execute}} und das Passwort **pass** eingeben.  
Dann wählen wir die Datenbank aus `use daten`{{execute}}.  
Zeigen alle darin bestehenden Tabellen an `SHOW TABLES;`{{execute}} und sehen die automatisch erstellte Tabelle **data**.  
Nun führen wir einen SQL Query aus, um den Inhalt der Tabelle zu sehen `SELECT * FROM data;`{{execute}}.  
Nun werden alle Datensätze in dieser Tabelle angezeigt. Die Spaltennamen wurden aus den Spaltennamen des DataFrames übernommen, dieses nutzte die Schlüsselwerte der JSON Objekte.   
Ebenfalls wurde etwa der Zeitstempel im korrekten Format gespeichert, denn er wird wie ein übliches Datum mit Uhrzeit formatiert angezeigt.  
So können nun beliebige Abfragen erstellt werden. Möchte man zum Beispiel alle Datensätze mit einem *value* zwischen 8 und 9 haben kann dies mit folgendem SQL Query erfolgen. `SELECT * FROM data WHERE value BETWEEN 8 AND 9;`{{execute}}  
So sind weitere Abfragen und Auswertungen möglich.    
Nun wieder die Konsole verlassen `\q`{{execute}}. (vgl.[4] Connecting to MariaDB)
