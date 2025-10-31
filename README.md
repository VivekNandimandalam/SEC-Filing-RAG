# SEC-Filing-RAG

Automated extraction of oil & gas metrics from SEC 10-Q and 10-K filings using RAG (Retrieval-Augmented Generation) with Excel export and PostgreSQL database storage.

## Features

- 🔍 Automatic SEC filing extraction from EDGAR database
- 🤖 AI-powered metric extraction using RAG pipeline
- 📊 Excel workbook generation with multiple sheets
- 💾 PostgreSQL database storage (optional)
- 🏢 Support for multiple oil & gas companies

## Installation

```bash
# Clone the repository
git clone https://github.com/VivekNandimandalam/SEC-Filing-RAG.git
cd SEC-Filing-RAG

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install requests beautifulsoup4 langchain-community langchain-openai
pip install langchain-text-splitters faiss-cpu sentence-transformers openai
pip install pandas openpyxl psycopg2-binary lxml html5lib
```

## Configuration

Set your OpenAI API key:

```bash
# Windows PowerShell
$env:OPENAI_API_KEY="your-key-here"

# Linux/Mac
export OPENAI_API_KEY="your-key-here"
```

For Azure OpenAI, set:
- `AZURE_OPENAI_API_KEY`
- `AZURE_OPENAI_ENDPOINT`
- `AZURE_OPENAI_DEPLOYMENT`

Optional: PostgreSQL environment variables:
- `PGHOST` or `POSTGRES_HOST`
- `PGPORT` or `POSTGRES_PORT`
- `PGDATABASE` or `POSTGRES_DB`
- `PGUSER` or `POSTGRES_USER`
- `PGPASSWORD` or `POSTGRES_PASSWORD`

## Usage

```bash
python secfiling_extraction.py
```

The script will:
1. Prompt for company selection
2. Fetch available filings from SEC EDGAR
3. Allow you to select 10-Q and/or 10-K filings
4. Extract metrics using AI
5. Generate Excel files in the `output` folder
6. Save JSON files in the current directory
7. Optionally store data in PostgreSQL database

## Output

- **Excel files**: Saved in the `output/` folder
- **JSON files**: Saved in the current working directory
- **Database**: Optional PostgreSQL storage

## Supported Companies

- FANG - Diamondback Energy
- PR - Permian Resources
- DVN - Devon Energy
- OVV - Ovintiv
- CTRA - Coterra Energy
- EOG - EOG Resources
- SM - SM Energy
- VTLE - Vital Energy
- MTDR - Matador Resources
- OXY - Occidental Petroleum
- XOM - Exxon Mobil

## License

This project is Secfiling_Extraction_Vivek.

