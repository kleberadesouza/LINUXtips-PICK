## Dockerfile Description

This Dockerfile uses a multi-stage build process to create a lightweight image for running a Python Flask application. 

- **Stage 1 (Build):** Uses `cgr.dev/chainguard/python:latest-dev` to create a virtual environment and install dependencies from `requirements.txt`.
- **Stage 2 (Run):** Uses `cgr.dev/chainguard/python:latest` to copy the virtual environment, application files, and static assets. It sets the environment path, exposes port 5000, and configures Flask to run on all network interfaces.

The resulting image is optimized for production with minimal size and dependencies.
--------------------------------------------------------------------------------------------------------------------------------------------------


## Instructions

You need to have Docker installed on your machine. For installation guidance, refer to the [Docker documentation](https://docs.docker.com/engine/install/).

To start the application, follow these steps:

1. Clone the repository:

    ```shell
    git clone https://github.com/kleberadesouza/LINUXtips-PICK.git
    ```

2. Use Docker Compose to start the application and the Redis container:

    ```shell
    docker compose up -d
    ```

3. The application will be available at [http://localhost:5000](http://localhost:5000/).

---

Security and vulnerability testing has been performed using Trivy.

- For more information about Trivy, visit [Trivy](https://trivy.dev/).
- Trivy needs to be installed.

   Execute:
   
   ```shell
   trivy image trivykleberadesouza/linuxtips-giropops-senhas:1.0
   ```
![Descrição da Imagem](/image.png)