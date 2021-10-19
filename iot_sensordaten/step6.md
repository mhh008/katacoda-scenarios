Mit folgendem Code erstellen wir ein Pandas DataFrame. Dies kann man sich wie eine Tabelle mit Daten vorstellen.  
Dazu rufen wir im Modul Pandas die Funktion read_json auf. Dieser übergeben wir den Speicherort der Sensordaten (sensor_daten.json). Da wir ein Attribut haben, das als Datumswert gelesen werden soll, übergeben wir dies ebenso als Parameter.  
Gespeichert wird das DataFrame in einer Variablen **df**  
`df = pandas.read_json("sensor_data.json", convert_dates=['createdAt'])`{{execute}}

Wenn wir nun die Variablen `df`{{execute}} Aufrufen, wird ein Ausschnitt der Daten angezeigt.
