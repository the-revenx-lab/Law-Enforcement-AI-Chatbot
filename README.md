# Legal AI Assistant for Law Enforcement

A comprehensive AI-powered system designed to assist law enforcement officers in India with legal information, FIR processing, and legal guidance. This project combines natural language processing, legal database management, and document processing to streamline law enforcement operations.

![Legal AI Assistant Demo](docs/images/demo.gif)

## 🌟 Key Features

### 1. Interactive Legal Assistant
- 🤖 AI-powered chatbot for legal queries
- 📚 Comprehensive IPC section information
- 🏛️ Crime classification and legal status checks
- ⚖️ Legal procedure guidance
- 💬 Natural language understanding

### 2. FIR Management System
- 📝 Digital FIR creation and processing
- 🔄 Automated IPC section suggestions
- 📋 Standardized format compliance
- 🔍 Case tracking and management
- 📊 Status monitoring and updates

### 3. Legal Database
- 📖 Complete IPC sections database
- 🎯 Crime classification system
- 🔗 IPC-Crime mapping
- 📈 Case precedent references
- 🔒 Secure data management

### 4. User Interface
- 🎨 Modern, intuitive design
- ⚡ Real-time chat interface
- 🔐 Secure authentication
- 📱 Responsive layout
- 🌐 Cross-platform compatibility

## 🛠️ Technology Stack

### Backend
- **Core Framework**: Python 3.8+
- **AI/ML**: 
  - Rasa 3.6.2 (Conversational AI)
  - Natural Language Processing
- **Web Framework**: 
  - Flask
  - FastAPI
- **Database**: 
  - MySQL
  - SQLite (for certain components)
- **Real-time Communication**: 
  - Flask-SocketIO
  - WebSocket

### Frontend
- **Core**: HTML5, CSS3, JavaScript (ES6+)
- **Real-time**: Socket.IO Client
- **UI Framework**: Custom responsive design
- **Documentation**: Interactive API docs

## 📂 Project Structure

```
Legal-AI-Assistant-For-Law-Enforcement/
├── chat/                      # Chatbot MVP
│   └── mvp_prototype/        # Minimal viable chatbot
├── fir_management/           # FIR processing system
├── legal_database/           # Database management
├── web_interface/            # Web UI components
├── docs/                     # Documentation
├── tests/                    # Test suites
└── utils/                    # Utility scripts
```

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- MySQL 8.0+
- Node.js 14+ (for development)
- Git

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/Legal-AI-Assistant-For-Law-Enforcement.git
   cd Legal-AI-Assistant-For-Law-Enforcement
   ```

2. **Set Up Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Environment**:
   Create `.env` file with:
   ```env
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=your_password
   DB_NAME=legal_ai
   RASA_ACTION_ENDPOINT=http://localhost:5055/webhook
   ```

5. **Initialize Database**:
   ```bash
   mysql -u root -p < schema.sql
   python setup_database.py
   ```

6. **Train AI Model**:
   ```bash
   cd chat
   rasa train
   ```

### Running the System

Start each component in separate terminals:

1. **Rasa Action Server**:
   ```bash
   rasa run actions
   ```

2. **Rasa Server**:
   ```bash
   rasa run --enable-api --cors "*"
   ```

3. **Web Interface**:
   ```bash
   python app.py
   ```

Access the application at `http://localhost:5000`

## 📚 Documentation

- [User Guide](docs/user_guide.md)
- [API Documentation](docs/api.md)
- [Development Guide](docs/development.md)
- [Database Schema](docs/schema.md)
- [Deployment Guide](docs/deployment.md)

## 🧪 Testing

Run comprehensive test suite:
```bash
pytest tests/
```

For specific components:
```bash
pytest tests/test_chat.py
pytest tests/test_fir.py
pytest tests/test_database.py
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🛡️ Security

- All passwords must be changed in production
- Enable HTTPS in production
- Implement proper session management
- Use secure database configurations
- Regular security audits recommended

## 🌟 Acknowledgments

- Indian Penal Code (IPC) documentation
- Law enforcement agencies for requirements
- Open source community
- Contributors and maintainers

## ⚠️ Disclaimer

This system is designed as an assistant tool and should not be considered as legal advice. Always consult with legal professionals for official proceedings and decisions.

## 📞 Contact & Support

- Report bugs: Open an issue
- Feature requests: Use issue templates
- Questions: Discussions section
- Email: support@legalai-assistant.org

## 🔄 Updates & Maintenance

- Regular updates for IPC changes
- Quarterly feature releases
- Monthly security patches
- Continuous model improvements

---

Made with ❤️ for Indian Law Enforcement