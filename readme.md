# 🍺 Beers API - NestJS + MongoDB Backend

A simple RESTful API built with **NestJS** and **MongoDB** for managing beers, their ingredients, and alcohol content (ABV). This project is structured with clean separation of concerns using modules, DTOs, services, and repositories — making it scalable and maintainable.

---

## 🚀 Features

- ✅ Create a beer with name, ingredients, and ABV
- 📖 Retrieve a list of all beers
- ❌ Delete a beer by ID
- 🔍 Input validation using class-validator
- 🧪 E2E testing with Jest & Supertest
- 🌱 Environment configuration using `.env` files
- ✅ Type-safe with TypeScript
- ⚙️ ESLint & Prettier integration

---

## 🛠 Tech Stack

- **Backend Framework**: [NestJS](https://nestjs.com/)
- **Database**: [MongoDB](https://www.mongodb.com/)
- **ODM**: [Mongoose](https://mongoosejs.com/)
- **Validation**: [class-validator](https://github.com/typestack/class-validator)
- **Testing**: Jest + Supertest
- **Language**: TypeScript
- **Linting/Formatting**: ESLint, Prettier

---

## 📁 Project Structure & Flow

```

src/
├── app.module.ts         # Root module
├── main.ts               # Entry point
└── beers/                # Feature module
├── beers.module.ts
├── beers.controller.ts
├── beers.service.ts
├── beers.repository.ts
├── beers.schema.ts
└── beers.dto.ts

````

### 🧭 Request Flow

1. **Client** sends HTTP request to `/beers`
2. **BeersController** handles the route and delegates to service
3. **BeersService** processes logic and interacts with repository
4. **BeersRepository** communicates with MongoDB via Mongoose
5. Response sent back to the client

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/beers-api.git
cd beers-api
````

### 2. Install Dependencies

```bash
npm install
```

### 3. Create Environment File

Create a `.development.env` file in the root with the following:

```env
DATABASE_URI=mongodb://localhost:27017/beersdb
```

> Make sure MongoDB is running locally or update the URI accordingly.

### 4. Run the Application

```bash
npm run start:dev
```

The server will start on `http://localhost:3000`.

---

## 🧪 Running Tests

### Run E2E Tests:

```bash
npm run test:e2e
```

---

## 📬 API Endpoints

| Method | Endpoint     | Description       |
| ------ | ------------ | ----------------- |
| GET    | `/beers`     | Get all beers     |
| POST   | `/beers`     | Create new beer   |
| DELETE | `/beers/:id` | Delete beer by ID |

### 📤 Example JSON for POST `/beers`:

```json
{
  "name": "Lager",
  "ingredients": ["Barley", "Hops", "Water", "Yeast"],
  "abv": 5.2
}
```

---

## 👨‍💻 Developer Notes

* The project uses **ESLint** for static code analysis and **Prettier** for formatting.
* You can customize validation logic inside `beers.dto.ts`.
* Unit and integration tests can be extended for other endpoints.
* Built with scalability in mind using modular structure.

---

## 📃 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

Built with ❤️ using [NestJS](https://nestjs.com/) and [MongoDB](https://www.mongodb.com/).

```
