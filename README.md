# Final Project Binar Academy

## Back-End Member

- John Tri Putra Sihombing
- Muhammad Umar Mansyur
- Achmad Fadilla

---

# REST API Terbang Tinggi

Final Project Independent Study Kampus Merdeka - Binar Academy

Terbang Tinggi App is a place to buy and book flight tickets online, both one way and round trip.

Features:

User :

- [x] Authentication : Register, Login, Google Oauth
- [x] Authorization : Role and Permission
- [x] Edit Profile User
- [x] Search Aiport
- [x] Search Flight
- [x] Search Flight
- [x] Booking Flight
- [x] CRUD Transaction and Payment
- [x] In App Notification
- [x] Print Ticket PDF
- [x] QR Code Ticket

Admin :

- [x] CRUD Flight
- [x] CRUD User
- [x] Pagination and Sorting User
- [x] CRUD Notification

## Install

    npm install

## Run the app

    npm run dev

## Online Documentation

- [Swagger API Documentation](https://terbangtinggi-api-staging.km3ggwp.com/api/docs/)

- [Postman API Documentation](https://documenter.getpostman.com/view/23103147/2s8YsxurAy)

## Docs API

### Auth User

`Register User`

```http
POST /auth/register
```

##### Example Request Body

```json
{
  "username": "john_123",
  "email": "johnsihombing80@gmail.com",
  "password": "tes1234",
  "confirmPassword": "tes1234"
}
```

##### Response

```json
{
  "status": true,
  "message": "account successfully registered",
  "data": {
    "id": 6,
    "username": "Basic",
    "email": "johnsihombing80@gmail.com",
    "role": "User"
  }
}
```

---

`Login User`

```http
POST /auth/login
```

##### Example Request Body

```json
{
  "email": "johnsihombing80@gmail.com",
  "password": "tes1234"
}
```

`Forgot Password`

```http
POST auth/forgot-password
```

##### Example Request Body

```json
{
  "email": "johnsihombing80@gmail.com"
}
```

##### Response

```json
{
  "success": true,
  "message": "Success send email forgot password to user"
}
```
