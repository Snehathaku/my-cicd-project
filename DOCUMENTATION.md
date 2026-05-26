# CI/CD Compensation Task - Documentation

## 1. What I Learned

### CI/CD Basics
- **CI (Continuous Integration):** Automatically builds and tests code on every push
- **CD (Continuous Deployment):** Automatically deploys code after tests pass
- **Pipeline Flow:** Push Code → Build → Test → Deploy
- **Secrets:** Sensitive values stored securely in GitHub Settings, never exposed in logs

### GitHub Actions
- Workflows are defined in `.github/workflows/*.yml`
- `on: push` triggers the pipeline on every push
- `jobs` define what machine to run on (e.g. ubuntu-latest)
- `steps` are individual tasks inside a job
- `uses` runs pre-built actions (e.g. actions/checkout)

### Netlify Deployment
- Netlify connects directly to GitHub repository
- Auto-deploys on every push to `main` branch
- No manual deployment needed after initial setup

---

## 2. Steps Performed

### Step 1 - Project Setup
- Created project folder `my-cicd-project`
- Created `index.html`, `style.css`, `README.md`
- Initialized Git and made initial commit

### Step 2 - GitHub
- Created repository on GitHub: `Snehathaku/my-cicd-project`
- Pushed code to `main` branch

### Step 3 - GitHub Actions
- Created `.github/workflows/ci.yml`
- Configured workflow to trigger on push to `main`
- Pipeline runs on `ubuntu-latest`
- Steps: Checkout code → Validate files → CI Complete
- Verified green checkmark on GitHub Actions tab

### Step 4 - Netlify Deployment
- Created Netlify account and connected GitHub
- Imported `my-cicd-project` repository
- Deployed to: https://my-cicd-project.netlify.app
- Auto-deployment enabled on every push to `main`

---

## 3. Challenges Faced

- **"Nothing to commit" error:** Files were in parent folder, not inside `my-cicd-project`. Fixed by copying files using `cp` command.
- **Repository not found error:** GitHub repo wasn't created before running `git push`. Fixed by creating the repo on GitHub first.
- **Git password issue:** GitHub no longer accepts passwords — used Personal Access Token instead.

---

## 4. Live Project

- **GitHub Repo:** https://github.com/Snehathaku/my-cicd-project
- **Live Website:** https://my-cicd-project.netlify.app
- **CI Pipeline:** https://github.com/Snehathaku/my-cicd-project/actions