# E-Commerce Application — Cloud & DevOps Deployment

A containerized 3-tier e-commerce application deployed on an AWS EC2 instance using Docker and Docker Compose.

## Architecture

```text
                    Internet
                       |
                       v
                 AWS EC2 Instance
                       |
                    :3001
                       |
                       v
              +----------------+
              |    Frontend    |
              | React + Nginx  |
              +----------------+
                       |
                    /api/*
                       |
                       v
              +----------------+
              |    Backend     |
              | Node.js/Express|
              +----------------+
                       |
                    :5432
                       |
                       v
              +----------------+
              |   PostgreSQL   |
              +----------------+
                       |
                       v
              Docker Persistent
                    Volume


