# Meeting Calendar Hub

This is a static HTML app that connects to Supabase and can be hosted on GitHub Pages.

## Deploy to GitHub Pages

1. Create a GitHub repository.
2. Copy `Index.html` into the repository root.
3. From your project folder, run:

```bash
git init
git add Index.html README.md
git commit -m "Initial deploy"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

4. Open your repository on GitHub.
5. Go to `Settings` → `Pages`.
6. Under `Source`, select `main` branch and `/(root)` folder.
7. Save.

Your site will publish at:

```
https://<your-username>.github.io/<your-repo>/
```

## Supabase setup

The app is already configured with a Supabase project URL and key.

You must create a table named `meetings` with these columns:

- `id` (primary key)
- `title` (text)
- `owner_id` (integer)
- `start_date` (date)
- `end_date` (date)
- `time` (text)
- `status` (text)
- `location` (text)
- `description` (text)

If you want the app to read/write from the browser, enable public access or configure Row Level Security policies for the `meetings` table.

## Notes

- Keep `Index.html` in the repo root.
- When the site is published, the app will load from the public URL and access Supabase from anywhere.
- If you change the Supabase project, update the URL and key in `Index.html`.
