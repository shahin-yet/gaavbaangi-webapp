# Gaavbaangi Conservation webapp — Simple Setup Guide

This guide is for non-technical users. Follow the steps in order to get the app live.

## 1) Create your accounts (free)
- GitHub: Create an account and sign in.
- Supabase: Create an account at https://supabase.com and sign in.

## 2) Put the project on GitHub
1. In GitHub, click New repository → name it (e.g., `gaavbaangi-webapp`) → Public → Create.
2. Upload these files to the repository root:
   - `index.html`
   - `app.js`
   - `styles.css`
   - (optional) `gitignore.txt`

## 3) Create a Supabase project
1. In the Supabase dashboard, click New Project.
2. Choose an organization, set a strong database password, and create the project.
3. Wait a few minutes until it finishes setting up.

## 4) Get your Supabase URL and anon key
1. Supabase → Project Settings → API.
2. Copy:
   - Project URL (like `https://xxxx.supabase.co`)
   - anon public key

## 5) Add your keys to the app
1. In your GitHub repo, open `index.html`.
2. Near the bottom, find:
```html
<script>
  window.SUPABASE_URL = 'https://YOUR-PROJECT-REF.supabase.co';
  window.SUPABASE_ANON_KEY = 'YOUR-ANON-KEY';
</script>
```
3. Replace with your actual values and save.

## 6) Deploy with GitHub Pages
1. In your GitHub repo → Settings → Pages.
2. Source: Deploy from a branch.
3. Select branch `main` and folder `/ (root)`.
4. Save and wait 1–3 minutes.
5. Your site URL will appear (e.g., `https://your-username.github.io/gaavbaangi-webapp`).

## 7) Test the app
- Open your site URL. The map should load.
- If you already have data in Supabase, polygons and pathlines will render.
- Saving polygons will be enabled when the app sets up the database in a later step.

## 8) (Optional) Use as a Telegram Mini App
1. In Telegram, talk to `@BotFather` → `/newbot` → follow prompts.
2. In `@BotFather` → your bot → Bot Settings → Web App → paste your GitHub Pages URL.
3. Open your bot and tap the menu to launch the web app.

## Quick fixes
- Nothing loads: check your `SUPABASE_URL` and `SUPABASE_ANON_KEY` in `index.html`.
- Data not visible: add sample rows in Supabase tables or wait for the app’s setup step.
- Still stuck? Open the browser Console for error messages and share them.
