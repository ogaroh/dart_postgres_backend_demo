# Dart Frog BFF Example

[![style: very good analysis][very_good_analysis_badge]][very_good_analysis_link]
[![License: MIT][license_badge]][license_link]
[![Powered by Dart Frog](https://img.shields.io/endpoint?url=https://tinyurl.com/dartfrog-badge)](https://dartfrog.vgv.dev)

A REST API backend built with Dart Frog framework for task and user management. This project demonstrates a full-featured backend API with authentication, database integration, and CRUD operations.

## Features

- **User Authentication**: JWT-based authentication with registration and login endpoints
- **Task Management**: Complete CRUD operations for task management
- **PostgreSQL Integration**: Database layer with connection management and models
- **Security**: Password hashing with bcrypt and secure authentication middleware
- **Repository Pattern**: Clean architecture with separated data access layer
- **API Structure**: RESTful API design with organized routing

## Tech Stack

- **Framework**: [Dart Frog](https://dartfrog.vgv.dev) - A fast, minimalist backend framework for Dart
- **Database**: PostgreSQL with `postgres` package for database connectivity
- **Authentication**: JWT tokens with `dart_jsonwebtoken` and `dart_frog_auth`
- **Security**: Password hashing with `bcrypt`
- **Testing**: Unit testing with `test` package and mocking with `mocktail`
- **Code Quality**: Static analysis with `very_good_analysis`

## Project Structure

```
lib/
├── database/          # Database connection and configuration
├── models/            # Data models for API responses, tasks, and users
├── repositories/      # Data access layer with repository pattern
└── utils/            # Utility functions and helpers

routes/
├── api/
│   ├── authentication/  # Login and registration endpoints
│   └── tasks/          # Task CRUD endpoints
└── index.dart         # Main route handler
```

## API Endpoints

- `POST /api/authentication/register` - User registration
- `POST /api/authentication/login` - User login
- `GET /api/tasks` - Get all tasks
- `POST /api/tasks` - Create a new task

## Getting Started

1. Ensure you have Dart SDK installed (>=3.0.0)
2. Install dependencies: `dart pub get`
3. Set up your PostgreSQL database
4. Configure database connection in `lib/database/db.dart`
5. Run the server: `dart_frog dev`

The API will be available at `http://localhost:8080`

[license_badge]: https://img.shields.io/badge/license-MIT-blue.svg
[license_link]: https://opensource.org/licenses/MIT
[very_good_analysis_badge]: https://img.shields.io/badge/style-very_good_analysis-B22C89.svg
[very_good_analysis_link]: https://pub.dev/packages/very_good_analysis