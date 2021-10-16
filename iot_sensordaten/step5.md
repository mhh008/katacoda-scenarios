Um die Daten einzulesen verwenden wir Python.  
Dabei werden zwei Module benötigt, die mit dem Paketverwaltungsprogramm pip installieren. `pip install pandas~=1.3.3 SQLAlchemy~=1.4.25`{{execute}}  
Nach erfolgter installation gelangen wir mit `python3`{{execute}} in die Python Konsole und können Python Code ausführen.  
Nun binden wir zunächst das Modul sqlalchemy ein, dies vereinfacht die Kommunikation mit der Datenbank. `import sqlalchemy`{{execute}}  
Anschließend das Modul pandas, welches das Lesen der Daten vereinfacht. `import pandas`{{execute}}  
Damit sind die notwendigen Vorbereitungen abgeschlossen und wir können mit dem Datenimport beginnen.