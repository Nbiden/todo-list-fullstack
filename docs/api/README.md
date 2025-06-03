# API Documentation

## Base URL
- Development: `http://localhost:5000/api`
- Production: `https://api.yourdomain.com`

## Authentication
All authenticated endpoints require a JWT token in the Authorization header:
Authorization: Bearer <token>

## Endpoints

### Authentication
- `POST /auth/register` - Register new user
- `POST /auth/login` - Login user
- `POST /auth/refresh` - Refresh access token
- `POST /auth/logout` - Logout user

### Tasks
- `GET /tasks` - Get all tasks for authenticated user
- `POST /tasks` - Create new task
- `PUT /tasks/:id` - Update task
- `DELETE /tasks/:id` - Delete task

### Categories
- `GET /categories` - Get all categories
- `POST /categories` - Create new category
- `PUT /categories/:id` - Update category
- `DELETE /categories/:id` - Delete category

Detailed endpoint documentation coming soon...
