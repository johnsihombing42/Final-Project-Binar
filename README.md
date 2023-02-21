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

`Who Am I`

```http
GET /auth/me
```

##### Authorization

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6NDgsInVzZXJuYW1lIjoiam9objEyMyIsImVtYWlsIjoiam9obnNpaG9tYmluZzgwQGdtYWlsLmNvbSIsInJvbGUiOiJVc2VyIiwidXNlcl90eXBlIjoiQmFzaWMiLCJpc192ZXJpZmllZCI6MSwiaWF0IjoxNjcxMDAwNjc0fQ.KD0n4-zxDIcTUGFz1kNMw0riJU6Vb8quU224Erruf0I
```

```json
{
  "status": true,
  "message": "successful authentication",
  "data": {
    "id": 47,
    "username": "john123",
    "email": "johnsihombing80@gmail.com",
    "role": "User"
  }
}
```

## ADMIN

### CRUD Flight

`Create Flight`

```http
POST /flight/data
```

##### Example Request Body

```json
{
{
  "code": "QZ707",
  "airlineIata":"QZ",
  "airlineName": "Air Asia",
  "departureAirport": "Kuala Namu",
  "departure": "KNO",
  "arrivalAirport": "Ngurah Rai",
  "arrival": "DPS",
  "date": "2022-12-30",
  "capacity":250,
  "tripType":"Round_Trip",
  "sc":"Economy",
  "departureTime": "14:00",
  "arrivalTime": "16:35",
  "price": 2500000
}
}
```

##### Response

```json
{
  "status": true,
  "message": "Success create flight",
  "data": {
    "id": 12,
    "code": "QZ787",
    "airlineIata": "QZ",
    "airlineLogo": "https://sta.nusatrip.net/static/img/front/V2/icon-flight/QZ.png",
    "airlineName": "Air Asia",
    "departureAirport": "Kuala Namu",
    "departure": "KNO",
    "arrivalAirport": "Ngurah Rai",
    "arrival": "DPS",
    "date": "2022-12-29",
    "returnDate": null,
    "capacity": 250,
    "tripType": "round_trip",
    "sc": "economy",
    "departureTime": "14:00:00",
    "arrivalTime": "16:35:00",
    "price": 2500000,
    "updatedAt": "2022-12-28T03:11:32.604Z",
    "createdAt": "2022-12-28T03:11:32.604Z"
  }
}
```

`Read Flight`

```http
GET /flight/data
```

##### Response

```json
{
  "status": true,
  "message": "Success get all flight",
  "data": {
    "id": 12,
    "code": "QZ787",
    "airlineIata": "QZ",
    "airlineLogo": "https://sta.nusatrip.net/static/img/front/V2/icon-flight/QZ.png",
    "airlineName": "Air Asia",
    "departureAirport": "Kuala Namu",
    "departure": "KNO",
    "arrivalAirport": "Ngurah Rai",
    "arrival": "DPS",
    "date": "2022-12-29",
    "returnDate": null,
    "capacity": 250,
    "tripType": "round_trip",
    "sc": "economy",
    "departureTime": "14:00:00",
    "arrivalTime": "16:35:00",
    "price": 2500000,
    "updatedAt": "2022-12-28T03:11:32.604Z",
    "createdAt": "2022-12-28T03:11:32.604Z"
  }
}
```

`Update Flight`

```http
PUT /flight/data
```

##### Example Request Body

```json
{
  "code": "ID707",
  "airlineIata": "ID",
  "airlineName": "Batik Air",
  "departureAirport": "Denpasar",
  "departure": "DPS",
  "arrivalAirport": "Soekarno Hatta",
  "arrival": "CGK",
  "date": "2022-12-28",
  "departureTime": "13:00:00+00",
  "arrivalTime": "16:00:00+00",
  "price": "2500000"
}
```

##### Response

```json
{
  "status": true,
  "message": "Success update flight"
}
```

`Delete Flight`

```http
DELETE /flight/data/:id
```

##### Response

```json
{
  "status": true,
  "message": "delete flight success",
  "data": 1
}
```
