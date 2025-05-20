Anonymous Secrets

Simple anonymous posting app with:

Express + Heroku backend for secure writes & filtering

Firebase Realtime DB for fast, client-side reads

bad-words filter blocks hateful slurs

Rate limiting for abuse protection

Setup

Backend (in backend/):

npm install
heroku create <app-name>
git push heroku main

Frontend (in frontend/):

Point to your Firebase config in <script>

Deploy on GitHub Pages or similar

Firebase Rules

{
  "secrets": { ".read": true, ".write": false }
}

Usage

Client uses onValue() to auto-refresh

All writes go through /api/secrets on Heroku

