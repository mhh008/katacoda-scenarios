Um die in der Datei gespeicherten Variablen nutzen zu können, binden wir diese als Umgebungsvariablen ein. `load_dotenv("db_credentials.env")`{{execute}}  
Nun müssen wir eine Verbindung zu unserer erstellten Datenbank herstellen.  
Dazu wird die url für die Verbindung aus den verschiedenen Komponenten zusammengebaut. `engine_string = f"mysql://{os.getenv('DB_USER')}:{os.getenv('DB_PASSWORD')}@{os.getenv('DB_HOST')}:{os.getenv('DB_PORT')}/{os.getenv('DB_DATABASE')}"`{{execute}}  

Für die Verbindung erstellen wir nun eine engine. `engine = sqlalchemy.create_engine(engine_string)
`{{execute}}