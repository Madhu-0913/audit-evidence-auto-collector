Interactive Dashboard: Real-time KPI metrics, responsive charts, and an interactive UI that scales perfectly from mobile (375px) to desktop (1280px+).
Secure Authentication: Robust user registration and login flows protected by Spring Security, stateless JSON Web Tokens (JWT), and BCrypt password hashing.
Advanced Filtering & Search: A dedicated logs interface allowing administrators to search through thousands of logs instantly by User, Action type, or Timeframe.
Optimized Database: Built on PostgreSQL with Flyway schema migrations and optimized indexing to completely eliminate N+1 query performance issues.
Security First: Defended against SQL injection via parameterized JPA queries. Dynamic, in-memory cryptographic secret generation ensures zero hardcoded vulnerabilities.
Containerized Deployment: Fully Dockerized architecture (docker-compose) containing multi-stage builds for the backend (Maven + Java) and frontend (Node + Nginx) for instantaneous "Fresh Machine" deployments.

Frontend: React 19, Vite, Tailwind CSS, Recharts, React Router
Backend: Java 17, Spring Boot 3.4, Spring Security, JWT, Maven
Database: PostgreSQL 15, Flyway Migrations, Spring Data JPA
Infrastructure: Docker, Docker Compose, Nginx

Using Docker (Recommended)
You can spin up the entire isolated stack (Database, Backend, and Frontend) with a single command:

bash
docker-compose up --build -d
The application will automatically become available at http://localhost.

Manual Development Setup
Database: Ensure local PostgreSQL is running on port 5432 with a database named audit_db.
Backend: Navigate to the /backend folder and run mvn spring-boot:run. The API will start on port 8082.
Frontend: Navigate to the /frontend folder, run npm install, and then npm run dev. The UI will start on port 5173.
