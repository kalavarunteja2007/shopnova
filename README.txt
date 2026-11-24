SHOPNOVA — HTML / CSS / JS (Separated) + Full Source + Vercel Deploy
=====================================================================
01-built-app-separated/   The compiled app, split into 3 separate parts:
  html/index.html           -> open this (links to ../css/style.css and ../js/script.js)
  css/style.css             -> all compiled CSS (Tailwind)
  js/script.js              -> all compiled JavaScript (React app bundle)
  NOTE: keep the html/css/js folder structure together. The JS calls /api/* —
  for a pure static preview use the Vercel deploy folder below (API included).

02-full-source/shopnova/  Complete editable source (client/src .jsx/.css, server/, tests/)
03-vercel-deploy/shopnova-vercel/  Same project with vercel.json + api/index.js — deploy THIS folder.
  Deploy:  cd 03-vercel-deploy/shopnova-vercel && npx vercel deploy --prod --token <YOUR_TOKEN>
  Or:      go to vercel.com/new and import/upload this folder.

VERCEL NOTE: Frontend is served from client_bundle (Vite build). The Express API runs as a
serverless function (api/index.js). SQLite runs on ephemeral /tmp storage on Vercel — data
resets on cold starts and better-sqlite3 is a native module, so for production persistence
use a hosted DB (Turso/Postgres) and host the API on Render/Railway. See docs in 02-full-source.
