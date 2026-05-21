# STIN Project - Folder Structure

## Overview
This document outlines the recommended folder structure for the Synthetic Transaction Intelligence Network (STIN) project, organized to support collaboration between four team members working on different components.

## Root Directory Structure

```
stin/
├── .github/                          # GitHub workflows and templates
│   ├── workflows/                    # CI/CD pipelines
│   │   ├── ml-models-ci.yml         # ML model testing
│   │   ├── infrastructure-ci.yml    # Infrastructure tests
│   │   ├── frontend-ci.yml          # Frontend tests
│   │   └── security-scan.yml        # Security scanning
│   ├── ISSUE_TEMPLATE/              # Issue templates
│   └── PULL_REQUEST_TEMPLATE.md     # PR template
│
├── docs/                             # Project documentation
│   ├── architecture/                 # Architecture diagrams and specs
│   ├── api/                         # API documentation
│   ├── user-guides/                 # End-user documentation
│   ├── development/                 # Developer guides
│   └── compliance/                  # Regulatory documentation
│
├── synthgen-engine/                  # Task 1: AI Model Development
│   ├── models/                      # Model implementations
│   │   ├── diffusion/              # Diffusion model
│   │   ├── timegan/                # Temporal GAN
│   │   ├── graphvae/               # Graph VAE
│   │   ├── causal/                 # Causal structure learner
│   │   └── fraud-generator/        # Adversarial fraud generator
│   ├── privacy/                     # Privacy validation
│   ├── fidelity/                    # Quality assessment
│   ├── training/                    # Training scripts
│   ├── evaluation/                  # Evaluation scripts
│   ├── notebooks/                   # Jupyter notebooks for experiments
│   ├── tests/                       # Unit and integration tests
│   ├── configs/                     # Model configurations
│   └── requirements.txt             # Python dependencies
│
├── data-infrastructure/              # Task 2: Data Infrastructure & MLOps
│   ├── pipelines/                   # Data pipelines
│   │   ├── ingestion/              # Data ingestion
│   │   ├── preprocessing/          # Data preprocessing
│   │   └── validation/             # Data validation
│   ├── mlops/                       # MLOps components
│   │   ├── orchestration/          # Workflow orchestration
│   │   ├── monitoring/             # Model monitoring
│   │   ├── versioning/             # Model versioning
│   │   └── deployment/             # Deployment scripts
│   ├── api/                         # API services
│   │   ├── generation/             # Data generation API
│   │   ├── management/             # Data management API
│   │   └── gateway/                # API gateway
│   ├── storage/                     # Storage layer
│   │   ├── data-lake/              # Data lake setup
│   │   ├── feature-store/          # Feature store
│   │   └── model-registry/         # Model registry
│   ├── infrastructure/              # Infrastructure as Code
│   │   ├── terraform/              # Terraform configs
│   │   ├── kubernetes/             # K8s manifests
│   │   └── docker/                 # Dockerfiles
│   ├── tests/                       # Tests
│   └── requirements.txt             # Python dependencies
│
├── fraudshield-platform/             # Task 3: Application Development
│   ├── frontend/                    # Frontend applications
│   │   ├── training-studio/        # Model training UI
│   │   │   ├── src/
│   │   │   ├── public/
│   │   │   ├── tests/
│   │   │   └── package.json
│   │   ├── fraud-dashboard/        # Monitoring dashboard
│   │   │   ├── src/
│   │   │   ├── public/
│   │   │   ├── tests/
│   │   │   └── package.json
│   │   ├── analytics-portal/       # Analytics interface
│   │   │   ├── src/
│   │   │   ├── public/
│   │   │   ├── tests/
│   │   │   └── package.json
│   │   └── shared/                 # Shared components
│   │       ├── components/
│   │       ├── utils/
│   │       └── styles/
│   ├── backend/                     # Backend services
│   │   ├── training-service/       # Training orchestration
│   │   ├── scoring-service/        # Fraud scoring
│   │   ├── decision-engine/        # Decision workflow
│   │   ├── analytics-service/      # Analytics computation
│   │   ├── reporting-service/      # Report generation
│   │   └── shared/                 # Shared utilities
│   ├── ml-components/               # ML components
│   │   ├── automl/                 # AutoML pipeline
│   │   ├── explainability/         # SHAP/LIME
│   │   ├── drift-detection/        # Model drift
│   │   └── ensemble/               # Ensemble models
│   ├── database/                    # Database schemas
│   │   ├── migrations/             # DB migrations
│   │   └── seeds/                  # Seed data
│   ├── tests/                       # Tests
│   │   ├── unit/
│   │   ├── integration/
│   │   ├── e2e/
│   │   └── load/
│   └── requirements.txt             # Python dependencies
│
├── governance-ethics/                # Task 4: Governance & Compliance
│   ├── frameworks/                  # Governance frameworks
│   │   ├── ai-ethics/              # AI ethics guidelines
│   │   ├── privacy/                # Privacy policies
│   │   └── compliance/             # Compliance frameworks
│   ├── documentation/               # Compliance documentation
│   │   ├── regulatory/             # Regulatory reports
│   │   ├── audits/                 # Audit reports
│   │   └── certifications/         # Certification docs
│   ├── collaboration/               # Industry collaboration
│   │   ├── partnerships/           # Partnership agreements
│   │   ├── standards/              # Industry standards
│   │   └── working-groups/         # Working group materials
│   ├── risk-management/             # Risk management
│   │   ├── assessments/            # Risk assessments
│   │   ├── mitigation/             # Mitigation strategies
│   │   └── monitoring/             # Risk monitoring
│   └── templates/                   # Document templates
│
├── collabhub-network/                # Cross-institution collaboration
│   ├── blockchain/                  # Blockchain components
│   │   ├── smart-contracts/        # Smart contracts
│   │   ├── ledger/                 # Ledger implementation
│   │   └── consensus/              # Consensus mechanism
│   ├── sharing-protocol/            # Data sharing protocol
│   ├── quality-certification/       # Quality certification
│   └── tests/                       # Tests
│
├── shared/                           # Shared resources across all tasks
│   ├── utils/                       # Common utilities
│   ├── configs/                     # Shared configurations
│   ├── schemas/                     # Data schemas
│   └── constants/                   # Constants
│
├── scripts/                          # Utility scripts
│   ├── setup/                       # Setup scripts
│   ├── deployment/                  # Deployment scripts
│   ├── testing/                     # Testing scripts
│   └── maintenance/                 # Maintenance scripts
│
├── tests/                            # Integration tests across components
│   ├── integration/                 # Cross-component integration
│   ├── system/                      # System-level tests
│   └── performance/                 # Performance tests
│
├── .gitignore                        # Git ignore file
├── .env.example                      # Environment variables template
├── docker-compose.yml                # Docker compose for local dev
├── Makefile                          # Common commands
├── README.md                         # Project README
├── CONTRIBUTING.md                   # Contribution guidelines
├── LICENSE                           # License file
└── CHANGELOG.md                      # Change log
```

