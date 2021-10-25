Herzlich willkommen zu diesem Scenario.  
## Beschreibung
Ausgangslage ist eine JSON Datei. Diese beinhaltet Daten eines Sensors. Ein solches Format ist heute oft Standard beim Datenaustausch von z.B. Sensordaten. Diese Daten könnten fortlaufend als JSON Dateien abgelegt und gespeichert werden. Aus meiner Erfahrung werden Daten oft in Datenbanken gespeichert. Um dies konsequent fort zu setzen bietet es sich ebenso an diese Daten im JSON Format in einer Datenbank zu speichern. Dadurch können diese wie gewöhnlich abgefragt und ausgewertet werden.  

Genau diesen Weg von JSON in die Datenbank werden wir in diesem Scenario gehen. Es werden Daten aus einer Datei im JSON Format in eine Datenbank eingefügt.  
Dazu wird in deisem Scenario zunächst ein Datenbankserver in einem Docker Container bereitgestellt. Anschließend eine Python Umgebung vorbereitet um die Daten im JSON-Format aus einer Datei einzulesen. Diese Daten werden dann in der Datenbank gespeichert.

## Voraussetzungen
Du solltest schon einmal ein Terminal in einem Linux System verwendet haben. Ebenso sind grundlegende Kenntnisse mit Python von Vorteil. Auch die Funktionsweise von Relationalen Datenbanken und einfaches SQL sollte bekannt sein.
