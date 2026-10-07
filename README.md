# Decentralized Cloud Storage

Welcome to **Decentralized Cloud Storage**, an innovative project combining a powerful backend and an intuitive frontend to deliver a complete decentralized storage solution. This project merges **The Merkle Trees** (backend API) and **The Merkle Trees Client** (frontend interface) into a unified platform.

https://github.com/user-attachments/assets/af053288-b3f8-4be9-8c1a-b3eb2a94c82b

## 📋 Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## 🌟 Introduction

Decentralized Cloud Storage is a comprehensive solution designed to provide secure, resilient, and decentralized data management. By leveraging IPFS (InterPlanetary File System) for distributed storage and MongoDB for metadata management, this project eliminates the risks associated with centralized cloud providers. The system features a modern Nuxt.js frontend that enables users to create folders, upload files, write notes, and interact with a local Large Language Model (LLM).

## ✨ Features

### Backend (The Merkle Trees API)
- **Decentralized Storage**: Utilizes IPFS for distributed data storage across multiple nodes
- **Enhanced Security**: Data is encrypted and distributed, reducing the risk of data loss or unauthorized access
- **Scalability**: Easily scales to accommodate growing data volumes
- **Robust API**: RESTful API built with ASP.Net Core for reliable data operations
- **MongoDB Integration**: Efficient metadata and document management

### Frontend (The Merkle Trees Client)
- **Modern UI**: User-friendly interface built with Nuxt.js
- **Folder Management**: Create and organize folders hierarchically
- **File Upload**: Seamlessly upload files to decentralized storage
- **Note Taking**: Write and manage notes directly in the application
- **LLM Integration**: Interact with a local Large Language Model for enhanced productivity
- **Responsive Design**: Works across desktop and mobile devices

## 🏗️ Architecture

This project consists of two main components:

1. **Backend API** (ASP.Net Core): Handles storage operations, IPFS interactions, and data management
2. **Frontend Client** (Nuxt.js): Provides the user interface and connects to the backend API

```
┌─────────────────────┐
│   Nuxt.js Client    │
│  (User Interface)   │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  ASP.Net Core API   │
│   (Backend Logic)   │
└──────────┬──────────┘
           │
     ┌─────┴─────┐
     ▼           ▼
┌─────────┐ ┌─────────┐
│  IPFS   │ │ MongoDB │
│  Node   │ │         │
└─────────┘ └─────────┘
```

## 📦 Prerequisites

Before starting, ensure you have the following installed:

- **.NET 8 SDK** or later
- **Node.js** (v18 or later) and **npm**
- **IPFS** (InterPlanetary File System)
- **MongoDB** (local or remote instance)

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/pierreuntas/decentralized-cloud-storage

cd decentralized-cloud-storage
```

### 2. Configure and run IPFS

Initialize and start your local IPFS node:

```bash
ipfs init
ipfs daemon
```

The IPFS daemon should now be running on `http://localhost:5001`.

### 3. Configure MongoDB

Ensure MongoDB is running and accessible. Note your connection string for the configuration step.

### 4. Backend Setup

Navigate to the API directory and configure your settings:

```bash
cd TheMerkleTrees.Api
```

Edit `appsettings.json` with your MongoDB configuration:

```json
{
  "MongoDB": {
    "ConnectionString": "your_mongodb_connection_string",
    "DatabaseName": "your_database_name"
  }
}
```

Install dependencies and run the API:

```bash
dotnet restore
dotnet run
```

The API will be available at `http://localhost:5083`.

### 5. Frontend Setup

Open a new terminal and navigate to the client directory:

```bash
cd TheMerkleTreeClient
```

Install dependencies:

```bash
npm install
```

Configure the API endpoint in your Nuxt configuration file if needed, then start the development server:

```bash
npm run dev
```

The frontend will be available at `http://localhost:3000`.

## 💻 Usage

### Accessing the Application

1. **Frontend Interface**: Navigate to `http://localhost:3000` to access the user interface
2. **API Documentation**: Access the Swagger documentation at `http://localhost:5083/swagger/index.html`

### Key Features

- **Create Folders**: Organize your files with a hierarchical folder structure
- **Upload Files**: Drag and drop files for decentralized storage
- **Write Notes**: Create and edit text notes
- **LLM Interaction**: Use the integrated local LLM for queries and assistance
- **Search**: Find your files and notes quickly

## ⚙️ Configuration

### Backend Configuration

Edit `appsettings.json` in the API project:

```json
{
  "MongoDB": {
    "ConnectionString": "mongodb://localhost:27017",
    "DatabaseName": "decentralized_storage"
  },
  "IPFS": {
    "ApiUrl": "http://localhost:5001"
  }
}
```

### Frontend Configuration

Configure API endpoints in your Nuxt config file as needed for your environment.

## 🤝 Contributing

Contributions are welcome and appreciated! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please ensure your code follows the existing style and includes appropriate tests.

## 📄 License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. This license ensures that the software remains free and open-source while allowing the project owner to monetize the software. Any modifications to the code must also be released under the same license.

See the [LICENSE](LICENSE) file for complete details.

## 🙏 Acknowledgments

Thank you for using Decentralized Cloud Storage! We hope this solution meets your decentralized storage needs while providing a modern and intuitive user experience.

For questions, suggestions, or issues, please feel free to open an issue on GitHub.

---

**Made with ❤️ for a decentralized future**
