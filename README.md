# 🐳 Docker Compose Generator

Generate multi-container Docker Compose files instantly with AI intelligence.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Ollama](https://img.shields.io/badge/Ollama-Compatible-green.svg)](https://ollama.com)
[![Gemma 3](https://img.shields.io/badge/Gemma-3-orange.svg)](https://ollama.com)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Privacy First](https://img.shields.io/badge/Privacy-First-red.svg)](#why-local)

## What It Does

- **Auto-generates docker-compose.yml files** from your service requirements
- **Multi-container orchestration** with networking, volumes, and environment variables
- **Production-ready configs** with health checks and resource limits
- **Local intelligence** powered by Gemma 3 for context-aware generation

## Tech Stack

- **Python 3.8+** — Generation engine
- **Gemma 3** (via Ollama) — Container configuration intelligence
- **PyYAML** — YAML generation and validation
- **Docker** — Container runtime (optional for testing)

## Quick Start

`ash
# Clone the repository
git clone https://github.com/kennedyraju55/docker-compose-generator.git
cd docker-compose-generator

# Install dependencies
pip install -r requirements.txt

# Pull Gemma 3 model locally
ollama pull gemma3:4b

# Generate a Docker Compose file
python generator.py --services postgres redis frontend backend
`

## Architecture

`
service list + requirements
    ↓
[Gemma 3 LLM Analysis] ← offline, local
    ↓
networking strategy + config rules
    ↓
docker-compose.yml (ready to deploy)
`

## Why Local?

- **Security**: Your infrastructure configs never leave your machine
- **Privacy**: No cloud exposure of your service architecture
- **Control**: Full customization without external constraints
- **Offline**: Works anywhere, anytime — no internet required

## Contributing

Contributions welcome! Please fork, create a feature branch, and submit a pull request.

## License

MIT License — see [LICENSE](LICENSE) for details.

---

*Part of 114+ privacy-first AI tools by Nrk Raju*