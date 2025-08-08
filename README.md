# Linkly - URL Shortener

A modern URL shortening service built with React and Spring Boot.

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Material-UI](https://img.shields.io/badge/Material_UI-0081CB?style=for-the-badge&logo=material-ui&logoColor=white)

## ✨ Features

- 🔗 **URL Shortening** - Create short, memorable URLs
- 📊 **Analytics** - Track clicks and engagement
- 👤 **User Dashboard** - Manage your URLs with a beautiful interface
- 🔐 **Authentication** - Secure user registration and login
- 📱 **Responsive Design** - Works on all devices
- 🎨 **Modern UI** - Built with Material-UI and Tailwind CSS

## 🚀 Quick Start

### Prerequisites
- Node.js (v18+)
- Java 23
- PostgreSQL

### Backend Setup
```bash
# Clone and setup database
git clone <repository-url>
cd url-shortener-sb

# Configure database in application.properties
# Run the application
mvn spring-boot:run
```

### Frontend Setup
```bash
cd url-shortener-react
npm install
npm run dev
```

Visit `http://localhost:5173` to see the application.

## 🛠️ Tech Stack

**Frontend:**
- React 18 + Vite
- Material-UI + Tailwind CSS
- React Query + Axios
- Chart.js for analytics

**Backend:**
- Spring Boot 3.4.0
- Spring Security + JWT
- PostgreSQL + JPA
- Maven

## 📁 Project Structure

```
Linkly/
├── url-shortener-react/     # React frontend
│   ├── src/components/      # UI components
│   ├── src/api/            # API integration
│   └── src/contextApi/     # State management
└── url-shortener-sb/       # Spring Boot backend
    └── src/main/java/
        ├── controller/      # REST endpoints
        ├── service/         # Business logic
        ├── repository/      # Data access
        └── security/        # Auth & security
```

## 🔧 Configuration

### Database Setup
Update `url-shortener-sb/src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/url_shortener
spring.datasource.username=your_username
spring.datasource.password=your_password
```

### API Configuration
Update `url-shortener-react/src/api/api.js` with your backend URL.

## 📚 API Endpoints

**Auth:**
- `POST /api/auth/register` - Register user
- `POST /api/auth/login` - Login user

**URLs:**
- `POST /api/urls` - Create short URL
- `GET /api/urls` - Get user's URLs
- `DELETE /api/urls/{id}` - Delete URL
- `GET /s/{shortUrl}` - Redirect to original URL

## 🚀 Deployment

**Frontend:**
```bash
cd url-shortener-react
npm run build
```

**Backend:**
```bash
cd url-shortener-sb
mvn clean package
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.

---

**Built with ❤️ using React and Spring Boot**

