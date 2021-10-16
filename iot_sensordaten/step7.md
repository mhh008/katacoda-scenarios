Um die in der Datei gespeicherten Variablen nutzen zu können, binden wir diese als Umgebungsvariablen ein. `load_dotenv("db_credentials.env")`{{execute}}  
Nun müssen wir eine Verbindung zu unserer erstellten Datenbank herstellen.  
Dazu wird die url für die Verbindung aus den verschiedenen Komponenten zusammengebaut. `engine_string = f"mysql://{os.getenv('DB_USER')}:{os.getenv('DB_PASSWORD')}@{os.getenv('DB_HOST')}:{os.getenv('DB_PORT')}/{os.getenv('DB_DATABASE')}"`{{execute}}  






    
    df = pd.read_json("./data/sensor_data.json", convert_dates=['createdAt'])

    engine = sqlalchemy.create_engine("mysql://root:@localhost:3306/IOTKATACODA")
    # if_exists: if_exists{‘fail’, ‘replace’, ‘append’}, default ‘fail’
    # How to behave if the table already exists.
    # fail: Raise a ValueError.
    # replace: Drop the table before inserting new values.
    # append: Insert new values to the existing table.
    # dies kann dann je nach tatsächlicher anwendung ersetzt werden
    df.to_sql('data', con=engine, index=False, if_exists='replace')

    engine.dispose()