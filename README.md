# CodeScout

<p align="center">
  <img src="https://img.shields.io/badge/CodeScout-Semantic%20Code%20Search-blue" alt="CodeScout">
</p>

<p align="center">
  <strong>Revolutionize Your Code Search with AI-Powered Semantic Understanding</strong>
</p>

<p align="center">
  Search your codebase using natural language queries, get intelligent code explanations, and analyze your repositories with cutting-edge AI technology.
</p>

<p align="center">
  <a href="#features">🔍 Features</a> •
  <a href="#architecture">🏗️ Architecture</a> •
  <a href="#installation">🚀 Installation</a> •
  <a href="#usage">💻 Usage</a> •
  <a href="#development">👨‍💻 Development</a>
</p>

---

## Features

### 🔍 **Semantic Code Search**
- Search your codebase using natural language queries
- AI-powered understanding of code semantics and context
- Support for multiple programming languages (Python, JavaScript, TypeScript, Java, C++, etc.)

### 🌐 **Multi-Interface Access**
- **Web Interface**: Modern, responsive Next.js frontend
- **CLI Tool**: Command-line interface for terminal users
- **REST API**: Flask backend for programmatic access

### 🧠 **AI-Powered Code Analysis**
- Code explanation and documentation generation
- Intelligent code highlighting and syntax analysis
- Repository structure analysis and insights

### ⚡ **Advanced Features**
- File difference analysis and generation
- Code clustering for duplicate detection
- Repository documentation generation
- Standards compliance checking

## Architecture

CodeScout is built as a full-stack application with three main components:

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │   CLI Tool      │
│   (Next.js)     │◄──►│   (Flask)       │    │   (Python)      │
│                 │    │                 │    │                 │
│ • Web Interface │    │ • REST API      │    │ • Terminal UI   │
│ • Modern UI     │    │ • AI Services   │    │ • Local Search  │
│ • Responsive    │    │ • Embeddings    │    │ • Fast Queries  │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### Components Overview

1. **Frontend** (`/frontend/`): Next.js React application with modern UI components
2. **Backend** (`/flask_backend/`): Flask API server with AI-powered services
3. **CLI Tool** (`/cli tool/`): Standalone Python CLI for semantic code search

## Installation

### Prerequisites

- **Python 3.8+** (for CLI tool and backend)
- **Node.js 16+** (for frontend)
- **npm or yarn** (for frontend dependencies)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/SatvikG7/CodeScout.git
   cd CodeScout
   ```

### CLI Tool Installation

The CLI tool provides semantic code search functionality directly from your terminal.

```bash
cd "cli tool"
pip install -r requirements.txt
python setup.py install
```

**Usage:**
```bash
# Navigate to your code repository
cd /path/to/your/repo

# Search using natural language
sem "authentication logic"
sem "database connection setup"
sem "error handling for API calls"
```

### Backend Setup

The Flask backend provides REST API services for code analysis and search.

```bash
cd flask_backend

# Install dependencies
pip install -r requirements.txt

# Start the server
python app.py
```

**Dependencies:**
- Flask & Flask-CORS
- LangChain with Ollama embeddings
- Chroma vector database
- Additional utilities for file processing

### Frontend Setup

The Next.js frontend provides a modern web interface for CodeScout.

```bash
cd frontend

# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build
npm start
```

**Access the application:**
- Development: http://localhost:3000
- Production: Configure your deployment environment

## Usage

### Web Interface

1. **Start the backend server** (Flask API)
2. **Launch the frontend** (Next.js application)
3. **Navigate to** http://localhost:3000
4. **Upload or connect** your repository
5. **Search using natural language** queries
6. **Explore results** with syntax highlighting and explanations

### CLI Interface

```bash
# Basic search
sem "function that handles user authentication"

# Search with file extension filter
sem "database queries" -x py

# Generate embeddings for a repository
sem --embed -p /path/to/repo

# Show cluster analysis
sem --cluster -p /path/to/repo

# Get help
sem --help
```

### API Endpoints

The Flask backend exposes several REST endpoints:

- `POST /api/search` - Semantic code search
- `POST /api/explain` - Code explanation
- `POST /api/highlight` - Syntax highlighting
- `POST /api/diff` - File difference analysis
- `POST /api/generate-docs` - Documentation generation

## Development

### Development Environment Setup

1. **Backend Development**
   ```bash
   cd flask_backend
   pip install -r requirements.txt  # Create based on imports
   python app.py  # Runs on http://localhost:5000
   ```

2. **Frontend Development**
   ```bash
   cd frontend
   npm install
   npm run dev  # Runs on http://localhost:3000
   ```

3. **CLI Development**
   ```bash
   cd "cli tool"
   pip install -e .  # Editable installation
   ```

### Technology Stack

**Frontend:**
- Next.js 14 with TypeScript
- Tailwind CSS for styling
- Radix UI components
- Monaco Editor for code display
- React Syntax Highlighter

**Backend:**
- Flask with CORS support
- LangChain with Ollama embeddings
- Chroma vector database
- Python utilities for file processing

**CLI Tool:**
- Sentence Transformers for embeddings
- Tree-sitter for code parsing
- Prompt Toolkit for interactive UI
- PyTorch for ML operations

### Project Structure

```
CodeScout/
├── frontend/                 # Next.js React application
│   ├── src/app/             # App router pages
│   ├── src/components/      # Reusable UI components
│   └── package.json         # Dependencies and scripts
├── flask_backend/           # Flask API server
│   ├── app.py              # Main application entry
│   ├── services/           # AI and utility services
│   └── utils/              # Helper functions
├── cli tool/               # Python CLI application
│   ├── src/semantic_code_search/  # Main package
│   ├── setup.py            # Package configuration
│   └── requirements.txt    # Python dependencies
└── README.md              # This file
```

## Contributing

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit your changes** (`git commit -m 'Add amazing feature'`)
4. **Push to the branch** (`git push origin feature/amazing-feature`)
5. **Open a Pull Request**

### Development Guidelines

- Follow the existing code style and conventions
- Add tests for new features when applicable
- Update documentation for API changes
- Ensure all components work together

## License

This project is licensed under the GNU Affero General Public License v3.0 (AGPL-3.0). See the CLI tool's setup.py for specific license details.

## Acknowledgments

- Built on top of semantic code search technology
- Uses state-of-the-art transformer models for code understanding
- Inspired by the need for better code discovery and documentation tools

---

<p align="center">
  <strong>Made with ❤️ by the CodeScout team</strong>
</p>
