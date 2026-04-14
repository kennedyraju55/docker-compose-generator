# 🐳 docker-compose-generator

Generate production-ready docker-compose files from plain English — no servers involved

[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org)
[![Ollama](https://img.shields.io/badge/Ollama-Local%20LLM-green)](https://ollama.com)
[![Gemma 3](https://img.shields.io/badge/Gemma%203-Language%20Model-orange)](https://ollama.com/library/gemma2)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow)](./LICENSE)
[![Privacy First](https://img.shields.io/badge/Privacy-First-darkgreen)](#why-local)

## 🎯 What it does

- Create complete docker-compose.yml files from natural language descriptions
- Auto-configure services, networking, volumes, environment variables, and health checks
- Supports popular stacks: LAMP, MERN, Django+PostgreSQL, Microservices, etc.
- 100% local processing — docker configs stay on your machine

## 🛠️ Tech Stack

- Streamlit (Web UI)
- FastAPI (Backend API)
- Ollama (Local LLM inference)
- Gemma 3 (Language model)
- Python 3.8+

## ⚡ Quick Start

1. **Clone the repository**
   \\\ash
   git clone https://github.com/kennedyraju55/docker-compose-generator.git
   cd docker-compose-generator
   \\\

2. **Install dependencies**
   \\\ash
   pip install -r requirements.txt
   \\\

3. **Download and start Ollama**
   - Download from [ollama.com](https://ollama.com)
   - Start Ollama service:
   \\\ash
   ollama serve
   \\\
   - In another terminal, pull Gemma 3:
   \\\ash
   ollama pull gemma2
   \\\

4. **Run the application**
   \\\ash
   streamlit run app.py
   \\\

Access the app at: http://localhost:8501

## 🏗️ Architecture

\\\
User describes services → Streamlit UI → FastAPI processes request → Ollama generates compose file using Gemma 3 → Returns complete YAML → Edit and deploy locally
\\\

All processing happens locally on your machine. No data is sent to external services.

## 🔒 Why Local?

Docker compose files define your entire service architecture, database credentials, secret management, and internal networking. Keeping this generation local protects your infrastructure design from external exposure.

## 📦 Environment Variables

Create a \.env\ file in the project root:

\\\nv
OLLAMA_BASE_URL=http://localhost:11434
MODEL_NAME=gemma2
LOG_LEVEL=INFO
\\\

## 🤝 Contributing

We love contributions! Here's how to help:

1. Fork the repository
2. Create a feature branch: \git checkout -b feature/your-feature\
3. Make your changes and commit: \git commit -am 'Add feature'\
4. Push to the branch: \git push origin feature/your-feature\
5. Submit a Pull Request

Please ensure:
- Code follows PEP 8 style guidelines
- Changes include appropriate comments
- Updates to documentation are included

## 📄 License

This project is licensed under the MIT License — see [LICENSE](./LICENSE) for details.

---

**Part of 114+ privacy-first AI tools by [Nrk Raju](https://github.com/kennedyraju55)**