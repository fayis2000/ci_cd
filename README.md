
---

```markdown
# CI/CD Pipeline for Node.js App using GitHub Actions

This project demonstrates a complete CI/CD pipeline using GitHub Actions to build, test, lint, Dockerize, and deploy a Node.js app to a self-hosted Linux server.

## 🚀 Features

- Express.js-based simple Node.js server
- Linting with ESLint
- Unit testing with Jest
- Dockerized application
- GitHub Actions CI/CD pipeline
- SSH deployment to self-hosted server via Docker

---

## 📁 Project Structure

```

ci-cd-nodejs/
├── .github/workflows/ci-cd.yml     # GitHub Actions pipeline
├── Dockerfile                      # Docker image definition
├── index.js                        # Express app entry point
├── package.json                    # NPM dependencies and scripts
├── test/
│   └── sample.test.js              # Jest test
└── .eslintrc.json                  # ESLint config

````

---

## 🧪 Run Locally

### 1. Clone the project

```bash
git clone https://github.com/YOUR_USERNAME/ci-cd-nodejs.git
cd ci-cd-nodejs
````

### 2. Install dependencies

```bash
npm install
```

### 3. Run the app

```bash
npm start
```

Visit: `http://localhost:3000`

---

## 🧹 Lint & Test

```bash
npm run lint
npm run test
```

---

## 🐳 Docker Commands

Build and run Docker container locally:

```bash
docker build -t node-app .
docker run -p 3000:3000 node-app
```

---

## ⚙️ GitHub Actions CI/CD

### Trigger

Push to the `main` branch triggers:

* Linting
* Testing
* Docker image build
* SSH deploy to server

### Secrets Required

| Name        | Description                    |
| ----------- | ------------------------------ |
| `SERVER_IP` | Your Linux server's IP address |
| `USERNAME`  | SSH username (e.g. `ubuntu`)   |
| `SSH_KEY`   | Private SSH key (no password)  |

> Add them in **GitHub > Repo > Settings > Secrets and variables > Actions**

---

## 📦 Deployment Details

The app runs on your server using Docker on port `3000`. Update the workflow file if needed to include a reverse proxy like Nginx or use Docker Compose for advanced setups.

---

## 👨‍💻 Author

* GitHub: [@fayis2000](https://github.com/fayis2000)

```

---

```
