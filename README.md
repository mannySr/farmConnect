# 🐄 FarmConnect

> Connecting livestock owners with feed and medicine suppliers through digital innovation

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Code Quality](https://sonar.server.examly.io/api/project_badges/measure?project=iamneo-production-2_d042574a-e859-4c58-9d86-aeeb23372f94-70ad352c-85b1-4151-823e-0d76251b1329&metric=alert_status)](https://sonar.server.examly.io/dashboard?id=iamneo-production-2_d042574a-e859-4c58-9d86-aeeb23372f94-70ad352c-85b1-4151-823e-0d76251b1329&codeScope=overall)

## 📖 About The Project

FarmConnect is a comprehensive platform designed to bridge the gap between livestock owners and suppliers of feed and medicine. The application facilitates seamless connections, enabling owners to manage their livestock and request supplies while allowing suppliers to list their products and fulfill requests efficiently.

### ✨ Key Features

- **🔐 User Authentication & Authorization**
  - Separate registration and login for Owners and Suppliers
  - JWT-based secure authentication
  - Role-based access control

- **👨‍🌾 Owner Dashboard**
  - Manage livestock inventory
  - Create and track supply requests
  - View available feed and medicine
  - Provide feedback on suppliers
  - Track request history

- **🏪 Supplier Dashboard**
  - Add and manage feed listings
  - Add and manage medicine inventory
  - View and respond to supply requests
  - Receive customer feedback
  - Track order fulfillment

- **🐮 Livestock Management**
  - Add and manage livestock information
  - Track livestock health and details
  - View livestock inventory

- **📦 Feed & Medicine Management**
  - Browse available feed and medicine products
  - Detailed product information
  - Real-time inventory updates
  - Image gallery for products

- **💬 Request System**
  - Create supply requests
  - Track request status
  - Direct communication between owners and suppliers
  - Request management and fulfillment

- **📝 Feedback System**
  - Rate and review suppliers
  - View feedback history
  - Quality assurance through customer reviews

## 🛠️ Tech Stack

### Frontend
- **React.js** - UI library for building interactive interfaces
- **Redux / Redux Toolkit** - State management
- **React Router** - Client-side routing
- **Axios** - HTTP client for API calls
- **CSS3** - Custom styling

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - Authentication and authorization
- **bcrypt.js** - Password hashing
- **Multer** - File upload handling

### Development Tools
- **Git** - Version control
- **ESLint** - Code linting
- **Babel** - JavaScript compiler
- **Jest** - Testing framework
- **Nodemon** - Development server auto-restart

## 🏗️ Project Structure

```
farmConnect/
├── .gitignore
├── LICENSE
├── README.md
├── nodeapp/                    # Backend application
│   ├── authUtils.js           # Authentication utilities
│   ├── controllers/           # Business logic controllers
│   │   ├── feedbackController.js
│   │   ├── feedController.js
│   │   ├── liveStockController.js
│   │   ├── medicineController.js
│   │   ├── requestController.js
│   │   └── userController.js
│   ├── index.js              # Server entry point
│   ├── middleware/           # Custom middleware
│   │   └── upload.js
│   ├── models/               # Database models
│   │   ├── feedbackModel.js
│   │   ├── feedModel.js
│   │   ├── liveStockModel.js
│   │   ├── medicineModel.js
│   │   ├── requestModel.js
│   │   └── userModel.js
│   └── routers/              # API routes
│       ├── feedbackRouter.js
│       ├── feedRouter.js
│       ├── liveStockRouter.js
│       ├── medicineRouter.js
│       ├── requestRouter.js
│       └── userRouter.js
├── nodejest/                 # Backend testing
│   └── run.sh
├── react/                    # Frontend build scripts
│   └── react.sh
└── reactapp/                 # Frontend application
    ├── .babelrc
    ├── eslintrc.js
    ├── file-mock.js
    ├── style-mock.js
    ├── public/               # Static assets
    │   ├── alert.png
    │   ├── farmconnect.png
    │   ├── favicon.ico
    │   ├── index.html
    │   ├── logo192.png
    │   ├── logo512.png
    │   ├── manifest.json
    │   ├── no_records_found.png
    │   └── robots.txt
    └── src/
        ├── apiConfig.js      # API configuration
        ├── App.css
        ├── App.js           # Main application component
        ├── index.css
        ├── index.js         # Application entry point
        ├── store.js         # Redux store configuration
        ├── userSlice.js     # User state management
        ├── Components/       # Shared components
        │   ├── ErrorPage.css
        │   ├── ErrorPage.jsx
        │   ├── HomePage.css
        │   ├── HomePage.jsx
        │   ├── Login.css
        │   ├── Login.jsx
        │   ├── PrivateRoute.jsx
        │   ├── Signup.css
        │   └── Signup.jsx
        ├── OwnerComponents/  # Owner-specific components
        │   ├── LivestockForm.css
        │   ├── LivestockForm.jsx
        │   ├── MyRequest.css
        │   ├── MyRequest.jsx
        │   ├── OwnerFeedback.css
        │   ├── OwnerFeedback.jsx
        │   ├── OwnerNavbar.css
        │   ├── OwnerNavbar.jsx
        │   ├── OwnerViewFeed.css
        │   ├── OwnerViewFeed.jsx
        │   ├── OwnerViewMedicine.css
        │   ├── OwnerViewMedicine.jsx
        │   ├── ViewLivestock.css
        │   └── ViewLivestock.jsx
        └── SupplierComponents/ # Supplier-specific components
            ├── AddFeed.css
            ├── AddFeed.jsx
            ├── AddMedicine.css
            ├── AddMedicine.jsx
            ├── SupplierFeedback.css
            ├── SupplierFeedback.jsx
            ├── SupplierNavbar.css
            ├── SupplierNavbar.jsx
            ├── ViewFeed.css
            ├── ViewFeed.jsx
            ├── ViewMedicine.css
            ├── ViewMedicine.jsx
            ├── ViewRequest.css
            └── ViewRequest.jsx
```

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v14.x or higher)
- **npm** or **yarn**
- **MongoDB** (local installation or MongoDB Atlas account)
- **Git**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Ritts17/farmConnect.git
   cd farmConnect
   ```

2. **Backend Setup**
   ```bash
   cd nodeapp
   npm install
   ```

3. **Create a `.env` file in the nodeapp directory**
   ```env
   PORT=8080
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   JWT_EXPIRE=30d
   NODE_ENV=development
   ```

4. **Start the backend server**
   ```bash
   npm start
   # OR for development with nodemon
   npm run dev
   ```
   The backend server will run on `http://localhost:8080`

