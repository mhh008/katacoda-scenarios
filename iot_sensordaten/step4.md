Hier sehen wir einen Ausschnitt aus den einzulesenden Sensordaten:
```JSON
{  
    "createdAt":"2021-10-09T15:49:46.518Z",  
    "value":"8.00",  
    "lat":48.769373,  
    "lon":9.175632,  
    "boxName":"Airrohr-1769933",  
    "boxId":"5a99c5a8bc2d410019cb8261",  
    "exposure":"outdoor",  
    "unit":"µg/m³",  
    "sensorId":"5a99c5a8bc2d410019cb8264",  
    "sensorType":"SDS 011"  
}  
```
Die Daten liegen im JSON Format vor. Dabei handelt es sich um ein standardisiertes Format.  
JSON steht für Java Script Object Notation. Diese wurde 2001, als Datenaustauschformat entwickelt. Es ist einfacher und kompakter im Vergleich zu XML.  
Ein JSON Objekt besteht aus verschachtelten Key: Value (Schlüssel: Werte) Paaren. Bekannte Strukturen wir Arrays [] können auch in JSON verwendet werden. (vgl. Buckenhofer, Andreas, Lecture@DHBW: Internet der Dinge, 04 Kommunikationsprotokolle, Seite 47 ff.)  
Im Folgenden lesen wir eine Array an solchen Objekten aus einer .json Datei ein.
