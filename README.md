# Auth to API

https://blog.kata.academy/api

## 1. Регистрируемся (Registration)

### POST /users

```json
{
  "user": {
    "username": "ignasiya",
    "email": "ignasiya@gmail.com",
    "password": "12345678Ru!"
  }
}
```

### 200 Ok

```json
{
  "user": {
    "username": "ignasiya",
    "email": "ignasiya@gmail.com",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY2ZWU3MjBiY2UxOGQwMWIwMDJiMWI3MyIsInVzZXJuYW1lIjoiaWduYXNpeWEiLCJleHAiOjE3MzIwODY3OTUsImlhdCI6MTcyNjkwMjc5NX0.            GO_yCtvPxfCx8QJBbXj-L2v-DUEyhj8n34_fI9Xaxd4"
  }
}
```

![СКРИНШОТ](./images/Снимок%20экрана%202024-09-21%20101353.png)

## 2. Логинимся (Authentication)

### POST /users/login

```json
{
  "user": {
    "email": "ignasiya@gmail.com",
    "password": "12345678Ru!"
  }
}
```

### 200 Ok

```json
{
  "user": {
    "username": "ignasiya",
    "email": "ignasiya@gmail.com",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY2ZWU3MjBiY2UxOGQwMWIwMDJiMWI3MyIsInVzZXJuYW1lIjoiaWduYXNpeWEiLCJleHAiOjE3MzIwODcxMjQsImlhdCI6MTcyNjkwMzEyNH0.xZPqKTSfgVIVfSp1WhDUkyhvvR5-YbkXuoN5ZwGxcF4"
  }
}
```

![СКРИНШОТ](./images/Снимок%20экрана%202024-09-21%20101903.png)

## 3. Получить данные текущего пользователя

### GET /user

```
Authorization: "Token _последний токен_"
```

### 200 Ok

```json
{
  "user": {
    "username": "ignasiya",
    "email": "ignasiya@gmail.com",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY2ZWU3MjBiY2UxOGQwMWIwMDJiMWI3MyIsInVzZXJuYW1lIjoiaWduYXNpeWEiLCJleHAiOjE3MzIwODc0OTAsImlhdCI6MTcyNjkwMzQ5MH0.IeXNNnfqcPWSlfM7LmaHoL0oXZ0usvgrpqNlPVb60v4"
  }
}
```

![СКРИНШОТ](./images/Снимок%20экрана%202024-09-21%20102510.png)
