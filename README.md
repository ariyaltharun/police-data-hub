# Police Data Hub 🚔

A comprehensive, secure platform designed for managing and protecting sensitive police data through advanced privacy-preserving technologies. This full-stack application combines modern web technologies, AI-powered data anonymization, and blockchain transparency to ensure the confidentiality, integrity, and accountability of police data handling.

> **🏆 Built for the Karnataka State Police Datathon**
> This project was developed as part of the Karnataka State Police Datathon, focusing on innovative solutions for secure police data management and privacy protection in law enforcement operations.

[![Demo Video](https://img.shields.io/badge/Demo-Watch%20Video-red)](https://github.com/satwikkamath/DataGuardians/assets/107809929/7bcaeb53-62dd-4f11-a434-b1443d93ef1e)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20App-blue)](https://data-guardians.vercel.app/)

## 🌐 Live Application
**[🚀 Access the live application here: data-guardians.vercel.app](https://data-guardians.vercel.app/)**

## 🌟 Key Features

### 🔐 Multi-Layer Security Architecture
- **Firebase Authentication**: Secure user authentication with role-based access control
- **Role-Based Permissions**: Differentiated access levels for ADMIN and USER roles
- **Secure File Upload**: Protected CSV file upload with validation
- **MongoDB Integration**: Secure database storage with proper data isolation

### 🔗 Blockchain Transparency
- **Immutable Audit Trail**: Every data access and anonymization request is recorded on the blockchain
- **Smart Contract Integration**: Ethereum-based smart contracts for transparent tracking
- **Activity Logging**: Comprehensive logging of user actions, timestamps, and file access patterns
- **Payment Integration**: Blockchain-based payment system for data access requests

### 🔒 Advanced Data Anonymization
- **Microsoft Presidio Integration**: State-of-the-art PII detection and anonymization
- **Selective Column Anonymization**: Granular control over which data fields to anonymize
- **Custom Anonymization Rules**: Enhanced analyzer with specialized detection patterns
- **Real-time Processing**: On-demand anonymization without permanent data modification

### 🔍 Full-Text Search
- **MongoDB Atlas Search**: Advanced search capabilities across all data fields
- **Anonymized Results**: Search results automatically anonymized based on user permissions
- **Flexible Querying**: Support for complex search queries with result limiting

### 📊 Data Management
- **CSV File Processing**: Automated parsing and storage of structured police data
- **Collection Management**: Organized data storage with file-based collections
- **Download Capabilities**: Export anonymized data in CSV format
- **Data Visualization**: User-friendly interface for data exploration

## 🏗️ System Architecture

### Frontend (React + Vite)
- **Modern UI Framework**: React 18 with Vite for fast development and building
- **Responsive Design**: Tailwind CSS for mobile-first, responsive design
- **Component Architecture**: Modular React components for maintainability
- **Routing**: React Router for single-page application navigation
- **State Management**: Context API for authentication and global state

### Backend (FastAPI + Python)
- **High-Performance API**: FastAPI for async, high-performance REST API
- **Database Integration**: MongoDB for flexible document storage
- **Privacy Engine**: Custom anonymization pipeline with Presidio
- **CORS Support**: Configured for secure cross-origin requests
- **Error Handling**: Comprehensive error handling and logging

### Blockchain (Ethereum/Solidity)
- **Smart Contracts**: Solidity contracts for activity tracking
- **Transaction Logging**: Immutable record of all data access events
- **Payment Integration**: ETH-based payment system for premium features
- **Transparency**: Public audit trail for accountability

### Database (MongoDB)
- **Document Storage**: Flexible schema for diverse data types
- **Full-Text Search**: Atlas Search for advanced querying capabilities
- **Data Isolation**: Separate collections for different data sources
- **Scalability**: Cloud-ready architecture for production deployment

## 🚀 Quick Start

### Prerequisites
- Node.js (v16 or higher)
- Python (v3.8 or higher)
- MongoDB Atlas account
- Firebase project setup
- Ethereum wallet (for blockchain features)

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/police-data-hub.git
   cd police-data-hub
   ```

2. **Frontend Setup**
   ```bash
   npm install
   npm run dev
   ```

3. **Backend Setup**
   ```bash
   cd backend
   pip install -r requirements.txt
   ```

4. **Environment Configuration**
   Create `.env` files with the following variables:

   **Backend (.env)**
   ```env
   MONGODB_URL=your_mongodb_connection_string
   DATABASE_NAME=your_database_name
   FIREBASE_PROJECT_ID=your_firebase_project_id
   ```

   **Frontend (.env)**
   ```env
   VITE_FIREBASE_API_KEY=your_firebase_api_key
   VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
   VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
   ```

5. **Start the Services**
   ```bash
   # Frontend (Terminal 1)
   npm run dev

   # Backend (Terminal 2)
   cd backend
   uvicorn app:app --reload --port 5000

   # Optional: Blockchain Development (Terminal 3)
   npx hardhat node
   ```

## 📱 Application Components

### Core Pages
- **Home**: Landing page with feature overview and navigation
- **Sign In/Sign Up**: Firebase-powered authentication system
- **Upload Data**: Secure CSV file upload interface (Admin only)
- **Access Data**: Data viewing and anonymization interface
- **Your Profile**: User account management and activity history
- **Privacy Regulations**: Compliance information and guidelines

### Key Features
- **File Management**: Upload, view, and manage police data files
- **Data Anonymization**: Select columns for privacy protection
- **Search & Filter**: Full-text search with anonymized results
- **Audit Trail**: Blockchain-recorded activity logs
- **Role Management**: Admin vs User access control

## 🔧 API Endpoints

### Authentication & File Management
- `GET /` - Health check and API status
- `POST /upload` - Upload CSV files (Admin only)
- `GET /fileNames` - List available data files
- `GET /columnNames` - Get column names for a specific file

### Data Processing
- `POST /anonymize-data` - Anonymize selected data columns
- `POST /search` - Full-text search with anonymization
- `GET /collections` - List all data collections
- `GET /download/<collection>` - Download anonymized data

### Blockchain Integration
- `anonymize_columns()` - Smart contract function for activity logging
- `getMemos()` - Retrieve blockchain activity logs

## 🔒 Security Features

### Data Protection
- **End-to-End Encryption**: Secure data transmission
- **Role-Based Access**: Granular permission system
- **Data Anonymization**: PII protection using Microsoft Presidio
- **Audit Logging**: Comprehensive activity tracking

### Privacy Compliance
- **GDPR Compliance**: Privacy-by-design architecture
- **Data Minimization**: Only necessary data processing
- **User Consent**: Explicit consent for data processing
- **Right to Deletion**: Support for data removal requests

### Blockchain Transparency
- **Immutable Records**: Tamper-proof activity logs
- **Public Auditability**: Transparent access to activity records
- **Decentralized Trust**: Blockchain-based verification

## 🛠️ Technology Stack

### Frontend
- **React 18**: Modern React with hooks and concurrent features
- **Vite**: Fast build tool and development server
- **Tailwind CSS**: Utility-first CSS framework
- **Heroicons**: Beautiful SVG icons
- **React Router**: Client-side routing
- **Firebase SDK**: Authentication and real-time features

### Backend
- **FastAPI**: Modern, fast Python web framework
- **Presidio**: Microsoft's PII anonymization library
- **PyMongo**: MongoDB driver for Python
- **Uvicorn**: ASGI server for FastAPI
- **CORS Middleware**: Cross-origin request handling

### Blockchain
- **Solidity**: Smart contract programming language
- **Hardhat**: Ethereum development environment
- **Ethers.js**: Ethereum library for JavaScript
- **MetaMask Integration**: Web3 wallet connectivity

### Database & Infrastructure
- **MongoDB Atlas**: Cloud database service
- **Firebase Auth**: Authentication service
- **Vercel**: Frontend deployment platform
- **IPFS**: Distributed file storage (optional)

## 📊 Data Flow

1. **User Authentication**: Firebase handles secure login/registration
2. **File Upload**: Admins upload CSV files to MongoDB collections
3. **Data Access**: Users request access to specific data files
4. **Anonymization**: Presidio processes data to remove PII
5. **Blockchain Logging**: Smart contracts record access events
6. **Result Delivery**: Anonymized data returned to user interface

## 🚀 Deployment

### Frontend (Vercel)
```bash
npm run build
vercel --prod
```

### Backend (Cloud Services)
- Deploy to platforms like Railway, Heroku, or AWS
- Configure environment variables
- Set up MongoDB Atlas connection
- Configure CORS for production domains

### Smart Contracts
```bash
npx hardhat compile
npx hardhat deploy --network mainnet
```

## 🧪 Testing

### Frontend Testing
```bash
npm run test
npm run lint
```

### Backend Testing
```bash
cd backend
python -m pytest
```

### Smart Contract Testing
```bash
npx hardhat test
```

## 📈 Performance Optimization

- **Lazy Loading**: Component-level code splitting
- **Caching**: Intelligent data caching strategies
- **Database Indexing**: Optimized MongoDB queries
- **CDN Integration**: Static asset delivery
- **Bundle Optimization**: Minimized JavaScript bundles

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-feature`
3. Commit changes: `git commit -am 'Add new feature'`
4. Push to branch: `git push origin feature/new-feature`
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support, email support@police-data-hub.com or create an issue in the GitHub repository.

## 🙏 Acknowledgments

- Microsoft Presidio team for the anonymization library
- Firebase team for authentication services
- MongoDB team for the database platform
- Ethereum community for blockchain infrastructure
- Open source contributors and maintainers

---

**⚠️ Important Security Notice**: This application handles sensitive police data. Ensure proper security measures, regular security audits, and compliance with local data protection regulations before deploying to production.
