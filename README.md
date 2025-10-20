# 🧩 MyHub API

A modern backend API built with **NestJS + Prisma + PostgreSQL**, running inside a **Docker** environment.

This project was created as part of a professional **FullStack learning journey**, focused on improving backend fundamentals, database integration, and clean API documentation.

---

## 🚀 Getting Started

### 🧱 Requirements

Make sure you have the following installed:

- [Node.js](https://nodejs.org/en/) (v18 or higher)
- [Docker](https://www.docker.com/)
- [Git](https://git-scm.com/)
- [PostgreSQL](https://www.postgresql.org/) *(optional if not using Docker)*

---

### ⚙️ Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/myhub.git
   cd myhub
   ```

2. **Start the database using Docker**
   ```bash
   docker-compose up -d
   ```
   > The PostgreSQL instance will run on `localhost:5433`.

3. **Install dependencies**
   ```bash
   npm install
   ```

4. **Configure environment variables**
   Create a `.env` file in the root directory:
   ```env
   DATABASE_URL="postgresql://myhub:myhub123@localhost:5433/myhub"
   ```

5. **Initialize Prisma**
   ```bash
   npx prisma generate
   npx prisma migrate dev --name init
   ```

6. **Run the development server**
   ```bash
   npm run start:dev
   ```
   > Your API will be available at [http://localhost:3000](http://localhost:3000)

---

## 📦 Tech Stack

| Technology | Purpose |
|-------------|----------|
| [NestJS](https://nestjs.com/) | Modular and scalable backend framework |
| [Prisma](https://www.prisma.io/) | Type-safe ORM for Node.js |
| [PostgreSQL](https://www.postgresql.org/) | Relational database |
| [Docker](https://www.docker.com/) | Containerized environment |
| [TypeScript](https://www.typescriptlang.org/) | Static typing and developer safety |

---

## 🧩 Project Structure

```
myhub/
 ┣ src/
 ┃ ┣ modules/
 ┃ ┃ ┣ users/
 ┃ ┃ ┃ ┣ users.controller.ts
 ┃ ┃ ┃ ┣ users.service.ts
 ┃ ┃ ┃ ┗ dto/
 ┃ ┣ main.ts
 ┃ ┗ app.module.ts
 ┣ prisma/
 ┃ ┗ schema.prisma
 ┣ .env
 ┣ docker-compose.yml
 ┣ package.json
 ┗ README.md
```

---

## 🧪 Useful Commands

| Command | Description |
|----------|-------------|
| `npm run start:dev` | Run the API in development mode |
| `npx prisma studio` | Open Prisma’s visual database editor |
| `npx prisma migrate dev --name <name>` | Create and apply a new database migration |
| `docker-compose up -d` | Start containers in detached mode |
| `docker-compose down` | Stop and remove all containers |

---

## 📚 API Documentation (Swagger)

Swagger integration will be configured in **Week 2**, once we create the first module (`Users`).

After configuration, the docs will be available at:  
👉 [http://localhost:3000/api](http://localhost:3000/api)

---

## 🧠 Development Notes

- All environment variables are stored in `.env`
- Always keep Prisma and your database schema in sync using migrations
- Follow NestJS modular architecture:
  - Controllers: define routes and handle requests
  - Services: contain all business logic
  - DTOs: define and validate input data
- Use `class-validator` for input validation
- Avoid putting logic inside controllers

---

## 🧾 License

This project is for educational and professional development purposes — feel free to use and modify it.

---

✍️ **Author:** Henrique Silva  
📅 **Started:** October 2025  
🔗 **Stack:** NestJS · Prisma · PostgreSQL · Docker
