# Development README

This file contains quick, PowerShell-friendly steps to run the project locally and notes about environment variables.

Prerequisites
- Node.js (LTS), npm
- Recommended Node >= 18

Install dependencies
```powershell
# From repository root
npm ci
```

Run the server in development
```powershell
# Uses cross-env to set NODE_ENV on Windows and Unix
npm run dev
```

Build (client + server bundle)
```powershell
npm run build
```

TypeScript check
```powershell
npm run check
```

Quick notes
- The project uses a monorepo-like layout: Vite client in `client/`, Express server in `server/`.
- Environment variables (refer to `.env.example`) are required for API keys and DB connection strings.
- The `dev` script now uses `cross-env` so `NODE_ENV` is set correctly on Windows PowerShell.

Docker
- The included `Dockerfile` builds a production image. See `DEPLOYMENT.md` for more details.

If you want, I can commit these two changes (`package.json` and `README-dev.md`) for you, then push to the current branch.