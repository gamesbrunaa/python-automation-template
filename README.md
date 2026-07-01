# 🐍 Python automation template

Personal template for Python automation projects: scripts, workers, integrations and data processing.  
No web frameworks, just pure Python doing its job.

---

## 📂 Project structure

```
python-automation-template/
│
├── app/
│   ├── main.py                # Where everything starts
│   │
│   ├── core/                  # Settings, database connection, logger
│   │   └── __init__.py
│   │
│   ├── repositories/          # Database access layer (queries and models)
│   │   └── __init__.py
│   │
│   ├── services/              # Business logic
│   │   └── __init__.py
│   │
│   ├── adapters/              # External integrations (APIs, email, etc.)
│   │   └── __init__.py
│   │
│   └── utils/                 # Helper functions (dates, strings, formatting)
│       └── __init__.py
│
├── tests/                     # Unit tests (pytest)
│   └── __init__.py
│
├── .env.example               # Environment variables template
├── .gitignore                 # Files excluded from version control
├── pyproject.toml             # Dependencies and tool settings
├── docker-compose.yml         # Container setup
└── README.md
```

---

## 🏗️ Architecture

Each folder has a clear responsibility:

| Folder | What it does | Example |
|---|---|---|
| `core/` | Centralized settings and connections | Database config, environment variables, logger |
| `repositories/` | Talks to the database | Queries, SQLAlchemy models |
| `services/` | Business logic and data processing | Generate reports, classify tickets, transform data |
| `adapters/` | Connects to external services | API, email (SMTP), OpenAI |
| `utils/` | Generic reusable helpers | Date formatting, string manipulation |

> **Rule of thumb:** repositories fetch data, services process it, adapters send it out.

---

## 🚀 Getting Started

### 1. Clone and setup

```bash
git clone https://github.com/gamesbrunaa/python-automation-template.git
cd python-automation-template
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
pip install -e .[dev]
```

### 2. Configure environment

```bash
cp .env.example .env
# Edit .env with your credentials
```

### 3. Run

```bash
python -m app.main
```

---

## 🧪 Quality

| Tool | Command | What it does |
|---|---|---|
| **Ruff** | `ruff check .` | Linting and code style |
| **Ruff** | `ruff format .` | Auto-format code |
| **Pytest** | `pytest` | Run tests |
| **Docker** | `docker compose up -d` | Start containers |

---

## 📝 Commit Convention

This project follows [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add report generation service
fix: correct date parsing in utils
chore: update dependencies
docs: add architecture section to README
```

---

## 🛠️ Tech Stack

- **Python 3.10+**
- **MySQL** + **SQLAlchemy**
- **Docker** + **Docker Compose**
- **Pytest** for testing
- **Ruff** for linting & formatting

---

## 📄 License

MIT