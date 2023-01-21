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
POST /auth/forgot-password
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

`Reset Password`

```http
POST /auth/change-password?=token
```

##### Example Request Body

```json
{
  "newPassword": "Tes12345",
  "confirmPassword": "Tes12345"
}
```

##### Response

```json
{
  "status": true,
  "message": "password updated successfully"
}
```

`Login Google`

```http
POST /auth/google
```

##### Example Request Body

```json
{
  "access_token": "ya29.a0AeTM1ie-SkXBb65317yime-6KcRflZmerzaYjm3zNYLS9Y5wjk2u-EVluXQj8yr8Xpp5rtQTjcCKYkomi1qzewcJHJsmPWgPN3fLRBzIYcqXlY2nARlIpFHLMz8VRN2fK3UZyRSQhFy8FmZI9HNFACE1tVg3aCgYKAcoSARISFQHWtWOmfJ8BdPCdMrNouJcD0JcWWg0163"
}
```

##### Response

```json
{
  "status": true,
  "message": "Success get token",
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6NzQsInVzZXJuYW1lIjoiS29tIEJfSm9obiBUcmkgUHV0cmFfIDA1MCIsImVtYWlsIjoiam9obnRyaXNpaG9tYmluZ0BnbWFpbC5jb20iLCJ1c2VyX3R5cGUiOiJHb29nbGUiLCJpYXQiOjE2NzAwNTY0ODV9.89ueO3ZEKGZL-ihkIVYFkN4rCH1b5Dh_R3k42QHBwZk"
}
```
