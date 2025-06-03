# Database Schema

## Tables

### users
- id: SERIAL PRIMARY KEY
- email: VARCHAR(255) UNIQUE NOT NULL
- username: VARCHAR(100) UNIQUE NOT NULL
- password_hash: VARCHAR(255) NOT NULL
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

### categories
- id: SERIAL PRIMARY KEY
- name: VARCHAR(100) NOT NULL
- color: VARCHAR(7)
- user_id: INTEGER (FK → users.id)
- created_at: TIMESTAMP

### tasks
- id: SERIAL PRIMARY KEY
- title: VARCHAR(255) NOT NULL
- description: TEXT
- completed: BOOLEAN
- priority: VARCHAR(20)
- due_date: TIMESTAMP
- category_id: INTEGER (FK → categories.id)
- user_id: INTEGER (FK → users.id)
- created_at: TIMESTAMP
- updated_at: TIMESTAMP

## Indexes
- users.email
- users.username
- tasks.user_id
- tasks.due_date
- categories.user_id
