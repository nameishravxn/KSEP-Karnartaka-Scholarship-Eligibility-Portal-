

1. Create a GitHub repository and upload `index.html`, `styles.css`, `config.js`, and `app.js` to its root.
2. In the repository, open **Setting# KSEP (Karnataka Scholarship Eligibility Portal)

A Kannada-first, bilingual scholarship finder for Karnataka government school students. The frontend is plain HTML, CSS, and JavaScript: no package install or build step is needed.

## Run it on your Mac

From this folder, run:

```sh
python3 -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000). Keep the terminal open while using the app; press `Control+C` to stop the local server.

## Publish with GitHub Pagess → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select your default branch and the `/ (root)` folder, then save.
4. GitHub will show the site URL in the Pages section after deployment.

The app is static-hosting friendly, so GitHub Pages can serve it directly. No GitHub Actions workflow or build command is required.

## Student privacy and staff tools

Student eligibility answers are held in JavaScript memory only. They are not written to browser storage or sent to the server. The language preference is stored locally. If configured, the app sends only class, category, and a zero-result boolean to the anonymous aggregate-counter endpoint.

Staff login, scheme publishing, announcements, and dashboards require a Supabase project. Add its **project URL** and **public anon key** to `config.js`; never add a service-role key to frontend files. The database schema, access policies, initial admin setup, and sample draft schemes must also be installed in Supabase before enabling staff tools. Without that backend, the student pages and eligibility wizard run, and the staff login page explains that staff setup is pending.

Only published schemes are shown to students. Sample schemes must remain drafts and use the source label `SAMPLE DATA — replace with verified scheme before publishing.` Do not publish placeholders as real scholarship guidance.

## Pages

- Student home, Kannada/English toggle, eligibility wizard, results, scheme details, Help/FAQ, and About.
- Staff sign-in, dashboard, scheme editor, announcements, and admin account management (available after backend setup).