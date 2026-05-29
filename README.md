# Parent-Teacher Hub

A simplified, multilingual messaging app that centralizes school announcements, report cards, and permission slips in one easy-to-use platform.

## 🎯 Features

- **📢 School Announcements**: Broadcast important updates to parents and teachers
- **📊 Report Cards**: Digital delivery and management of student report cards
- **📋 Permission Slips**: Digital permission slip requests and approvals
- **🌐 Multilingual Support**: Available in multiple languages (EN, ES, FR, etc.)
- **📱 Responsive Design**: Works seamlessly on desktop and mobile devices
- **🔐 Secure Authentication**: Role-based access control (Admin, Teacher, Parent)
- **🔔 Real-time Notifications**: Push notifications for important updates

## 📋 Table of Contents

- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## 🏗️ Project Structure

```
parent-teacher-hub/
├── frontend/                  # React/Next.js frontend application
│   ├── components/           # Reusable React components
│   ├── pages/               # Page components
│   ├── styles/              # CSS and styling
│   ├── hooks/               # Custom React hooks
│   ├── utils/               # Utility functions
│   ├── i18n/                # Internationalization config
│   └── package.json
├── backend/                   # Node.js/Express backend
│   ├── routes/              # API routes
│   ├── controllers/         # Route controllers
│   ├── models/              # Database models
│   ├── middleware/          # Express middleware
│   ├── utils/               # Utility functions
│   ├── config/              # Configuration files
│   └── package.json
├── database/                  # Database setup and migrations
│   ├── migrations/          # Database migrations
│   ├── seeds/               # Seed data
│   └── schema.sql
├── .github/
│   └── workflows/           # GitHub Actions workflows
├── docker-compose.yml       # Docker configuration
├── .env.example             # Environment variables template
└── README.md
```

## 🛠️ Tech Stack

### Frontend
- **Framework**: React 18 / Next.js
- **Language**: TypeScript / JavaScript
- **Styling**: Tailwind CSS
- **State Management**: Redux / Context API
- **API Client**: Axios
- **Internationalization**: i18next

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL / MongoDB
- **Authentication**: JWT
- **Testing**: Jest, Supertest
- **Documentation**: Swagger/OpenAPI

### DevOps
- **Containerization**: Docker & Docker Compose
- **CI/CD**: GitHub Actions
- **Version Control**: Git

## 📥 Installation

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn
- PostgreSQL/MongoDB
- Docker (optional)

### Local Setup

1. **Clone the repository**
```bash
git clone https://github.com/Roba76/parent-teacher-hub.git
cd parent-teacher-hub
```

2. **Install dependencies**

Frontend:
```bash
cd frontend
npm install
```

Backend:
```bash
cd backend
npm install
```

3. **Environment Configuration**
```bash
# Copy environment template
cp .env.example .env

# Edit with your configuration
nano .env
```

4. **Start the application**

Using Docker Compose (recommended):
```bash
docker-compose up -d
```

Or manually:

Frontend (Terminal 1):
```bash
cd frontend
npm run dev
```

Backend (Terminal 2):
```bash
cd backend
npm run dev
```

5. **Access the application**
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000
- API Documentation: http://localhost:5000/api-docs

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
# Frontend
REACT_APP_API_URL=http://localhost:5000
REACT_APP_DEFAULT_LANGUAGE=en

# Backend
NODE_ENV=development
PORT=5000
DATABASE_URL=postgresql://user:password@localhost:5432/parent-teacher-hub
JWT_SECRET=your_jwt_secret_here
JWT_EXPIRE=7d

# Email Configuration
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASS=your_app_password
```

### Database Setup

```bash
# Run migrations
npm run db:migrate

# Seed initial data
npm run db:seed
```

## 🚀 Usage

### For Teachers
1. Log in with your school credentials
2. Post announcements
3. Upload and manage report cards
4. Create and track permission slips

### For Parents
1. Create account and link to children
2. Receive announcements and updates
3. View report cards
4. Sign and submit permission slips
5. Receive notifications

### For Administrators
1. Manage user accounts and roles
2. Configure school settings
3. View system statistics
4. Manage content

## 🌐 Multilingual Support

The application supports multiple languages through i18next:

- **English** (en)
- **Spanish** (es)
- **French** (fr)
- **More languages coming soon!**

To add a new language:
1. Create a new translation file in `frontend/i18n/locales/{language}.json`
2. Add language to the language selector
3. Test the translations

## 🧪 Testing

### Run Tests

Frontend:
```bash
cd frontend
npm run test
```

Backend:
```bash
cd backend
npm run test
```

### Run Tests with Coverage

```bash
npm run test:coverage
```

## 🔐 Security

- JWT-based authentication
- Role-based access control (RBAC)
- Input validation and sanitization
- HTTPS/TLS encryption
- SQL injection prevention
- XSS protection
- CSRF tokens

## 🐛 Troubleshooting

### Port Already in Use
```bash
# Find process using port 3000
lsof -i :3000

# Kill the process
kill -9 <PID>
```

### Database Connection Issues
- Verify PostgreSQL/MongoDB is running
- Check DATABASE_URL in .env
- Ensure credentials are correct

### Frontend Won't Load
- Clear browser cache
- Clear node_modules and reinstall: `rm -rf node_modules && npm install`
- Check API endpoint in .env

## 📚 API Documentation

Full API documentation is available at: `http://localhost:5000/api-docs` (Swagger UI)

### Main Endpoints
- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration
- `GET /api/announcements` - Get all announcements
- `POST /api/announcements` - Create announcement
- `GET /api/report-cards` - Get report cards
- `GET /api/permission-slips` - Get permission slips

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines.

Quick steps:
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Support

For issues, questions, or suggestions:
1. Check existing [Issues](https://github.com/Roba76/parent-teacher-hub/issues)
2. Create a new issue with detailed information
3. Contact: robgithubug@gmail.com

## 🙏 Acknowledgments

- Built with ❤️ for educators and parents
- Special thanks to all contributors
- Inspired by the need for better school-home communication

---

**Last Updated**: 2026-05-29  
**Version**: 0.1.0 (Alpha)
