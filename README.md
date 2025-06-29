# 📄 DocManager

<p align="center">
  <a href="#features">Features</a> •
  <a href="#demo">Demo</a> •
  <a href="#technologies">Technologies</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#installation">Installation</a> •
  <a href="#usage">Usage</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#license">License</a>
</p>

<p align="center">
  <a href="https://github.com/ishan22399/Next-Gen-Document-Management-System/stargazers"><img src="https://img.shields.io/github/stars/ishan22399/Next-Gen-Document-Management-System?style=social" alt="GitHub stars"></a>
  <a href="https://github.com/ishan22399/Next-Gen-Document-Management-System/network/members"><img src="https://img.shields.io/github/forks/ishan22399/Next-Gen-Document-Management-System?style=social" alt="GitHub forks"></a>
  <a href="https://github.com/ishan22399/Next-Gen-Document-Management-System/issues"><img src="https://img.shields.io/github/issues/ishan22399/Next-Gen-Document-Management-System" alt="GitHub issues"></a>
  <a href="https://github.com/ishan22399/Next-Gen-Document-Management-System/blob/main/LICENSE"><img src="https://img.shields.io/github/license/ishan22399/Next-Gen-Document-Management-System" alt="License"></a>
</p>

---

## 📋 Introduction

**DocManager** is a next-generation, cloud-based document management system designed for secure storage, rapid search, and tamper-proof verification of documents. Built with Flask, AWS, and blockchain-inspired technology, it ensures your data is always protected and verifiable.

- **Motivation:** Provide a secure, transparent, and efficient way to manage and verify documents in the cloud.
- **Why:** Eliminate document tampering, streamline search, and provide full auditability for compliance and trust.
- **What Makes It Stand Out:** Combines AES encryption, Merkle tree verification, and blockchain logging in a user-friendly, responsive interface.

---

## 📑 Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Demo](#demo)
- [Technologies](#technologies)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [Credits](#credits)
- [License](#license)

---

## ✨ Features

- 🔐 **Robust Security:** AES encryption and secure authentication.
- 📤 **Seamless Document Operations:** Upload, view, edit, download, and delete.
- 🔍 **Advanced Search:** Fast keyword search with Aho-Corasick algorithm.
- ⚡ **Efficient Filtering:** Bloom Filters for quick query rejection.
- 🌳 **Data Integrity:** Merkle Root verification for tamper-proof assurance.
- ⛓️ **Transparent Auditing:** Immutable blockchain-inspired logs.
- 📱 **Responsive Design:** Works on desktop and mobile.
- 📊 **Analytics Dashboard:** Visualize storage and document metrics.

---

## 🎬 Demo

See DocManager in action! Watch the full workflow: Upload ➡️ Encrypt ➡️ Search ➡️ Verify ➡️ Log.

<p align="center">
  <a href="https://drive.google.com/file/d/1giTkAmWYzmX4qj2xtrcRhWkZP8Y9jKSr/view?usp=drive_link" target="_blank">
    <img src="https://img.icons8.com/color/480/google-drive--v2.png" alt="Watch Demo on Google Drive" width="180">
  </a>
</p>

[Watch the full demo on Google Drive](https://drive.google.com/file/d/1giTkAmWYzmX4qj2xtrcRhWkZP8Y9jKSr/view?usp=drive_link)

---

## 🛠️ Technologies

**Backend:**
- ![Python](https://img.shields.io/badge/Python-3776AB?style-for-the-badge&logo=python&logoColor=white) Flask
- ![AWS](https://img.shields.io/badge/AWS-232F3E?style-for-the-badge&logo=amazon-aws&logoColor=white) S3, DynamoDB
- ![Blockchain](https://img.shields.io/badge/Blockchain-121D33?style-for-the-badge&logo=ethereum&logoColor=white) Solidity, Ganache

**Frontend:**
- ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style-for-the-badge&logo=html5&logoColor=white) HTML5
- ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style-for-the-badge&logo=css3&logoColor=white) CSS3
- ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style-for-the-badge&logo=javascript&logoColor=black) JavaScript
- ![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style-for-the-badge&logo=bootstrap&logoColor=white) Bootstrap

**Development & Testing:**
- ![Git](https://img.shields.io/badge/Git-F05032?style-for-the-badge&logo=git&logoColor=white) Git
- ![Selenium](https://img.shields.io/badge/Selenium-43B02A?style-for-the-badge&logo=selenium&logoColor=white) Selenium
- ![PyTest](https://img.shields.io/badge/PyTest-0A9EDC?style-for-the-badge&logo=pytest&logoColor=white) PyTest

---

## 🏗️ Architecture

```
User Interface (Frontend) --> Flask API --> AWS Services (S3, DynamoDB) --> Blockchain Verification
```

- **Frontend:** Responsive, Bootstrap-powered interface.
- **Backend:** Flask routes for document operations, encryption, and search.
- **Storage:** AWS S3 for files, DynamoDB for metadata.
- **Verification:** Solidity smart contracts and Ganache for tamper-proof logging.

---

## 🚀 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ishan22399/Next-Gen-Document-Management-System.git
   cd Next-Gen-Document-Management-System
   ```

2. **Set up a virtual environment:**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r Backend/requirements.txt
   ```

4. **Configure AWS and Ganache:**
   - Update `Backend/.env` with your AWS and blockchain credentials.
   - Launch Ganache and deploy smart contracts using scripts in `Backend/blockchain`.

5. **Initialize the database:**
   ```bash
   python Backend/init_db.py
   ```

6. **Set up the blockchain environment:**
   ```bash
   python Backend/setup_blockchain.py
   ```

7. **Run the application:**
   ```bash
   python Backend/app.py
   ```

8. **Access the app:**
   ```
   http://localhost:5000
   ```

---

## 📖 Usage

- **Login/Register:** Create an account or log in.
- **Upload Documents:** Securely upload and encrypt files.
- **Search:** Use keywords to find documents instantly.
- **Verify:** Check document integrity and blockchain log.
- **Dashboard:** View analytics and document history.

---

## 🤝 Contributing

Contributions are welcome! Please open issues or submit pull requests.

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a pull request

---

## 👥 Credits

- **Ishan22399** – [GitHub](https://github.com/ishan22399)
- Special thanks to all contributors and the open-source community.

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

> _Every day is a learning day. Keep your README up to date and make your project stand out!_
