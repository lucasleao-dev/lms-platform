
# 🎓 LMS Platform — Fullstack (Java 21 + Spring Boot 3 + React)

A complete learning management platform inspired by Alura/Udemy, built with **Java 21**, **Spring Boot 3**, **React**, **PostgreSQL**, **JWT authentication**, and **Docker**.  
This project was developed to demonstrate real-world fullstack architecture, clean code, and strong backend + frontend engineering skills.

---

## 🚀 Technologies

### **Backend — Java 21 + Spring Boot 3**
- Spring Web
- Spring Security + JWT
- Spring Data JPA
- Spring Validation
- PostgreSQL
- Flyway Migrations
- Testcontainers
- JUnit 5 + Mockito
- Swagger / OpenAPI
- Docker

### **Frontend — React + TypeScript**
- React + Vite
- React Router
- Axios
- TailwindCSS (or Material UI)
- Global state (Context API or Zustand)

### **Infrastructure**
- Docker & Docker Compose  
- GitHub Actions (optional CI/CD)  
- API documentation via Swagger  

---

## 🏛 Architecture Overview

The platform is organized in a **monorepo** structure:



/backend
/frontend
/docs
docker-compose.yml
README.md


The backend follows **Clean Architecture / Layered Architecture**:



controller → service → repository → entity → dto


---

## 👤 User Roles (RBAC)

### **Admin**
- Manages users
- Manages all courses
- Access platform reports

### **Instructor**
- Creates/edit courses
- Creates modules and lessons
- Views reviews for their own courses

### **Student**
- Purchases courses
- Watches lessons
- Tracks progress
- Reviews courses

---

## 📚 Main Features

### **Public Area**
- Browse courses
- View course details

### **Student Area**
- Purchase courses
- Watch video lessons
- Save progress automatically
- Leave reviews
- Student dashboard

### **Instructor Area**
- Create courses
- Add modules and lessons
- Edit course content

### **Admin Area**
- Manage users
- Moderate reviews
- View platform metrics

---

## 📂 Database Schema (simplified)

**Entities included:**

- **User**
- **Course**
- **Module**
- **Lesson**
- **StudentCourse (purchases)**
- **Progress**
- **Review**

A full ER diagram is available in `/docs`.

---

## 🧱 API Endpoints (examples)

### **Auth**


POST /auth/register
POST /auth/login


### **Courses**


GET /courses
GET /courses/{id}
POST /courses (instructor)
PUT /courses/{id}


### **Modules & Lessons**


POST /courses/{id}/modules
POST /modules/{id}/lessons
GET /lessons/{id}


### **Progress**


POST /lessons/{id}/finish
GET /progress/course/{id}


### **Reviews**


POST /courses/{id}/reviews
GET /courses/{id}/reviews


---

## 🧪 Testing Strategy

### **Unit Tests**
- JUnit 5  
- Mockito  

### **Integration Tests**
- Testcontainers (PostgreSQL)
- MockMvc + JWT authentication tests

---

## 🐳 Running with Docker

Ensure Docker is installed, then run:

```bash
docker-compose up --build


Backend: http://localhost:8080
Frontend: http://localhost:5173
Swagger: http://localhost:8080/swagger-ui.html

📈 Roadmap

 Full JWT authentication

 Painel do instrutor

 Curso CRUD concluído

 Módulos e aulas

 Upload de vídeo

 Acompanhamento do progresso do aluno

 Sistema de avaliações

 Módulo de pagamentos

 Implantação em produção (Renderização / Ferrovia / AWS)

👨‍💻 Autor

Lucas Souza Leão
Desenvolvedor Fullstack — Java | Bota Primavera | Reagir
