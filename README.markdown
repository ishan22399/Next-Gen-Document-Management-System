# 📄 DocManager

<p align="center">
  <img src="https://user-images.githubusercontent.com/69488528/236614389-9b7b6e5f-eda3-4e22-a73c-4c5c4faff6d7.png" alt="DocManager Logo" width="200">
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#demo">Demo</a> •
  <a href="#technologies">Technologies</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#installation">Installation</a> •
  <a href="#usage">Usage</a>
</p>

## 📋 Introduction

DocManager is a state-of-the-art, cloud-based document management system designed to securely store, search, and verify documents with unmatched efficiency. Built with Flask and AWS, it leverages advanced security features like AES encryption and blockchain-inspired verification to ensure data integrity and transparency.

Featuring a sleek, responsive interface optimized for both desktop and mobile, DocManager makes document management intuitive and accessible from anywhere.

## ✨ Features <a name="features"></a>

- 🔐 **Robust Security**: AES encryption and secure user authentication for airtight protection.
- 📤 **Seamless Document Operations**: Upload, view, edit, download, and delete documents effortlessly.
- 🔍 **Advanced Search**: Aho-Corasick algorithm for rapid keyword searches.
- ⚡ **Efficient Filtering**: Bloom Filters for quick rejection of irrelevant queries.
- 🌳 **Data Integrity**: Merkle Root verification for tamper-proof assurance.
- ⛓️ **Transparent Auditing**: Immutable logs inspired by blockchain for full traceability.
- 📱 **Responsive Design**: Optimized for desktop and mobile users.
- 📊 **Analytics Dashboard**: Visualize storage usage and document metrics.

## 🎬 Demo <a name="demo"></a>

Explore DocManager in action! Our demo showcases the complete workflow: Upload ➡️ Encrypt ➡️ Search ➡️ Verify ➡️ Log.

[Watch the full demo on Google Drive](https://drive.google.com/your-demo-link)

## 🛠️ Technologies <a name="technologies"></a>

### Backend
- ![Python](https://img.shields.io/badge/Python-3776AB?style-for-the-badge&logo=python&logoColor=white) **Flask**: Lightweight web framework.
- ![AWS](https://img.shields.io/badge/AWS-232F3E?style-for-the-badge&logo=amazon-aws&logoColor=white) **AWS Services**:
  - **S3**: Scalable document storage.
  - **DynamoDB**: High-performance NoSQL database.
- ![Blockchain](https://img.shields.io/badge/Blockchain-121D33?style-for-the-badge&logo=ethereum&logoColor=white) **Solidity & Ganache**: Blockchain-based verification and logging.
- ![Python](https://img.shields.io/badge/Python-3776AB?style-for-the-badge&logo=python&logoColor=white) **Python**: Encryption, search, Bloom Filters, and Merkle Trees.

### Frontend
- ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style-for-the-badge&logo=html5&logoColor=white) **HTML5**: Structured content.
- ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style-for-the-badge&logo=css3&logoColor=white) **CSS3**: Modern styling.
- ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style-for-the-badge&logo=javascript&logoColor=black) **JavaScript**: Dynamic functionality.
- ![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style-for-the-badge&logo=bootstrap&logoColor=white) **Bootstrap**: Responsive layouts.

### Development & Testing
- ![Git](https://img.shields.io/badge/Git-F05032?style-for-the-badge&logo=git&logoColor=white) **Git**: Version control.
- ![Selenium](https://img.shields.io/badge/Selenium-43B02A?style-for-the-badge&logo=selenium&logoColor=white) **Selenium**: Automated testing.
- ![PyTest](https://img.shields.io/badge/PyTest-0A9EDC?style-for-the-badge&logo=pytest&logoColor=white) **PyTest**: Unit and integration testing.

## 📐 Architecture <a name="architecture"></a>

DocManager employs a modular architecture for scalability and reliability:

```
User Interface (Frontend) --> Flask API --> AWS Services (S3, DynamoDB) --> Blockchain Verification
```

- **Frontend**: Delivers a responsive, Bootstrap-powered interface for user interactions.
- **Backend**: Flask routes handle document operations, encryption, and search.
- **Storage**: AWS S3 for secure file storage, DynamoDB for metadata management.
- **Verification**: Solidity smart contracts and Ganache for tamper-proof logging.

## 🚀 Installation <a name="installation"></a>

1. Clone the repository:
   ```bash
   git clone https://github.com/ishan22399/Next-Gen-Document-Management-System.git
   cd Next-Gen-Document-Management-System
   ```

2. Set up a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r Backend/requirements.txt
   ```

4. Configure AWS and Ganache:
   - Set up AWS credentials for S3 and DynamoDB access (update `Backend/.env` with your credentials).
   - Launch Ganache and deploy Solidity smart contracts using scripts in `Backend/blockchain`.

5. Initialize the database:
   ```bash
   python Backend/init_db.py
   ```

6. Set up the blockchain environment:
   ```bash
   python Backend/setup_blockchain.py
   ```

7. Run the application:
   ```bash
   python Backend/app.py
   ```

8. Access the application at:
   ```
   http://localhost:5000
   ```

## 📂 Project Structure <a name="usage"></a>

```
Next-Gen-Document-Management-System/
├── Backend/
│   ├── blockchain/            # Solidity contracts and blockchain setup
│   ├── reports/              # Test and coverage reports
│   ├── routes/               # Flask route handlers
│   ├── test_venv/            # Virtual environment for testing
│   ├── tests/                # Unit and integration tests
│   ├── utils/                # Utility scripts for encryption, search, etc.
│   ├── .coverage             # Code coverage data
│   ├── .env                  # Environment variables
│   ├── .env.example          # Sample environment variables
│   ├── .gitignore            # Git ignore rules
│   ├── app.py                # Main Flask application
│   ├── credentials.json      # AWS credentials (ensure this is not committed)
│   ├── generate_test_requirements.txt  # Script to generate test requirements
│   ├── init_db.py            # Database initialization script
│   ├── pytest.ini            # PyTest configuration
│   ├── requirements.txt      # Python dependencies
│   ├── run_tests.py          # Script to execute tests
│   ├── schema.md             # Database schema documentation
│   ├── setup_blockchain.py   # Blockchain environment setup
│   └── setup_test_env.py     # Test environment setup
├── Frontend/
│   ├── static/               # CSS, JS, and images
│   └── templates/            # HTML templates
├── demo/
│   ├── auto_demo.py          # Automated demo script
│   ├── demo_document.txt     # Sample document for demo
│   ├── full_end_to_end_demo.py  # Full end-to-end demo script
│   ├── ganache_explorer.py   # Ganache blockchain explorer script
│   ├── run_full_demo.py      # Script to run the full demo
│   └── tamper_document.txt   # Sample tampered document for demo
└── README.md                 # Project documentation
```