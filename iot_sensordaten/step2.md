Um ein solches RDBMS zu installieren, verwenden wir einen Docker Container.  
Solche Container stellen eine vom Host System isolierte Umgebung dar. Docker baut dabei auf dem Host System auf und stellt darüber die Container Umgebungen bereit.  
Im Gegensatz zu einem Hypervisor (Typ 1), der direkt auf die Infrastruktur aufsetzt, ohne ein Host System. (vgl. [2] What Does Docker Do, and When Should You Use It?)  
![Architektur Docker Container im Vergleich zu Hypervisor Typ 1](https://raw.githubusercontent.com/mhh008/katacoda-scenarios/main/iot_sensordaten/assets/docker.png)
Abb. https://www.cloudsavvyit.com/490/what-does-docker-do-and-when-should-you-use-it/  
  
Nun erstellen wir einen solchen Container.  
Dazu verwenden wir eine fertige Vorlage (das Image). Diese beinhaltet ein mariaDB System.  
Im folgenden Command setzen wir einen Namen für den Container (mariaDbContainer), setzen das Passwort für den root Benutzer (pass) und definieren den erreichbaren Port, sowie welches Image wir laden wollen.  
`docker run --name mariaDbContainer -e MYSQL_ROOT_PASSWORD=pass -p 3308:3308 -d docker.io/library/mariadb:10.4`{{execute}}  
Nun läuft unser Datenbankserver im erstellten Container. Mit `docker ps`{{execute}} können wir alle laufenden Container sehen, auch den eben erstellten. (vgl. [3] Setting up MariaDB Docker Deployment)