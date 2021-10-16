Um die Daten einzulesen verwenden wir Python.  
Dabei werden drei Module benötigt, die mit dem Paketverwaltungsprogramm pip installiert werden. `pip install pandas~=1.3.3 SQLAlchemy~=1.4.25 python-dotenv~=0.19.0`{{execute}}  
Nach erfolgter installation gelangen wir mit `python3`{{execute}} in die Python Konsole und können Python Code ausführen.  
Nun binden wir die Funktion load_dotenv aus dem Modul dotenv ein, dies wir benötigt um auf die gespeicherten Variablen in der Datei zuzugreifen. `from dotenv import load_dotenv`{{execute}}  
Dann das Modul os, welches ebenso für den Zugriff auf die Umgebungsvariaben benötigt wird. `import os`{{execute}}  
Nun wird das Modul sqlalchemy eingebunden, welches die Kommunikation mit der Datenbank ermöglicht. `import sqlalchemy`{{execute}}  
Anschließend das Modul pandas, um die Daten zu lesen. `import pandas`{{execute}}  
Damit sind die notwendigen Vorbereitungen abgeschlossen und wir können mit dem Datenimport beginnen.