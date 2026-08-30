# PromptToStack

Describe any app in plain English and get a complete full-stack system blueprint — UI pages, API endpoints, database schema, auth roles, and business logic — validated and ready to build.

## What It Does

PromptToStack takes a natural language description like _"Build a CRM with login, contacts, dashboard, role-based access, and premium plan with payments"_ and compiles it into a structured, validated system architecture.

The output is a strict Pydantic-validated JSON contract covering:
- **UI Layer** — Pages, components, and layout mappings
- **API Layer** — RESTful endpoints, HTTP methods, and validation rules
- **Database Layer** — Tables, columns, and foreign key relations
- **Auth System** — Roles and granular permission mappings
- **Business Logic** — Domain rules and constraints

## Features

- **Multi-stage compilation pipeline** — Intent parsing, schema generation, cross-layer validation
- **Self-repair engine** — Detects inconsistencies (e.g., UI references an analytics page but no API endpoint exists) and patches them automatically
- **Input sanity checking** — Rejects vague prompts, surfaces calculated assumptions for ambiguous specs
- **Deterministic output** — Pydantic model contracts ensure type-safe, reproducible blueprints
- **Performance benchmarks** — Built-in evaluation matrix with edge case profiling
- **Interactive workspace** — Simulated build execution with directory structure preview

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Streamlit |
| Validation | Pydantic |
| Language | Python |
| Container | Dev Containers (Python 3.11) |

## Getting Started

```bash
# Clone the repo
git clone https://github.com/jasonjose007/PromptToStack.git
cd PromptToStack

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```

The app opens at `http://localhost:8501`.

## How It Works

```
User Prompt → Sanity Check → Schema Generation → Cross-Layer Validation → Self-Repair (if needed) → Validated JSON Blueprint
```

1. **Input** — Describe your app in the sidebar text area
2. **Compile** — Click "Compile System Architecture"
3. **Review** — Inspect the generated JSON contract in the Pipeline tab
4. **Execute** — Trigger a simulated workspace build in the Execution tab
5. **Benchmark** — View compilation metrics and edge case results

## Project Structure

```
PromptToStack/
├── app.py              # Main application — compiler pipeline + Streamlit UI
├── requirements.txt    # Python dependencies
└── .devcontainer/      # Dev container configuration for Codespaces
```
