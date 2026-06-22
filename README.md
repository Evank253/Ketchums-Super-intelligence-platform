# Ketchum Super Intelligence Platform

**Production-ready deployment instructions**

## Deploy to Render (Recommended)

1. Go to [render.com](https://render.com) and create a new **Web Service**
2. Connect your GitHub repo: `Ketchum-super-intelligence-platform`
3. Use these settings:

   - **Name**: `ketchum-super-intelligence`
   - **Environment**: `Python 3`
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `gunicorn --bind 0.0.0.0:$PORT --workers 4 webapp.app:app`
   - **Instance Type**: Free or Starter

4. Add these **Environment Variables**:
   - `FLASK_ENV` = `production`
   - `PYTHONUNBUFFERED` = `1`

5. Click **Create Web Service**

Your app will be live at: `https://ketchum-super-intelligence.onrender.com`

---

## Deploy to Railway

1. Go to [railway.app](https://railway.app)
2. Create new project → Deploy from GitHub
3. Select your repo
4. Railway will auto-detect the `Procfile`
5. Add environment variable:
   - `FLASK_ENV` = `production`

---

## Environment Variables (Required)

| Variable          | Value          | Required |
|-------------------|----------------|----------|
| `FLASK_ENV`       | `production`   | Yes      |
| `PYTHONUNBUFFERED`| `1`            | Yes      |

---

## Subscription Plans (Live in Production)

| Plan     | Price | Daily Allowance     |
|----------|-------|---------------------|
| Free     | $0    | 5 computations      |
| Pro 25   | $25   | 35 tokens           |
| Pro 50   | $50   | 75 tokens           |
| Pro 100  | $100  | 200 tokens          |

---

**This platform is now ready for production deployment.**
