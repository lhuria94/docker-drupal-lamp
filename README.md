# docker-drupal-lamp
Minimal Drupal 7.x development environment stack.

Basic uses:
1. Place a copy of this file at your Drupal site root.
2. Build it using "docker build -t your_image_name ."
3. Start the web stack: 'docker-compose up -d'
4. To see your running containers: 'docker ps'
5. To get inside the container using bash: 'docker-compose exec web bash'
6. And you are now "inside" the Docker container. Now use Drush to import the database: drush sql-query --db-url=mysql://drupal:drupal@mysql/drupal --file=import.sql
