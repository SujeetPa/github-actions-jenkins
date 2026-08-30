# GitHub Actions + Jenkins Integration

## How It Works
```
GitHub Push → GitHub Actions → Triggers Jenkins Job
```

## Setup

### 1. Add GitHub Secrets
Go to: Repo → Settings → Secrets → Actions → New repository secret

| Secret | Value |
|--------|-------|
| JENKINS_URL | 3.89.31.130:8443 |
| JENKINS_JOB | eks-pipeline |
| JENKINS_USER | admin |
| JENKINS_TOKEN | (Jenkins API token) |

### 2. Get Jenkins API Token
1. Jenkins → Click username (top right) → Configure
2. API Token → Add new token → Generate
3. Copy token

### 3. Push Code
```bash
git add .
git commit -m "Trigger Jenkins"
git push
```

GitHub Actions will trigger Jenkins job automatically!
