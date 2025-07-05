# WHO Expertise-Locator System

A knowledge management system inspired by NASA's Expert Seeker, adapted to the World Health Organization context. It uses web data mining and information retrieval to build dynamic expertise profiles for WHO staff.

## Features
- PDF/HTML document ingestion
- Name disambiguation and fuzzy matching
- TF-IDF keyword extraction and profile building
- FastAPI backend with search endpoints
- Streamlit frontend for searching experts

- who-expert-locator/
├── README.md
├── requirements.txt
├── .env.example
├── .gitignore
├── docker-compose.yml
├── backend/
│   ├── main.py                 # FastAPI application
│   ├── models.py               # Pydantic models
│   ├── crud.py                 # DB access logic
│   ├── utils/
│   │   ├── text_mining.py      # TF-IDF & keyword extraction
│   │   ├── name_matching.py    # Fuzzy matching of names
│   │   └── doc_parser.py       # PDF and HTML text extraction
│   └── data/
│       ├── who_staff.csv       # Example name list
│       └── documents/          # Sample WHO documents
├── frontend/
│   ├── app.py                  # Streamlit app or Flask UI
│   └── static/                 # JS, CSS, images if Flask
├── database/
│   ├── init.sql                # SQL schema
│   └── postgres_data/          # Docker volume mount
└── tests/
    └── test_keyword_extraction.py
