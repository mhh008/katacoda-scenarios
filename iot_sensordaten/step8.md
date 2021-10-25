Im finalen Teil speichern wir nun die eingelesenen Daten, also unser DataFrame in der Datenbank.  

Dazu wird die Funktion *to_sql* am DataFrame df aufgerufen.  
Erster Parameter ist der Name der Tabelle in der Datenbank, dann die engine für die Datenbankverbindung. Mit *index=False* wird verhindert, das der Zeilenindex des DataFrames auch gespeichert wird. Der letzte Parameter gibt an was Python tun soll, wenn die Tabelle in der Datenbank bereits existiert:
- replace: Tabelle wird ersetzt
- fail: Es wird eine Exception / Fehler geworfen
- append: Daten werden an die bestehenden angefügt  
Für dieses Beispiel verwenden wir *replace*  
`df.to_sql('data', con=engine, index=False, if_exists='replace')`{{execute}} (vgl. [12] pandas.DataFrame.to_sql)    

Nun kann die Engine, also die Verbindung wieder geschlossen werden. `engine.dispose()`{{execute}}  
Mit `quit()`{{execute}} verlassen wir Python.