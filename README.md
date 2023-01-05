# Final Project Binar Academy

## Back-End Member

- John Tri Putra Sihombing
- Muhammad Umar Mansyur
- Achmad Fadilla

---

<!-- ## Develop The Repository

## How to make a PR & merge

1. Pull the latest changes (main branch)
   `git pull origin main`
2. Make some change to file you want to change, add, or delete.
3. Make your own branch, with format:
   1. If it `feature`: `feature_yourname_featurename`
   2. If it `bug fix`: `fix_yourname_bugname`
   3. Command: `git checkout -b your_own_branch`
4. Git add
   `git add .`
5. Git commit with format `feature/fix: your_feature/your_bug_name`
   `git commit -m your_commit`
6. Git push to your branch
   `git push origin your_branch`
7. Make PR to Github web.
8. Back to main branch
   `git checkout main`

## If you want to change your branch code

1. Go to your branch that other collaborators comments.
   `git checkout your_own_branch`
2. Make some change to file you want to change, add, or delete.
3. Git add
   `git add .`
4. Git commit with format `feature/fix: your_feature/your_bug_name`
   `git commit -m your_commit`
5. Git push to your branch
   `git push origin your_branch`
6. Make PR to Github web.
7. Back to main branch
   `git checkout main` -->

# Final Project Binar Academy

## Back-End Member

- John Tri Putra Sihombing
- Muhammad Umar Mansyur
- Achmad Fadilla

---

<!-- ## Develop The Repository

## How to make a PR & merge

1. Pull the latest changes (main branch)
   `git pull origin main`
2. Make some change to file you want to change, add, or delete.
3. Make your own branch, with format:
   1. If it `feature`: `feature_yourname_featurename`
   2. If it `bug fix`: `fix_yourname_bugname`
   3. Command: `git checkout -b your_own_branch`
4. Git add
   `git add .`
5. Git commit with format `feature/fix: your_feature/your_bug_name`
   `git commit -m your_commit`
6. Git push to your branch
   `git push origin your_branch`
7. Make PR to Github web.
8. Back to main branch
   `git checkout main`

## If you want to change your branch code

1. Go to your branch that other collaborators comments.
   `git checkout your_own_branch`
2. Make some change to file you want to change, add, or delete.
3. Git add
   `git add .`
4. Git commit with format `feature/fix: your_feature/your_bug_name`
   `git commit -m your_commit`
5. Git push to your branch
   `git push origin your_branch`
6. Make PR to Github web.
7. Back to main branch
   `git checkout main` -->

# REST API Terbang Tinggi

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
