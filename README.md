# URL Shortener Project

A full-stack URL shortening application built with React frontend and Spring Boot backend. This project provides a modern, user-friendly interface for creating and managing shortened URLs with analytics and user authentication.

## 🚀 Features

### Core Functionality
- **URL Shortening**: Create short, memorable URLs from long URLs
- **Custom URLs**: Generate custom short URLs with your preferred alias
- **Click Analytics**: Track clicks and engagement metrics for your shortened URLs
- **QR Code Generation**: Generate QR codes for easy sharing
- **Real-time Dashboard**: Monitor your URL performance with interactive charts

### User Management
- **User Registration & Login**: Secure authentication with JWT tokens
- **User Dashboard**: Personalized dashboard for managing your URLs
- **Private URLs**: Keep your URLs private or make them public
- **Bulk URL Management**: Manage multiple URLs efficiently

### Technical Features
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Modern UI**: Built with Material-UI and Tailwind CSS
- **Real-time Updates**: Live data updates using React Query
- **Secure API**: RESTful API with Spring Security
- **Database Persistence**: PostgreSQL database for reliable data storage

## 🏗️ Architecture

This project follows a modern full-stack architecture:

```
url-shortener-project/
├── url-shortener-react/     # React Frontend
│   ├── src/
│   │   ├── components/      # React components
│   │   ├── api/            # API integration
│   │   ├── contextApi/     # React Context
│   │   └── utils/          # Utility functions
│   └── public/             # Static assets
└── url-shortener-sb/       # Spring Boot Backend
    └── src/main/java/
        └── com/url/shortener/
            ├── controller/  # REST controllers
            ├── service/     # Business logic
            ├── repository/  # Data access layer
            ├── models/      # Entity models
            ├── dtos/        # Data transfer objects
            └── security/    # Authentication & authorization
```

## 🛠️ Technology Stack

### Frontend
- **React 18** - Modern React with hooks
- **Vite** - Fast build tool and dev server
- **React Router** - Client-side routing
- **Material-UI** - Component library
- **Tailwind CSS** - Utility-first CSS framework
- **React Query** - Data fetching and caching
- **Chart.js** - Data visualization
- **Axios** - HTTP client
- **React Hook Form** - Form handling
- **React Hot Toast** - Notifications

### Backend
- **Spring Boot 3.4.0** - Java framework
- **Spring Security** - Authentication and authorization
- **Spring Data JPA** - Data persistence
- **PostgreSQL** - Database
- **JWT** - Token-based authentication
- **Lombok** - Code generation
- **Maven** - Build tool

## 📦 Installation & Setup

### Prerequisites
- Node.js (v18 or higher)
- Java 23
- PostgreSQL
- Maven

### Backend Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd url-shortener-project
   ```

2. **Configure Database**
   - Create a PostgreSQL database
   - Update `url-shortener-sb/src/main/resources/application.properties` with your database credentials

3. **Run Spring Boot Application**
   ```bash
   cd url-shortener-sb
   mvn spring-boot:run
   ```
   The backend will start on `http://localhost:8080`

### Frontend Setup

1. **Install Dependencies**
   ```bash
   cd url-shortener-react
   npm install
   ```

2. **Configure API Endpoint**
   - Update the API base URL in `src/api/api.js` if needed

3. **Start Development Server**
   ```bash
   npm run dev
   ```
   The frontend will start on `http://localhost:5173`

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the frontend directory:

```env
VITE_API_BASE_URL=http://localhost:8080/api
```

### Database Configuration

Update `application.properties` in the backend:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/url_shortener
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
```

## 🚀 Deployment

### Frontend Deployment
```bash
cd url-shortener-react
npm run build
```
The built files will be in the `dist` directory, ready for deployment to any static hosting service.

### Backend Deployment
```bash
cd url-shortener-sb
mvn clean package
```
The JAR file will be created in the `target` directory and can be deployed to any Java hosting service.

## 📚 API Documentation

### Authentication Endpoints
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/profile` - Get user profile

### URL Management Endpoints
- `POST /api/urls` - Create new shortened URL
- `GET /api/urls` - Get user's URLs
- `GET /api/urls/{id}` - Get specific URL details
- `DELETE /api/urls/{id}` - Delete URL
- `GET /s/{shortUrl}` - Redirect to original URL

### Analytics Endpoints
- `GET /api/urls/{id}/clicks` - Get click analytics
- `POST /api/urls/{id}/click` - Record click event

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues or have questions:

1. Check the existing issues in the repository
2. Create a new issue with detailed information
3. Include steps to reproduce the problem
4. Provide your environment details (OS, Node.js version, Java version)

## 🎯 Roadmap

- [ ] Social media sharing integration
- [ ] Advanced analytics with heatmaps
- [ ] API rate limiting
- [ ] URL expiration dates
- [ ] Bulk URL import/export
- [ ] Mobile app development
- [ ] Multi-language support
- [ ] Advanced security features

---

**Built with ❤️ using React and Spring Boot**

