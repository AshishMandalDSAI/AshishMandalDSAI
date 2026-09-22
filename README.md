PROJECT NAME: AUREX AI

PROJECT TITLE:
AUREX AI — Enterprise AI Decision Intelligence Platform

ROLE:
You are acting as a Principal AI Architect, Senior Data Scientist, ML Engineer, MLOps Engineer, Backend Engineer, UI/UX Engineer, QA Engineer, and Production Software Architect.

I am building AUREX AI as a serious portfolio-grade and production-style Enterprise AI Decision Intelligence Platform.

IMPORTANT:
Do NOT treat this as a simple academic project.
Do NOT create a toy ML application.
Do NOT create a static dashboard.
Do NOT hardcode one specific dataset.
Do NOT assume a fixed business domain.

The platform must be designed as a reusable data-driven AI system where a user can upload their own CSV, Excel, or JSON datasets and AUREX AI dynamically profiles, analyzes, visualizes, models, explains, forecasts, simulates, optimizes, and generates business insights from the uploaded data.

The system must be modular, testable, maintainable, extensible, production-oriented, and suitable for future deployment.

==================================================
CORE PRODUCT VISION
==================================================

AUREX AI should transform:

RAW DATA
    ↓
DATA QUALITY
    ↓
DATA UNDERSTANDING
    ↓
EDA
    ↓
FEATURE ENGINEERING
    ↓
PREDICTIVE ANALYTICS
    ↓
RISK ANALYSIS
    ↓
FORECASTING
    ↓
EXPLAINABLE AI
    ↓
WHAT-IF SIMULATION
    ↓
OPTIMIZATION
    ↓
AI BUSINESS INSIGHTS
    ↓
DECISION SUPPORT

The system should support different datasets and business use cases without requiring source-code modification for every new dataset.

==================================================
PRIMARY USER WORKFLOW
==================================================

Design the product around this workflow:

1. User opens AUREX AI.
2. User uploads CSV / XLSX / JSON.
3. System validates file type and size.
4. System loads the dataset safely.
5. System automatically detects:
   - rows
   - columns
   - data types
   - numeric columns
   - categorical columns
   - date/time columns
   - identifier columns
   - possible target columns
   - missing values
   - duplicate rows
   - outliers
   - constant columns
   - high-cardinality columns
   - suspicious/leakage-like columns
6. System generates a Data Quality Score.
7. System creates an automated data profile.
8. System provides interactive EDA.
9. User selects a target variable or allows automatic target recommendation.
10. System identifies problem type:
    - classification
    - regression
    - time series
    - clustering
    - anomaly detection
11. System performs appropriate preprocessing.
12. System trains multiple candidate models.
13. System evaluates models using appropriate metrics.
14. System selects a champion model using a transparent selection strategy.
15. System provides model explainability.
16. System performs predictions.
17. System calculates risk where applicable.
18. System performs forecasting where applicable.
19. System provides scenario simulation.
20. System generates business recommendations.
21. System provides an AI Analyst layer.
22. System exposes reusable API endpoints.
23. System stores model metadata and experiment information.
24. System provides system health monitoring.

==================================================
DESIGN PRINCIPLES
==================================================

Follow these principles throughout the project:

- Modular architecture
- Separation of concerns
- Configuration-driven behavior
- No hardcoded dataset assumptions
- No hardcoded column names
- No hardcoded target variable
- No business-specific logic embedded into generic modules
- Type-safe data handling where practical
- Defensive programming
- Clear exception handling
- Logging
- Reproducibility
- Deterministic random seeds
- Input validation
- Output validation
- Unit tests
- Integration tests
- Regression tests
- Security-conscious file handling
- Resource-aware processing
- Graceful degradation
- Clear user-facing errors
- Explainable model decisions

==================================================
TECHNOLOGY DIRECTION
==================================================

Use a modern Python architecture.

Preferred stack:

Python 3.11+

Core:
- pandas
- numpy
- scipy

Machine Learning:
- scikit-learn
- XGBoost
- LightGBM if available
- optionally other mature libraries only when justified

Visualization:
- Plotly
- Streamlit

Explainability:
- SHAP

Forecasting:
- statsmodels
- Prophet only if compatibility is reliable
- ML-based forecasting where appropriate

Optimization:
- scipy.optimize
- OR-Tools if justified

Backend:
- FastAPI
- Pydantic

Database:
- PostgreSQL-ready architecture
- SQLite may be used for local development where appropriate

MLOps:
- MLflow

Testing:
- pytest

Code quality:
- Ruff
- Black

Containerization:
- Docker
- Docker Compose

CI/CD:
- GitHub Actions

==================================================
UI/UX DIRECTION
==================================================

AUREX AI must have a premium enterprise interface.

The design should be:

- professional
- modern
- futuristic
- minimal but information-rich
- visually consistent
- executive-friendly
- analyst-friendly
- responsive
- accessible
- fast

Use a sophisticated "3D-inspired" visual language.

IMPORTANT:
Do NOT create fake 3D charts merely for decoration.

Use:
- depth-inspired cards
- layered panels
- subtle gradients
- glass-like surfaces where appropriate
- elevated KPI cards
- smooth transitions where supported
- interactive Plotly charts
- modern navigation
- clean typography
- professional spacing
- consistent iconography

