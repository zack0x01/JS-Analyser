# 🔒 JavaScript Security Analyzer

A powerful, modern web application for analyzing JavaScript files to detect sensitive data, security vulnerabilities, and potential attack vectors. Perfect for bug bounty hunters, security researchers, and developers.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-3.0+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## ✨ Features

### 🔍 Security Detection
- **API Keys**: Detects AWS, Google, GitHub, Stripe, PayPal, Slack, Firebase, JWT tokens, and more
- **Credentials**: Finds hardcoded passwords, usernames, database credentials
- **Email Addresses**: Extracts email addresses from JavaScript code
- **XSS Vulnerabilities**: Identifies potential Cross-Site Scripting vulnerabilities
  - innerHTML/outerHTML assignments
  - document.write() usage
  - eval() with user input
  - React dangerouslySetInnerHTML
  - jQuery injection points
- **XSS Functions**: Detects functions that may lead to XSS attacks

### 🌐 API & Endpoint Discovery
- Extracts API endpoints from fetch, axios, XMLHttpRequest, jQuery AJAX calls
- Identifies API paths, versioned endpoints, and base URLs
- Maps all network requests in the codebase

### 📋 Parameter Analysis
- Finds URL query parameters (`?key=`, `&email=`, etc.)
- Extracts function parameters
- Identifies sensitive parameters (keys, tokens, passwords)

### 📁 Path & Directory Discovery
- Extracts file paths and directories
- Identifies relative and absolute paths
- Finds file references

### 💬 Code Analysis
- Interesting comments (TODO, FIXME, SECURITY, HACK, BUG, WARNING)
- Suspicious comments containing sensitive keywords

### 🚀 Advanced Features
- **Multiple File Analysis**: Analyze single or multiple JavaScript files
- **File Upload**: Upload a text file with multiple URLs
- **Live Results**: View results as they're processed
- **Code Context**: See exact code locations with "Show Code" functionality
- **Filterable Results**: Filter findings by category
- **Modern UI**: Beautiful dark-themed interface
- **Reduced False Positives**: Smart filtering to minimize noise

## 🛠️ Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/zack0X01/js-analysis.git
cd js-analysis
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Run the application**
```bash
python app.py
```

4. **Access the web interface**
Open your browser and navigate to:
```
http://localhost:5000
```

## 📖 Usage

### Single File Analysis
1. Enter a JavaScript file URL in the input field
2. Click "Analyze"
3. View results organized by category

### Multiple Files Analysis
1. Switch to "Multiple URLs" tab
2. Paste multiple URLs (one per line)
3. Click "Analyze All"
4. Browse results using file cards

### File Upload
1. Switch to "Upload File" tab
2. Upload a `.txt` file containing URLs (one per line)
3. Click "Analyze File"

### Example URLs
```
https://example.com/app.js
http://localhost:8081/test.js
https://cdn.example.com/vendor.js
```

## 🎯 Use Cases

- **Bug Bounty Hunting**: Find exposed API keys and credentials
- **Security Audits**: Identify vulnerabilities in JavaScript codebases
- **Code Review**: Automated security scanning
- **Asset Discovery**: Map API endpoints and paths
- **Penetration Testing**: Identify potential attack vectors

## 🔧 Technical Details

### Architecture
- **Backend**: Flask (Python) - All analysis happens server-side
- **Frontend**: Vanilla JavaScript, HTML5, CSS3
- **Analysis Engine**: Regex-based pattern matching with false positive filtering

### Server-Side Processing
All analysis is performed on the server for:
- **Security**: Sensitive patterns never exposed to client
- **Performance**: Server can handle large files efficiently
- **Reliability**: Consistent results across different browsers

### Supported Patterns
- AWS Access Keys & Secrets
- Google API Keys
- GitHub Tokens
- Stripe Keys
- PayPal Tokens
- Slack Tokens
- Firebase Tokens
- JWT Tokens
- Generic API Keys & Secrets
- Hardcoded Credentials
- Email Addresses
- XSS Vulnerabilities
- API Endpoints
- URL Parameters
- File Paths

## 📊 Output Format

Results are displayed in an organized, filterable interface:
- **Statistics Dashboard**: Quick overview of findings
- **Categorized Results**: Organized by finding type
- **Code Context**: Exact line numbers and code snippets
- **Show Code**: Expandable code blocks with syntax highlighting
- **Export**: JSON format available via API

## 🛡️ Security Considerations

- All analysis performed server-side
- No JavaScript code is executed in the browser
- File size limits (10MB) to prevent DoS
- Input validation and sanitization
- CORS protection enabled

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**Zack0X01**

- 🎓 **Ethical Hacking Course**: [lureo.shop](https://lureo.shop)
- 📺 **YouTube**: [@zack0X01](https://youtube.com/@zack0X01)
- 🐦 **Twitter**: [@zack0X01](https://twitter.com/zack0X01)
- 📷 **Instagram**: [@zack0X01](https://instagram.com/zack0X01)

## 🙏 Acknowledgments

- Built for the security research and bug bounty community
- Inspired by the need for better JavaScript security analysis tools
- Thanks to all contributors and users

## ⚠️ Disclaimer

This tool is for **authorized security testing and educational purposes only**. Only use this tool on systems you own or have explicit permission to test. Unauthorized access to computer systems is illegal.

---

⭐ If you find this tool useful, please give it a star on GitHub!

