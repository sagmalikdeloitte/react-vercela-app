# Simple React App with Auto Vercel Deploy

This project is a simple React app created with Vite and configured for automatic deployment to Vercel via GitHub Actions.

## Run locally

1. Install dependencies:

```bash
npm install
```

2. Start development server:

```bash
npm run dev
```

3. Build for production:

```bash
npm run build
```

## Automatic Vercel deployment setup

The workflow file is at `.github/workflows/deploy-vercel.yml`. It deploys automatically on every push to `main`.

1. Push this project to a GitHub repository.
2. In Vercel, import the GitHub repository once and let Vercel create the project.
3. In your GitHub repo, add these Actions secrets:
	- `VERCEL_TOKEN`
	- `VERCEL_ORG_ID`
	- `VERCEL_PROJECT_ID`

You can get these values with the Vercel CLI:

```bash
npm i -g vercel
vercel login
vercel link
```

After that, every push to `main` will trigger an automatic production deploy on Vercel.
