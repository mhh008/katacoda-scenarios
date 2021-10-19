Um die Daten einzulesen verwenden wir Python.  
Zunächst wird eine virtuelle Umgeung für Python erstellt und diese dann aktiviert. `virtualenv -p /usr/bin/python3.8 venv && source venv/bin/activate`{{execute}}

Außerdem werden vier Module benötigt, die mit dem Pakteverwaltungsprogramm pip installiert werden. `pip install python-dotenv==0.19.1 pandas==1.3.4 SQLAlchemy==1.4.25 pymysql==1.0.2`{{execute}}  
Für eine bessere Übersicht leeren wir den Inhalt des Terminals. `clear`{{execute}}


Nach erfolgter installation gelangen wir mit `./venv/bin/python3`{{execute}} in die Python Konsole und können Python Code ausführen.  
Nun binden wir die Funktion load_dotenv aus dem Modul dotenv ein, dies wird benötigt, um auf die gespeicherten Variablen in der Datei zuzugreifen. `from dotenv import load_dotenv`{{execute}}  
Dann das Modul os, welches ebenso für den Zugriff auf die Umgebungsvariablen benötigt wird. `import os`{{execute}}  
Anschließend das Modul pandas, um die Daten zu lesen. `import pandas`{{execute}}  
Nun wird das Modul sqlalchemy eingebunden, welches die Kommunikation mit der Datenbank vereinfacht. `import sqlalchemy`{{execute}}  
Das installierte Modul pymysql, wird unter der Hand von sqlalchemy für den Datenbankzugriff verwendet.

Damit sind die notwendigen Vorbereitungen abgeschlossen und wir können mit dem Datenimport beginnen.