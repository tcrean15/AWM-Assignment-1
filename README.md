# GeoUpdate - Interactive Location-Based Note Sharing Platform

## Overview
GeoUpdate is a sophisticated web application built with Django and GeoDjango that enables users to create, share, and interact with location-based notes on an interactive map. The application combines modern web technologies with robust geospatial capabilities to deliver a seamless user experience.

## Features

### Core Functionality
- 🗺️ Interactive map interface powered by Leaflet.js
- 📍 Create and share location-based notes
- 💬 Real-time commenting system
- 🎯 Precise geolocation tracking
- 👤 User authentication and authorization
- 🔒 Secure data handling with CSRF protection

### Technical Features
- Responsive design with Bootstrap 5
- Real-time location updates
- PostGIS spatial database integration
- Docker containerization
- Nginx reverse proxy with SSL/TLS
- Automated certificate management with Certbot

## Technology Stack

### Backend
- Django 4.1
- GeoDjango
- PostgreSQL with PostGIS
- Python 3.8
- Gunicorn

### Frontend
- Leaflet.js for mapping
- Bootstrap 5
- jQuery
- Font Awesome icons
- Custom CSS with CSS variables

### Infrastructure
- Docker & Docker Compose
- Nginx
- Certbot for SSL
- Conda environment management

## Installation

### Prerequisites
- Docker and Docker Compose
- Conda (for local development)
- PostGIS-enabled PostgreSQL database

### Setup Steps

1. Clone the repository:
bash
git clone https://github.com/tcrean15/AWM-Assignment-1
cd geodjango_tutorial

2. Create a `.env` file with required variables:
```env
SECRET_KEY=your_secret_key
DEBUG=False
ALLOWED_HOSTS=your_domain,localhost
DB_NAME=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
```

3. Build and start the Docker containers:
```bash
docker-compose up --build
```

### Local Development Setup

1. Create Conda environment:
```bash
conda env create -f ENV.yml
conda activate awm_env
```

## Project Structure

### Key Components
- `/world` - Main Django application
- `/static` - Static assets (CSS, JS)
- `/templates` - HTML templates
- `/nginx` - Nginx configuration
- `docker-compose.yml` - Container orchestration

### Models
The application uses several key models:
- `WorldBorder` - Geographical boundary data
- `Profile` - User profile with location data
- `LocationNote` - Location-based notes
- `NoteComment` - Note commenting system

## Security Features

### Authentication & Authorization
- User authentication system
- Session management
- Permission-based access control

### Security Headers
- CSRF protection
- SSL/TLS encryption
- Secure cookie handling
- XSS protection

## API Endpoints

### Authentication
- `GET/POST /login/` - User login
- `GET/POST /signup/` - User registration
- `GET /logout/` - User logout

### Note Management
- `GET /map/` - Main map interface
- `POST /add_note/` - Create new note
- `GET /get-notes/` - Retrieve all notes
- `POST /edit_note/<id>/` - Edit existing note
- `POST /delete_note/<id>/` - Delete note

### Comments
- `POST /add_comment/<id>/` - Add comment to note
- `POST /delete_comment/<id>/` - Delete comment

