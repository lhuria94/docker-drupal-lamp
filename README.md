# docker-drupal-lamp
Minimal Drupal 7.x development environment stack. <br/>

How to use:<br/>

1. Place a copy of this <b><i>docker-compose.yml</i></b> file at your Drupal site root or maybe create a folder "docker/".<br/>

2. Build the image using 'docker build -t your_image_name .'<br/>

3. Start the web stack: 'docker-compose up -d'<br/>

4. To see your running containers: <b><i>docker ps</i></b><br/>

5. To get inside the container using bash: 'docker-compose exec web bash'<br/>

6. <b><i>For new installation:</i></b><br/>
Add Database setup instructions while installing Drupal:
  - Database name = 'your_db_name'<br/>
  - Database username = 'root'<br/>
  - Leave database password blank<br/>
  - Expand "Advanced options" and set Database host = 'db' (This is defined in docker-compose.yml file)<br/>

7. <b><i>For existing installation:</i></b><br/>
Import Database using:<br/>
docker exec -i your_db_container mysql -uroot -proot your_db_name < filename.sql

8. Make necessary changes in settings.php

9. <b><i>Run Drush commands with:</i></b>
 - USER_ID=$(id -u) docker-compose run --rm drush $rest_of_the_command 