5. **Frontend Setup** (Open a new terminal)
   ```bash
   cd reactapp
   npm install
   ```

6. **Configure API endpoint in `src/apiConfig.js`**
   ```javascript
   export const API_URL = 'http://localhost:8080/api';
   ```

7. **Start the frontend development server**
   ```bash
   npm start
   ```
   The application will open at `http://localhost:3000`

## 📱 Usage

### For Livestock Owners
1. Register as an Owner with required details
2. Add and manage your livestock inventory
3. Browse available feed and medicine from suppliers
4. Create supply requests for needed items
5. Track request status and fulfillment
6. Provide feedback on suppliers

### For Suppliers
1. Register as a Supplier
2. Add feed and medicine products with details
3. View and manage product inventory
4. Receive and respond to supply requests
5. Track fulfilled orders
6. View customer feedback

## 🧪 Testing

```bash
# Run backend tests
cd nodejest
./run.sh

# Run frontend tests
cd react
./react.sh
```

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to the branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**

### Development Guidelines
- Follow the existing code style
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting PR

## 🐛 Bug Reports & Feature Requests

Found a bug or have a feature request? Please open an issue [here](https://github.com/Ritts17/farmConnect/issues) with:
- Clear title and description
- Steps to reproduce (for bugs)
- Expected vs actual behavior
- Screenshots if applicable

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Ritts17** - *Initial work* - [Ritts17](https://github.com/Ritts17)

See also the list of [contributors](https://github.com/Ritts17/farmConnect/contributors) who participated in this project.

## 🙏 Acknowledgments

- Inspiration from the need to streamline livestock supply chain management
- Thanks to all contributors and supporters
- Built with ❤️ for the farming community

## 📞 Contact & Support

- **GitHub Issues**: [Report bugs or request features](https://github.com/Ritts17/farmConnect/issues)
- **Email**: your.email@example.com

## 🗺️ Roadmap

- [x] User authentication system
- [x] Livestock management
- [x] Feed and medicine listings
- [x] Request system
- [x] Feedback system
- [ ] Payment gateway integration
- [ ] Mobile application (React Native)
- [ ] Real-time notifications
- [ ] Advanced analytics dashboard
- [ ] Delivery tracking system
- [ ] Multi-language support

## SonarQube

d042574a-e859-4c58-9d86-aeeb23372f94-70ad352c-85b1-4151-823e-0d76251b1329<br/>
https://sonar.server.examly.io/dashboard?id=iamneo-production-2_d042574a-e859-4c58-9d86-aeeb23372f94-70ad352c-85b1-4151-823e-0d76251b1329&codeScope=overall

## 📊 Project Status

![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Ritts17/farmConnect)
![GitHub last commit](https://img.shields.io/github/last-commit/Ritts17/farmConnect)
![GitHub issues](https://img.shields.io/github/issues/Ritts17/farmConnect)
![GitHub pull requests](https://img.shields.io/github/issues-pr/Ritts17/farmConnect)

---

<div align="center">
  Made with ❤️ by the FarmConnect Team Ritts17 , mannySr
  <br/>
  <strong>Empowering Livestock Owners, Connecting Suppliers</strong>
</div>