Charts must remain analytically correct and readable.

Avoid:
- excessive animations
- unnecessary neon effects
- unreadable dark backgrounds
- chart clutter
- fake metrics
- decorative graphs without analytical meaning.

==================================================
INITIAL DASHBOARD INFORMATION ARCHITECTURE
==================================================

Plan the following major modules:

1. Executive Command Center
2. Data Upload & Data Studio
3. Data Quality
4. Automated EDA
5. Customer / Entity Intelligence
6. Predictive Analytics
7. Risk Intelligence
8. Fraud / Anomaly Detection
9. Forecasting
10. Explainable AI
11. What-If Scenario Simulator
12. Optimization
13. AI Analyst
14. Model Lab
15. Model Registry
16. API / System Health
17. Settings

Do NOT implement all modules in this prompt.

This prompt is ONLY for architecture and foundation planning.

==================================================
REQUIRED FOLDER ARCHITECTURE
==================================================

Design a scalable structure similar to:

AUREX-AI/
│
├── app/
├── api/
├── src/
│   ├── ingestion/
│   ├── validation/
│   ├── profiling/
│   ├── preprocessing/
│   ├── feature_engineering/
│   ├── analytics/
│   ├── ml/
│   ├── forecasting/
│   ├── risk/
│   ├── anomaly/
│   ├── explainability/
│   ├── optimization/
│   ├── simulation/
│   ├── decision_engine/
│   ├── ai/
│   ├── registry/
│   └── utils/
│
├── tests/
├── models/
├── data/
├── reports/
├── docs/
├── configs/
├── scripts/
├── assets/
│
├── requirements.txt
├── pyproject.toml
├── Dockerfile
├── docker-compose.yml
├── .env.example
├── .gitignore
├── README.md
├── CLAUDE.md
└── PROJECT_SPEC.md

You may improve this architecture if you identify a better professional structure.

==================================================
IMPORTANT DATA ARCHITECTURE
==================================================

The application must distinguish between:

1. Raw uploaded data
2. Validated data
3. Cleaned/transformed data
4. Feature datasets
5. Training datasets
6. Prediction outputs
7. Model artifacts
8. Metadata
9. Experiment records
10. Reports

Never overwrite raw user data.

Design a session/project-based data lifecycle.

Consider:

project_id
dataset_id
dataset_version
model_id
experiment_id

The architecture should allow future multi-dataset projects.

==================================================
SECURITY & FILE SAFETY
==================================================

Plan protections for:

- unsupported file extensions
- oversized files
- malicious filenames
- malformed files
- corrupted Excel files
- invalid JSON
- empty datasets
- extremely wide datasets
- extremely large datasets
- duplicate uploads
- unsafe paths
- formula injection risks where applicable
- memory exhaustion
- unsafe serialized model loading

Do not blindly deserialize untrusted objects.

==================================================
ERROR HANDLING
==================================================

Every major module should eventually use structured exceptions.

Errors should contain:

- error code
- human-readable message
- technical details for logs
- suggested user action where appropriate

Never expose raw Python stack traces to normal users.

==================================================
TESTING STRATEGY
==================================================

Define a serious testing strategy.

Include:

Unit tests
Integration tests
Data validation tests
ML pipeline tests
API tests
UI smoke tests where practical
Regression tests
Edge-case tests

Examples:

- empty CSV
- one-row dataset
- missing values
- all-null column
- constant column
- duplicate records
- mixed data types
- date parsing failure
- binary target
- multiclass target
- high-cardinality categorical data
- regression target
- insufficient sample size
- missing target
- infinite values
- extreme outliers
- unsupported files

Every implementation phase must include tests.

==================================================
REPRODUCIBILITY
==================================================

Use deterministic seeds where possible.

Centralize:

RANDOM_STATE = 42

Do not scatter magic numbers throughout the project.

Use configuration files/settings.

==================================================
OBSERVABILITY
==================================================

Plan:

- structured logging
- application logs
- model training logs
- data processing logs
- error logs
- performance timing
- model metrics
- dataset metadata

The architecture should allow future monitoring.

==================================================
DOCUMENTATION
==================================================

Create a documentation plan for:

- system architecture
- data lifecycle
- ML lifecycle
- API
- model selection
- explainability
- security
- testing
- deployment
- user guide
- developer guide

==================================================
IMPORTANT CLAUDE WORKFLOW
==================================================

DO NOT implement the whole project now.

First:

1. Inspect the current workspace.
2. If a project folder already exists, preserve useful existing work.
3. Do not overwrite unrelated files.
4. Analyze the environment.
5. Produce the architecture.
6. Create only the foundational files required for this phase.
7. Add initial configuration.
8. Add project-level documentation.
9. Add initial test infrastructure.
10. Run all relevant tests.
11. Fix any failures.
12. Verify imports.
13. Verify that the application can start at a basic level if applicable.

At the end provide:

A. Files created
B. Files modified
C. Architecture summary
D. Dependencies added
E. Tests executed
F. Test results
G. Known limitations
H. Recommended next milestone

IMPORTANT:
Do not claim a feature works unless you actually tested it.

Do not fabricate test results.

Do not skip validation.

Do not move to the next major feature automatically.

STOP after completing this milestone and wait for my next instruction.
