<div align="center">

# 🏋️ GymPass API

**Node.js + TypeScript API applying SOLID, with full unit and E2E test coverage**

[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![Fastify](https://img.shields.io/badge/Fastify-000000?style=for-the-badge&logo=fastify&logoColor=white)](https://www.fastify.io)
[![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)](https://www.prisma.io)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white)](https://vitest.dev)
[![License: MIT](https://img.shields.io/badge/license-MIT-000000?style=for-the-badge)](./LICENSE)

</div>

## 📖 About

A GymPass-style API: users sign up, find nearby gyms, and check in when they arrive. Built to practice and demonstrate **SOLID** principles, the **repository pattern** (Prisma + in-memory implementations), and a test-first workflow — every use case has unit tests, and the HTTP layer is covered end-to-end.

## ✨ Features

- User registration and authentication (JWT)
- Logged-in user profile
- Check-in count and check-in history per user
- Search gyms within 10km, and by name
- Gym check-in, with validation window and admin approval
- Gym registration (admin only)

## 📐 Business Rules

- A user can't register with a duplicate email
- A user can't check in twice on the same day
- Check-in only allowed within 100m of the gym
- A check-in can only be validated up to 20 minutes after creation
- Only admins can validate a check-in or register a gym

## 🛠 Tech Stack

Node.js · TypeScript · Fastify · Prisma · PostgreSQL · Zod · JWT · bcryptjs · Vitest (unit + E2E) · Docker

## 🚀 Getting Started

```bash
git clone https://github.com/allanaramont/gympass_api.git
cd gympass_api
npm i
```

Start PostgreSQL:

```bash
docker-compose up -d
```

Create the `.env` file and fill in the variables (JWT secret, database URL):

```bash
cp .env.example .env
```

Run the app:

```bash
npm run dev
```

## 🧪 Tests

```bash
npm run test           # unit tests
npm run test:e2e       # end-to-end tests
npm run test:coverage  # coverage report
```

## 📄 License

Distributed under the [MIT License](./LICENSE).

---

<div align="center">

Built by <a href="https://github.com/allanaramont">Allan Monteiro</a>

</div>
