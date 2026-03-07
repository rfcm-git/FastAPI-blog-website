# FastAPI Blog Website
  &nbsp;A **RESTful Blog API built with FastAPI** that supports user authentication, blog post management, and secure API endpoints using JWT authentication.
  
  &nbsp;This project demonstrates a modern FastAPI backend architecture using asynchronous database operations, modular routing, and environment-based configuration.

# Features

- User authentication with **JWT tokens**
- Secure password hashing
- Create, read, update, and delete blog posts
- Author–post relationships
- Environment-based configuration using `.env`
- Async database support
- Modular project structure
- Automatic API documentation

---

# Tech Stack

## Backend
- FastAPI  
- SQLAlchemy (Async ORM)  
- Pydantic  
- Pydantic Settings  
- OAuth2 + JWT Authentication  

## Database

- SQLite / PostgreSQL (depending on configuration)

## Other Tools

- Uvicorn  
- Python Virtual Environment  
- `.env` configuration  

---

# Project Structure
```
FastAPI-blog-website/
├── main.py                # FastAPI application entry point
├── config.py              # Application settings and environment config
├── database.py            # Database connection and session management
├── models.py              # SQLAlchemy database models
├── schemas.py             # Pydantic schemas for validation
├── auth.py                # Authentication and JWT utilities
├── routers/
│   ├── posts.py           # Blog post routes
│   └── users.py           # User authentication and management routes
├── .env                   # Environment variables
├── requirements.txt       # Project dependencies
└── README.md              # Project documentation
```

---

# Installation

## 1. Clone the Repository

```bash
git clone https://github.com/rfcm-git/FastAPI-blog-website.git
cd FastAPI-blog-website
```


## 2. Create Virtual Environment

```bash
python -m venv .venv
```
  ### Activate it:
  - **Windows**
```bash
.venv\Scripts\activate
```
  - **Mac/Linux**
```bash
source .venv/bin/activate
```

## 3. Install Dependencies
&nbsp;&nbsp;pip install -r requirements.txt

### Environment Variables
&nbsp;&nbsp;Create a `.env` file in the root directory:

```
  SECRET_KEY=your-secret-key
  ALGORITHM=HS256
  ACCESS_TOKEN_EXPIRE_MINUTES=30
  DATABASE_URL=sqlite+aiosqlite:///./blog.db
  Running the Application
```

#### Run the development server:
```bash
uvicorn main:app --reload
```

#### Server will start at:
```bash
http://127.0.0.1:8000
```

#### API Documentation
```bash
FastAPI automatically generates API documentation.
```

#### Swagger UI:
```bash
http://127.0.0.1:8000/docs
```

#### ReDoc:
```bash
http://127.0.0.1:8000/redoc
```

#### Example API Endpoints
 - Authentication
    - POST /users/register
    - POST /users/login
 - Posts
    - GET /posts
    - GET /posts/{id}
    - POST /posts
    - PUT /posts/{id}
    - DELETE /posts/{id}
    
#### Authentication Flow

1. User registers or logs in.
2. API returns a JWT access token.
3. Token is sent in request headers:
```bash
  Authorization: Bearer <token>
```
4. Protected endpoints validate the token.

#### Example Request
  ##### Create a post:
```
{
	"title": "My First Blog",
	"content": "This is my first FastAPI blog post."
}
```
### Future Improvements
  - Pagination
  - Comments system
  - File/image uploads
  - Role-based access control
  - Docker support
  - Unit tests
  - Deployment configuration

### Learning Goals
  - This project demonstrates:
  - FastAPI project structuring
  - Async SQLAlchemy usage
  - JWT authentication
  - Dependency injection
  - API design best practices

## License
This project is open-source and available under the MIT License.
=======
# FastAPI-blog-website
About FastAPI Blog Engine A high-performance, async REST API built with FastAPI &amp; PostgreSQL. Features a multi-layered security stack using Argon2 &amp; JWT. Engineered with Pydantic-Settings for env management and SQLAlchemy (Async) for database ops. Implements strict schema validation, CRUD logic, pagination, and image processing (Pillow).
