# User Management API

A simple REST API built with **Node.js**, **Express.js**, **Prisma ORM**, and **MySQL** for creating and retrieving users.

---

## Tech Stack

* Node.js
* Express.js
* Prisma ORM v6
* MySQL

---

## Prerequisites

Before running this project, make sure you have installed:

* Node.js (v18 or later recommended)
* MySQL Server
* Git

---

## Installation

### 1. Clone the repository

```bash
git clone <repository-url>
cd <project-folder>
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create a `.env` file

Create a `.env` file in the project root and add:

```env
DATABASE_URL="mysql://root:@localhost:3306/prisma_demo"
```

> Update the username, password, database name, host, or port if your MySQL configuration is different.

### 4. Create the database

Create a MySQL database named:

```text
prisma_demo
```

You can create it using MySQL or phpMyAdmin.

### 5. Run Prisma migrations

Since this project already contains migrations, run:

```bash
npx prisma migrate dev
```

This will create all required tables in your database.

### 6. Generate the Prisma Client

```bash
npx prisma generate
```

### 7. Start the server

```bash
node index.js
```

The API will be available at:

```text
http://localhost:3000
```

---

# API Endpoints

## Create User

**POST** `/users`

Request Body

```json
{
  "name": "John Doe",
  "email": "john@example.com"
}
```

Response

```json
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com"
}
```

---

## Get All Users

**GET** `/users`

Response

```json
[
  {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com"
  }
]
```

---

# Project Structure

```text
.
├── prisma
│   ├── migrations
│   └── schema.prisma
├── index.js
├── package.json
├── package-lock.json
├── .env.example
└── README.md
```

---

# Useful Prisma Commands

Generate Prisma Client

```bash
npx prisma generate
```

Apply existing migrations

```bash
npx prisma migrate dev
```

Open Prisma Studio

```bash
npx prisma studio
```

---

# License

This project is available for learning and educational purposes.