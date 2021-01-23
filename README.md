# H1 Programmierumgebung in Docker mit nginx und mySQL


## Datenquelle

Diese Anleitung baut auf dem Tutorial von ANTHONY PROTANO [Art of README](https://liquid.fish/current/creating-a-simple-laravel-docker-environment) auf.


## Verwendung

1. ZIP herunterladen und entpacken
  Bsp.: C:\docker\laravel\....
  
2. Konsole aufrufen und in den Ordner mit der "docker-compose.yml" wechseln

3. Den Container zusammenstellen `docker-compose build`


4. Warten bis alles heruntergeladen und bereit ist.

5. Den Container starten `docker-compose up -d`

6. In die bash des Containers wechseln `docker-compose exec app bash`

7. Laravel herunterladen `composer create-project --prefer-dist laravel/laravel .`

8. Nun sollten im Ordner /www/ die Laravel Dateien zu finden sein und mit der Adresse http://127.0.0.1 solltest du die Laravel Startseite sehen können

9. Die .env Datei im Laravel Projekt bearbeiten und die folgenden Daten eintragen:
```javascript
DB_CONNECTION=mysql
DB_HOST=database
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=user
DB_PASSWORD=secret
```

10. Die Datenban per artisan migrieren `php artisan migrate`

11. Nun sollte Laravel deine Datenbank mit den Standardwerten beschrieben haben.

12. Loslegen :-)


## Dank und Quellen

https://liquid.fish/current/creating-a-simple-laravel-docker-environment
