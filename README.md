# Docker Setup for Existing Simple Laravel Application

This guide will walk you through setting up all the required Docker containers for your existing Simple Laravel Application, including MySQL, PHP, and Redis. If you have a Laravel application already running and want to containerize it using Docker, you're just a few steps away from achieving it.

## Prerequisites

- Make sure you already have a `.env` file in your project's root directory with your Laravel application's configurations.

## Getting Started

Follow these steps to containerize your Laravel application:

1. **Download the Required Files:**

   Download the Docker-related files provided in this repository and place them in your Laravel project's root directory.

2. **Configure .env File:**

   Ensure that your project's `.env` file contains the necessary configurations for your Laravel application.

3. **Set MySQL Version:**

   In your `.env` file, add the following value to specify the MySQL version you want to use:

   ```env
   DB_MYSQL_VERSION=8.0
   ```

4. **Set PHP Version:**

   Open the `Dockerfile` in the project's root directory and set your desired PHP version on line number 1.

5. **Build the Docker Containers:**

   Open your terminal and navigate to your project's root directory. Run the following command to build the Docker containers:

   ```sh
   docker-compose up --build
   ```

   This command will build and start the Docker containers for your Laravel application.

6. **Run in Detached Mode (Optional):**

   If you want to run the containers in detached mode (in the background), you can use the following command:

   ```sh
   docker-compose up -d
   ```

   This will allow you to continue using your terminal without the containers' output.

With these steps completed, your Laravel application should now be running within Docker containers, including MySQL, PHP, and Redis. You can access your application by navigating to 127.0.0.1:8000 in your web browser.

Feel free to customize the Docker configuration files according to your project's specific requirements.
