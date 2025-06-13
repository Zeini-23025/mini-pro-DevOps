# 🐍 Mini Flask App with Docker & CI/CD

Ce projet est une application Flask très simple, contenant deux routes (`/` et `/index`). Il est conteneurisé avec Docker et intègre un workflow GitHub Actions pour automatiser la construction et la publication d'une image Docker sur Docker Hub.

## 🚀 Fonctionnalités

- Application Flask minimaliste
- Dockerfile pour conteneuriser l'application
- Fichier `requirements.txt` pour les dépendances
- Workflow GitHub Actions (`docker-publish.yml`) pour CI/CD

## 📁 Structure du projet

```
.
├── app.py
├── Dockerfile
├── requirements.txt
├── .github/
│   └── workflows/
│       └── docker-publish.yml
└── README.md
```

## 🧪 Exemple de routes

- `GET /` → `{"message": "Hello, World!"}`
- `GET /index` → `welcom to index`

## ⚙️ Installation locale

```bash
git clone https://github.com/Zeini-23025/mini-pro-DevOps.git
cd mini-pro-DevOps
python -m venv venv
source venv/bin/activate  # ou .\venv\Scripts\activate sous Windows
pip install -r requirements.txt
python app.py
```

## 🐳 Utilisation avec Docker

### 🔨 Construire l’image Docker

```bash
docker build -t zeini/mini-pro:latest .
```

### ▶️ Lancer le conteneur

```bash
docker run -p 5000:5000 zeini/mini-pro:latest
```

### ☁️ Pousser manuellement l’image sur Docker Hub

```bash
docker login
docker push zeini/mini-pro:latest
```

## 🔄 CI/CD avec GitHub Actions

Ce workflow permet de construire et publier automatiquement l’image Docker à chaque push sur `main`.
