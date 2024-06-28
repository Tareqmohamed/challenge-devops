# Challenge Setup



## Running the Application

1. Clone the repository:

    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```



2. Start the application using Docker Compose:

    ```sh
    docker compose up --build
    ```
3. Install Laravel dependencies
    ```sh
    docker compose exec api php artisan cache:clear
    docker compose exec api php artisan config:clear
    docker compose exec api composer update
    docker compose exec api php artisan key:generate
    ```
4.  Run the database migrations:
    ```sh
    docker compose exec api php artisan migrate:fresh --seed
    ```
5. Access the application:

    - Client: [https://localhost](https://localhost)
    - API: [https://localhost/api](https://localhost/api)

## Screenshots

1. docker-compose running screenshot

![docker-compose runing screenshot](./screenshots/Screenshot%20from%202024-06-26%2010-33-54.png)

2. client screenshot

![client screenshot](./screenshots/Screenshot%20from%202024-06-26%2010-31-25.png)

3.  API screenshot (changed port from 80 to 443 and ran through https)

![api screenshot](./screenshots/Screenshot%20from%202024-06-26%2010-32-26.png)

4. ssl  screenshot

![ssl screenshot](./screenshots/ssl.png)


[![Docker Image CI](https://github.com/Tareqmohamed/challenge-devops/actions/workflows/main.yml/badge.svg)](https://github.com/Tareqmohamed/challenge-devops/actions/workflows/main.yml)
