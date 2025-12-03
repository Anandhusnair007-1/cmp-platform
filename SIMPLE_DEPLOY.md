# Simple Deployment Guide (No Docker)

## 🚀 Deploy to Render.com (FREE - Easiest)

### 1. Sign Up
- Go to: https://render.com
- Click "Get Started for Free"
- Sign up with GitHub

### 2. Deploy Backend
1. Click "New +" → "Web Service"
2. Connect GitHub repository: `Anandhusnair007-1/cmp-platform`
3. Configure:
   - **Name**: `cmp-backend`
   - **Runtime**: `Go`
   - **Build Command**: `cd backend && go build -o bin/server ./cmd/inventory-service`
   - **Start Command**: `./backend/bin/server`
   - **Plan**: Free
4. Add Environment Variables:
   - `PORT`: 8080
   - `DATABASE_URL`: (will add after database is created)
5. Click "Create Web Service"

### 3. Deploy Database
1. Click "New +" → "PostgreSQL"
2. Configure:
   - **Name**: `cmp-postgres`
   - **Plan**: Free
3. Click "Create Database"
4. Copy the "Internal Database URL"
5. Go back to `cmp-backend` → Environment
6. Update `DATABASE_URL` with the database URL

### 4. Deploy Frontend
1. Click "New +" → "Static Site"
2. Connect same GitHub repository
3. Configure:
   - **Name**: `cmp-frontend`
   - **Build Command**: `cd frontend/webapp && npm install && npm run build`
   - **Publish Directory**: `frontend/webapp/dist`
4. Add Environment Variable:
   - `VITE_API_URL`: (your backend URL, e.g., `https://cmp-backend.onrender.com`)
5. Click "Create Static Site"

---

## 🌐 Alternative: Vercel + Railway

### Deploy Frontend on Vercel (FREE)
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy frontend
cd frontend/webapp
vercel --prod
```

### Deploy Backend on Railway (FREE)
1. Go to: https://railway.app
2. Click "Start a New Project"
3. Select "Deploy from GitHub repo"
4. Choose `cmp-platform`
5. Railway will auto-detect Go and deploy

---

## 🎯 Your Live URLs

After deployment:
- **Frontend**: `https://cmp-frontend.onrender.com`
- **Backend API**: `https://cmp-backend.onrender.com`
- **Database**: Internal (managed by Render)

---

## ✅ What You Get (FREE)

- ✓ Live backend API (Go)
- ✓ Live frontend website (React)
- ✓ PostgreSQL database
- ✓ SSL certificates (HTTPS)
- ✓ Auto-deploy on GitHub push
- ✓ Custom domains (optional)

---

## 📝 Quick Start

**Fastest way:**
1. Sign up: https://render.com
2. Click "New +" → "Blueprint"
3. Select your GitHub repo
4. Click "Apply"
5. Wait 10 minutes
6. Done! 🎉

Your app will be live with no Docker needed!
