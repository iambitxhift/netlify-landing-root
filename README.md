# Netlify Landing (Root Publish)

This repo is a **minimal landing page** for Netlify. It publishes from the **repo root** (no base directory).

## Files
- `index.html` – simple landing page with a button
- `style.css` – minimal styling
- `netlify.toml` – forces Netlify to publish from `.` and route all paths to `index.html`

## Usage
1. Push these files to a new GitHub repo.
2. On Netlify → New site from Git → select the repo.
3. **Build settings** (or leave to `netlify.toml`):
   - Base directory: *(leave empty)*
   - Build command: *(empty)*
   - Publish directory: `.`
4. Edit the button link inside `index.html` and set it to your Streamlit app URL.

### Auto-redirect (optional)
If you want Netlify to **redirect immediately** to your Streamlit app (no landing page), create a file named `_redirects` at the repo root with:

```
/* https://YOUR-STREAMLIT-APP.streamlit.app/:splat 301!
```

Commit and push.
