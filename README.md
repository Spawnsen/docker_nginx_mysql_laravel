# Programmierumgebung in Docker mit nginx und mySQL

Laravel Umgebung in Docker mit nginx &amp; mysql

1. ZIP herunterladen und entpacken
  Bsp.: C:\docker\laravel\....
  
2. Konsole aufrufen und in den Ordner mit der "docker-compose.yml" wechseln

3. Folgenden Befehl ausführen: "docker-compose build"

4. Warten bis alles heruntergeladen und bereit ist.

5. Mit "docker-compose up -d" den Container starten

6. Mit "docker-compose exec app bash" in die bash des Containers wechseln

7. Folgenden Befehl eingeben um Laravel herunterzuladen "composer create-project --prefer-dist laravel/laravel ."

8. Nun sollten im Ordner /www/ die Laravel Dateien zu finden sein und mit der Adresse http://127.0.0.1 solltest du die Laravel Startseite sehen können

9. Die .env Datei im Laravel Projekt bearbeiten und die folgenden Daten eintragen:
  DB_CONNECTION=mysql
  DB_HOST=database
  DB_PORT=3306
  DB_DATABASE=laravel
  DB_USERNAME=user
  DB_PASSWORD=secret

10. Den Befehl "php artisan migrate" in der bash des Containers aufrufen

11. Nun sollte Laravel deine Datenbank mit den Standardwerten beschrieben haben.

12. Loslegen :-)




Quelle: https://liquid.fish/current/creating-a-simple-laravel-docker-environment
