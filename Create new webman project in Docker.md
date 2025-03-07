# Create New Webman Project in Docker

1. **Using template from last existing webman docker project**.
2. On file **docker-compose.yml** :

   - `container_name : your-project-name` <= _rename_
   - `# - /webman/vendor` <= _comment this line_

3. On file **phpwebman.docker** : ( _comment this two line in bottom_ )

   - `# RUN composer install --ignore-platform-reqs`
   - `# CMD ["php", "start.php", "start"]`

4. **Running the docker compose** :

   ```bash
   docker compose up -d --build
   ```

5. **Create webman project** :

   ```bash
   docker exec [container_id/name] composer create-project workerman/webman .
   ```

6. **Install default plugins** :

   ```bash
   docker exec [container_id/name] composer require webman/database workerman/crontab firuze/jwt vlucas/phpdotenv phpmailer/phpmailer webman/push aws/aws-sdk-php polarising/bcrypt webman/redis illuminate/events
   ```

7. On file **docker-compose.yml** :

   - `- /webman/vendor` <= _un-comment this line_

8. On file **phpwebman.docker** : (_un-comment this two line in bottom_)

   - `RUN composer install --ignore-platform-reqs`
   - `CMD ["php", "start.php", "start"]`

9. **Restart the docker compose** :

   ```bash
   docker compose down
   ```

   ```bash
   docker compose up -d --build
   ```

## Folder Structure

```bash
\ (root)
L docker
   L php-webman
   L redis (optional)
   L nginx (optional)
L webman
L docker-compose.yml
```
