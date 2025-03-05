# Deploy Webman in Server

1. **Clone Repository** :

   ```bash
   git clone [repository name]
   ```

2. **Setup Environment**:

   - Buat file `.env` di folder `./webman`. Dan isi dengan konfigurasi yang sesuai.
   - (optional) hanya untuk keperluan development. Jika ingin meng-copy vendor yang ada pada container ke local storage, jalankan perintah ini.

     ```bash
     docker cp [container_name/container_id]:/webman/vendor ./webman
     ```

3. **Jalankan Docker Compose**:

   ```bash
   docker-compose up -d --build
   ```

   atau

   ```bash
   docker compose up -d --build
   ```

4. **Akses Aplikasi**:

- Web API akan berjalan di

    ```bash
    http://localhost:8787
    ```

- Gunakan Postman atau sejenisnya untuk mengakses endpoint API.
