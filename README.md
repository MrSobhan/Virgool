# Virgool 📝✨

Welcome to **Virgool**, a vibrant Persian blogging platform built to empower users to share their stories, engage with communities, and discover inspiring content! 🚀 Whether you're a writer, reader, or admin, Virgool offers a seamless and modern experience with a robust API-driven backend. Deployed on Render at [https://virgool.onrender.com](https://virgool.onrender.com), this project is ready to shine! 🌟

## 🎉 Features

Virgool is packed with features to make blogging fun and interactive:

- **User Authentication** 🔐

  - Register and login with email, username, or phone 📧📱
  - JWT-based secure authentication 🛡️
  - Role-based access (user/admin) 👤👑

- **Posts & Content Creation** ✍️

  - Create, update, publish, and delete posts 📜
  - Filter posts by title, paginate results, and prioritize followed topics 🔍
  - Rich post details with author info, topics, likes, and comments 💬

- **Comments** 💭

  - Add, edit, delete, and approve comments (admin-only approval) ✅
  - Nested comments support for engaging discussions 🗣️

- **Topics** 🏷️

  - Follow/unfollow topics to personalize your feed 🌐
  - Admin-managed topic creation, updates, and deletion 🛠️

- **Lists** 📋

  - Create and manage personalized lists of posts 📚
  - Add/remove posts to lists with partial updates 🔄
  - Private or public list options 🔒

- **Likes & Interactions** ❤️

  - Toggle likes on posts with real-time feedback 👍
  - Track engagement with like counts 📊

- **Notifications** 🔔

  - Get notified about new posts, comments, or followed topic updates 📩
  - Mark notifications as read 📬

- **File Uploads** 📤

  - Secure file uploads for profile avatars or post media 🖼️
  - Integrated with Multer` for smooth handling 📁

- **User Management** 👥

  - Follow/unfollow users, ban/unban, and role changes (admin-only) ⚖️
  - Partial profile updates for name, phone, bio, avatar, and more 🔧

- **API Documentation** 📖
  - Interactive Swagger UI at `/api-docs` for easy testing 📚
  - Comprehensive endpoint details with JWT support 📜

---

## � Tech Stack

Virgool is built with a modern, production-ready stack:

- **Backend**: Node.js, Express.js 🚀
- **Database**: MongoDB with Mongoose 🗄️
- **Authentication**: JWT, bcrypt 🔐
- **File Uploads**: Multer 📤
- **API Docs**: Swagger/OpenAPI 📖
- **Deployment**: Render ☁️
- **Validation**: Joi for input validation ✅
- **Environment**: dotenv for secure config 🌐

---

## 🛠️ Getting Started

Follow these steps to set up Virgool locally and start blogging! 📚

### Prerequisites

- Node.js (v18 or higher) 🟢
- MongoDB (local or MongoDB Atlas) 🗄️
- Git 🐙
- A cup of coffee ☕ (optional but recommended!)

### Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/virgool.git
   cd virgool
   ```

2. **Install dependencies**:

   ```bash
   npm install
   ```

3. **Set up environment variables**:
   Create a `.env` file in the root directory and add:

   ```env
   PORT=3000
   MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/virgool?retryWrites=true&w=majority
   JWT_SECRET=your-super-secret-key
   ```

4. **Run the server**:

   ```bash
   npm start
   ```

   The server will run at `http://localhost:3000` 🚀

5. **Explore the API**:
   Visit `http://localhost:3000/api-docs` to interact with the Swagger UI 📖

---

## 🌐 API Endpoints

Here’s a quick overview of the main API routes. Check `/api-docs` for full details! 📚

| Endpoint                   | Method | Description                     | Auth Required? |
| -------------------------- | ------ | ------------------------------- | -------------- |
| `/v1/auth/register`        | POST   | Register a new user             | No             |
| `/v1/auth/login`           | POST   | Login with email/username/phone | No             |
| `/v1/posts`                | GET    | Get paginated posts             | No             |
| `/v1/posts`                | POST   | Create a new post               | Yes            |
| `/v1/comments`             | POST   | Add a comment to a post         | Yes            |
| `/v1/comments/:id/approve` | PATCH  | Approve a comment (admin)       | Yes (Admin)    |
| `/v1/users/:userId/follow` | POST   | Follow a user                   | Yes            |
| `/v1/lists`                | POST   | Create a new list               | Yes            |
| `/v1/topics`               | GET    | Get all topics                  | No             |
| `/v1/upload`               | POST   | Upload a file                   | Yes            |

---

## 🚀 Deployment

Virgool is deployed on Render at [https://virgool.onrender.com](https://virgool.onrender.com). To deploy your own instance:

1. **Push to GitHub**:
   Ensure your code is in a GitHub repository 🐙

2. **Set up Render**:

   - Create a new Web Service in Render ☁️
   - Connect your GitHub repo 📂
   - Add environment variables (`PORT`, `MONGODB_URI`, `JWT_SECRET`) 🔧
   - Deploy! 🚀

3. **Test the API**:
   Access your Swagger docs at `https://your-app.onrender.com/api-docs` 📖

---

## 🧪 Testing

To ensure everything works smoothly:

- **Local Testing**:
  Use Postman or Swagger UI to test endpoints like `/v1/auth/login` or `/v1/posts` 🧪
- **Sample Request** (Login):
  ```bash
  POST http://localhost:3000/v1/auth/login
  Content-Type: application/json
  {
    "email": "test@example.com",
    "password": "password123"
  }
  ```
- **Unit Tests** (Future):
  Add Jest or Mocha for automated testing 🛠️

---

## 🤝 Contributing

We love contributions! 💖 To get started:

1. Fork the repo 🍴
2. Create a new branch (`git checkout -b feature/awesome-feature`) 🌿
3. Commit your changes (`git commit -m "Add awesome feature"`) 📝
4. Push to the branch (`git push origin feature/awesome-feature`) 🚀
5. Open a Pull Request 🎉

Please follow the [Code of Conduct](CODE_OF_CONDUCT.md) 🙌

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details 📄