## Team Member Responsibilities

### Team Member 1: ML/AI Specialist
**Primary Directory:** `synthgen-engine/`
- Owns all AI model development
- Responsible for model training, evaluation, and optimization
- Maintains privacy and fidelity validation frameworks

### Team Member 2: Data Engineer/MLOps Specialist
**Primary Directory:** `data-infrastructure/`
- Owns data pipelines and infrastructure
- Responsible for MLOps platform and API services
- Maintains deployment and monitoring systems

### Team Member 3: Full-Stack Developer/ML Engineer
**Primary Directory:** `fraudshield-platform/`
- Owns frontend and backend applications
- Responsible for user interfaces and API services
- Maintains ML components for production use

### Team Member 4: Strategy/Compliance Lead
**Primary Directory:** `governance-ethics/`
- Owns governance frameworks and compliance documentation
- Responsible for regulatory reporting and industry collaboration
- Maintains risk management and ethical guidelines

## Shared Responsibilities

### All Team Members
- **`docs/`**: Contribute documentation relevant to their area
- **`shared/`**: Use and contribute to shared utilities
- **`tests/`**: Write integration tests for cross-component features
- **`.github/`**: Maintain CI/CD workflows for their components

## Branch Strategy

```
main                    # Production-ready code
├── develop            # Integration branch
│   ├── feature/ml-*   # ML model features (Team Member 1)
│   ├── feature/infra-* # Infrastructure features (Team Member 2)
│   ├── feature/app-*  # Application features (Team Member 3)
│   └── feature/gov-*  # Governance features (Team Member 4)
├── release/*          # Release branches
└── hotfix/*           # Hotfix branches
```

## File Naming Conventions

### Python Files
- Snake case: `model_training.py`, `data_pipeline.py`
- Test files: `test_model_training.py`

### JavaScript/TypeScript Files
- Camel case for files: `modelTraining.ts`, `dataPipeline.ts`
- Pascal case for components: `ModelTrainingView.tsx`
- Test files: `modelTraining.test.ts`

### Configuration Files
- Kebab case: `model-config.yaml`, `deployment-config.json`

### Documentation Files
- Pascal case with hyphens: `API-Documentation.md`, `User-Guide.md`

## Key Configuration Files

### Root Level
- **`.env.example`**: Template for environment variables
- **`docker-compose.yml`**: Local development environment
- **`Makefile`**: Common commands (setup, test, deploy)

### Component Level
- **`requirements.txt`** or **`package.json`**: Dependencies
- **`Dockerfile`**: Container definition
- **`config.yaml`**: Component configuration
- **`README.md`**: Component-specific documentation

## Data Storage Locations

### Development
- Local data: `data/` (gitignored)
- Model checkpoints: `models/checkpoints/` (gitignored)
- Logs: `logs/` (gitignored)

### Production
- Cloud storage (S3/GCS) for data lakes
- Model registry for trained models
- Centralized logging system

## Notes

1. **Large Files**: Use Git LFS for model checkpoints and large datasets
2. **Secrets**: Never commit secrets; use environment variables
3. **Documentation**: Keep README files updated in each major directory
4. **Testing**: Maintain test coverage above 80% for all components
5. **Code Review**: All PRs require at least one approval from another team member