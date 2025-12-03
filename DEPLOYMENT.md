# Deploy CMP Platform to Cloud

## 🚀 Free Deployment Options

### Option 1: Render.com (Recommended)

1. **Sign up at**: https://render.com (use your GitHub account)
2. **Connect your repository**: `Anandhusnair007-1/cmp-platform`
3. **Click**: "New" → "Blueprint"
4. **Select**: Your `cmp-platform` repository
5. Render will automatically detect `render.yaml` and deploy all services
6. **Wait 5-10 minutes** for deployment

**Your live URLs will be:**
- Frontend: `https://cmp-frontend.onrender.com`
- API: `https://cmp-inventory.onrender.com`

---

### Option 2: Railway.app

1. **Sign up at**: https://railway.app
2. **Click**: "New Project" → "Deploy from GitHub repo"
3. **Select**: `cmp-platform`
4. **Add services** one by one:
   - PostgreSQL database
   - Backend services
   - Frontend

---

### Option 3: Fly.io

```bash
# Install Fly CLI
curl -L https://fly.io/install.sh | sh

# Login
fly auth login

# Deploy
fly launch
```

---

## 🎯 Easiest Method: Render.com

**Step-by-step:**

1. Go to https://render.com
2. Click "Get Started for Free"
3. Sign up with GitHub
4. Click "New +" → "Blueprint"
5. Select `Anandhusnair007-1/cmp-platform`
6. Click "Apply"

**Done!** Your app will be live in 10 minutes.

---

## 📊 What Gets Deployed:

✅ PostgreSQL database (free tier)
✅ All 3 backend services (Go)
✅ Frontend (React app)
✅ Auto-deploy on every GitHub push

---

## 💰 Cost:

**FREE** for small projects!
- Render.com: Free tier includes everything
- Auto-sleep after 15 min inactivity (wakes on request)

---

## 🔗 After Deployment:

Update GitHub Pages to link to your live app:
1. Get your Render URLs
2. Update `docs/index.html` with live demo link
3. Push to GitHub
