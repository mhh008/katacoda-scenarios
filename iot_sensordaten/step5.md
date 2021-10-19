Um die Daten einzulesen verwenden wir Python.  
Zunächst wird eine virtuelle Umgeung für Python erstellt und diese dann aktiviert. `virtualenv -p /usr/bin/python3.8 venv && source venv/bin/activate`{{execute}}

Außerdem werden vier Module benötigt, die mit dem Pakteverwaltungsprogramm pip installiert werden. `pip install pymysql mysql-connector-python python-dotenv pandas SQLAlchemy`{{execute}}  
Für eine bessere Übersicht leeren wir den Inhalt des Terminals. `clear`{{execute}}


Nach erfolgter installation gelangen wir mit `./venv/bin/python3`{{execute}} in die Python Konsole und können Python Code ausführen.  
Nun binden wir die Funktion load_dotenv aus dem Modul dotenv ein, dies wird benötigt, um auf die gespeicherten Variablen in der Datei zuzugreifen. `from dotenv import load_dotenv`{{execute}}  
Dann das Modul os, welches ebenso für den Zugriff auf die Umgebungsvariablen benötigt wird. `import os`{{execute}}  
Anschließend das Modul pandas, um die Daten zu lesen. `import pandas`{{execute}}  
Nun wird das Modul sqlalchemy eingebunden, welches die Kommunikation mit der Datenbank vereinfacht. `import sqlalchemy`{{execute}}  
Als letztes das Modul pymysql, dieses wird von sqlalchemy für den Datenbankzugriff verwendet. `import pymysql`{{execute}}  

Damit sind die notwendigen Vorbereitungen abgeschlossen und wir können mit dem Datenimport beginnen.