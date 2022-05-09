# Решение задачи 4.3.9 (JS Core)
## POST https://kata.academy:8021/api/users
### Тело запроса
    {
        "user": {
            "username": "testUserName",
            "email": "test-mail@mail.com",
            "password": "123"
        }
    }

### Ответ (200)
    {
        "user": {
            "username": "testusername",
            "email": "test-mail@mail.com",
            "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYyNzhmZDM2ZmQyMTFjMjEwMGRiMzU3YyIsInVzZXJuYW1lIjoidGVzdHVzZXJuYW1lIiwiZXhwIjoxNjU3MjgwMzEwLCJpYXQiOjE2NTIwOTYzMTB9.seaF3FDdG5I0srR4Mpgb-SdCYTuj9RR5NrUq8IxvbdU"
        }
    }

---

## POST https://kata.academy:8021/api/users/login
### Тело запроса
    {
        "user": {
            "email": "test-mail@mail.com",
            "password": "123"
        }
    }

### Ответ (200)
{
    "user": {
        "username": "testusername",
        "email": "test-mail@mail.com",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYyNzhmZDM2ZmQyMTFjMjEwMGRiMzU3YyIsInVzZXJuYW1lIjoidGVzdHVzZXJuYW1lIiwiZXhwIjoxNjU3MjgwNzQxLCJpYXQiOjE2NTIwOTY3NDF9.q3T0clG0kF-a9QztRNec_gI8MAqYZMLgwwMZoQ367kw"
    }
}

---

## GET https://kata.academy:8021/api/user
### Тело запроса
(Не требуется.)

### Authorization
**Bearer Token**
Token:
    eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYyNzhmZDM2ZmQyMTFjMjEwMGRiMzU3YyIsInVzZXJuYW1lIjoidGVzdHVzZXJuYW1lIiwiZXhwIjoxNjU3MjgwNzQxLCJpYXQiOjE2NTIwOTY3NDF9.q3T0clG0kF-a9QztRNec_gI8MAqYZMLgwwMZoQ367kw

### Ответ (200)
{
    "user": {
        "username": "testusername",
        "email": "test-mail@mail.com",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYyNzhmZDM2ZmQyMTFjMjEwMGRiMzU3YyIsInVzZXJuYW1lIjoidGVzdHVzZXJuYW1lIiwiZXhwIjoxNjU3MjgwOTQxLCJpYXQiOjE2NTIwOTY5NDF9._fKAQ4_n4nAKUyAaA4jma4INsCAfdyjqVkUjlRi-780"
    }
}
