# Nuanced Therapy Colorado

Static website for Nuanced Therapy Colorado — four pages: Home, Meet the Therapist,
What I Do, and Contact Me.

## Editing content

Every spot that needs your real information is marked with a highlighted
`[PLACEHOLDER: ...]` tag. Open each `.html` file and search for `PLACEHOLDER`
to find them all:

- `index.html` — homepage intro and services teaser
- `meet-the-therapist.html` — bio, credentials, approach
- `what-i-do.html` — specialties, rates, insurance, FAQ
- `contact.html` — email, phone, location, hours

To add your photo, replace the `.portrait` div in `meet-the-therapist.html`
with an `<img src="assets/your-photo.jpg" alt="...">` tag, and drop the photo
file in the `assets/` folder.

## Previewing locally

Open `index.html` directly in a browser, or serve the folder locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publishing on GitHub Pages

1. Create a new repository on GitHub (e.g. `nuanced-therapy-colorado`).
2. Push this folder to it:

   ```bash
   git remote add origin https://github.com/<your-username>/nuanced-therapy-colorado.git
   git branch -M main
   git push -u origin main
   ```

3. On GitHub, go to the repo's **Settings → Pages**.
4. Under "Build and deployment", set **Source** to "Deploy from a branch",
   branch `main`, folder `/ (root)`. Save.
5. Your site will be live at `https://<your-username>.github.io/nuanced-therapy-colorado/`
   within a few minutes.

### Custom domain (optional)

If you buy a domain (e.g. `nuancedtherapycolorado.com`), add it under
Settings → Pages → Custom domain, and create a `CNAME` DNS record at your
domain registrar pointing to `<your-username>.github.io`.

## A note on contact forms

GitHub Pages only hosts static files — it can't process form submissions.
This site uses simple `mailto:` and `tel:` links instead. If you'd rather have
an on-page contact form, a service like [Formspree](https://formspree.io) can
be added later without needing a backend server.
