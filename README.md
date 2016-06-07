# docker-drupal-lamp
Minimal Drupal 7.x development environment stack. <br/>

Basic uses:<br/>
1. Place a copy of this file at your Drupal site root.<br/>
2. Build it using 'docker build -t your_image_name .'<br/>
3. Start the web stack: 'docker-compose up -d'<br/>
4. To see your running containers: 'docker ps'<br/>
5. To get inside the container using bash: 'docker-compose exec web bash'<br/>
6. And you are now "inside" the Docker container. Now use Drush to import the database: <br/>
drush sql-query<br/> --db-url=mysql://drupal:drupal@mysql/drupal --file=import.sql<br/>
