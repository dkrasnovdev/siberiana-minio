<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/dkrasnovdev/siberiana-public-assets/main/assets/siberiana-logo-dark-background.svg">
    <img src="https://raw.githubusercontent.com/dkrasnovdev/siberiana-public-assets/main/assets/siberiana-logo-dark-background.svg" width="240" height="90" alt="Logo for Siberiana">
  </picture>
</p>

<p align="center">
Siberiana | Aggregator of the Historical and Cultural Heritage of the Yenisei Siberia.
</p>

# Siberiana MinIO Setup

This repository contains configuration files and instructions for setting up a MinIO server with predefined buckets using Docker Compose.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Getting Started

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/dkrasnovdev/siberiana-minio.git
   cd siberiana-minio
   ```

2. Copy the `.env.example` file and rename it to `.env`. Fill in the required environment variables with appropriate values.

   ```bash
   cp .env.example .env
   # Edit .env file with your configuration
   ```

3. Build and Start the Services:

   ```bash
   docker-compose up -d
   ```

   This will start the MinIO server and the bucket creation service.

4. Access MinIO:

   MinIO console will be available at: `http://localhost:9000`. Use the provided access credentials specified in your `.env` file to log in.

5. Clean Up:

   To stop and remove the containers, run:

   ```bash
   docker-compose down -v
   ```

## Files

- `docker/Dockerfile`: Dockerfile for building the MinIO server container.
- `docker-compose.yml`: Docker Compose configuration for MinIO and bucket creation services.
- `.env.example`: Example environment variables file. Create a `.env` file based on this template.

## Customization

You can customize the configuration files to suit your specific requirements. Refer to the official documentation for Docker Compose and MinIO for more advanced configurations.

## Troubleshooting

If you encounter any issues or have questions, please feel free to create an issue on this repository.

## Related Repositories

- [Siberiana GraphQL API](https://github.com/dkrasnovdev/siberiana-api)
- [Siberiana Nginx Setup](https://github.com/dkrasnovdev/siberiana-nginx)
- [Siberiana Keycloak Setup](https://github.com/dkrasnovdev/siberiana-keycloak)
- [Siberiana MinIO Setup](https://github.com/dkrasnovdev/siberiana-minio)
- [Siberiana Public Assets](https://github.com/dkrasnovdev/siberiana-public-assets)
