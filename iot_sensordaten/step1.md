Zunächst wird eine Datenbank benötigt. Hierfür wird ein RDBMS (Relationales Datenbank Management System) installiert.
Mit einem RDBMS können relationale Datenbanken erstellt, administriert und verwaltet werden.
Dabei speichert eine relationale Datenbank Daten auf einem relationalen Modell. Dies entspricht einer tabellarischen Form.

### Docker
Um ein solches RDBMS zu installieren, verwenden wir einen Docker Container.  
Solche Container stellen eine, vom Host System isolierte Umgebung dar. Docker baut, dabei auf dem Host System auf und stellt darüber die Container Umgebungen bereit. Im Gegensatz zu einem Hypervisor (Typ 1), der direkt auf die Infrastruktur aufsetzt, ohne ein Host System. 
![Docker Container](https://raw.githubusercontent.com/mhh008/katacoda-scenarios/main/assets/docker.png)
Abb. https://www.cloudsavvyit.com/490/what-does-docker-do-and-when-should-you-use-it/

Nun erstellen wir einen solchen Container.
Dazu verwenden wir eine fertige Vorlage (das Image). Diese beinhaltet ein mariaDB System. Im folgenden Command setzen wir einen Namen für den Container (mariaDbContainer), setzen das Passwort für den root Benutzernamen (pass) und definieren den erreichbaren Port, sowie welches Image wir alden wollen. 
`docker run --name mariadbContainer -e MYSQL_ROOT_PASSWORD=pass -p 3308:3308 -d docker.io/library/mariadb:10.4`{{execute}}
Nun läuft unser Datenbankserver im erstellten Container. Mit `docker ps`{{execute}} können wir alle laufenden Container sehen, auch den eben erstellten.

---
Quellen:
https://www.oracle.com/de/database/what-is-a-relational-database/
https://www.storage-insider.de/was-ist-ein-relational-database-management-system-rdbms-a-973087/
https://www.cloudsavvyit.com/490/what-does-docker-do-and-when-should-you-use-it/