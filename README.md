# F1 Insights

Monorepo avec 3 modules :
- **api/** : FastAPI + FastF1 (Python)
- **web/** : Next.js + React
- **ios/** : SwiftUI iOS App

## Prérequis

- Docker
- Python 3.10+
- Node.js 18+
- Xcode 15+
- CocoaPods

## Installation locale

### 1. Backend (api)

```bash
cd api
pip install -r requirements.txt
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

### 2. Frontend (web)

```bash
cd web
npm ci
npm run dev
```

### 3. iOS

```bash
cd ios
pod install
open F1Insights.xcworkspace
```

## CI/CD

Chaque répertoire a son workflow GitHub Actions déclenché sur `push` et `pull_request`  
- Secrets à configurer :
  - `DOCKERHUB_USER`, `DOCKERHUB_TOKEN`
  - `VERCEL_TOKEN`, `VERCEL_ORG_ID`, `VERCEL_PROJECT_ID`
  - `APP_STORE_KEY_ID`, `APP_STORE_ISSUER_ID`, `APP_STORE_KEY`

## Gestion de projet

- Branches `feature/LINEAR-123-description`
- Issues et PR liées automatiquement dans Linear