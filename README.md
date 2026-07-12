# Setup guide

## 1. Fill in your details
Every file has `[Apartment Complex Name]`, `[City, State]`, and similar placeholders —
do a find-and-replace across all files (`index.html`, `timeline.html`, `evidence.html`)
for each bracketed placeholder. The two most important ones for Google are the
`<title>` and `<meta name="description">` lines at the top of `index.html`.

## 2. Put it on GitHub Pages (free hosting)
1. Create a free GitHub account if you don't have one: https://github.com/join
2. Click **New repository**. Name it something like `apartment-maintenance-record`.
   Make it **Public**.
3. On the new repo page, click **uploading an existing file** and drag in every file
   from this folder (`index.html`, `timeline.html`, `evidence.html`, `styles.css`,
   `robots.txt`, `sitemap.xml`, and the `evidence/` folder with your photos inside it).
   Commit the changes.
4. Go to **Settings → Pages** in your repo. Under "Build and deployment," set
   **Source** to "Deploy from a branch," branch `main`, folder `/ (root)`. Save.
5. Wait ~1 minute, then refresh — GitHub shows your live URL, something like
   `https://yourusername.github.io/apartment-maintenance-record/`.
6. Go back into `index.html`, `robots.txt`, and `sitemap.xml` and replace
   `YOUR-GITHUB-USERNAME` and `YOUR-REPO-NAME` with your real values, then
   re-upload those files to overwrite them.

## 3. Add evidence
- Put photos/screenshots inside `evidence/<case-name>/` folders (a starter one exists).
- Keep filenames descriptive: `ceiling-stain-2026-03-03.jpg`.
- In `evidence.html`, duplicate a `<figure class="evidence-card">` block per image
  and update the `src`, `alt`, date, case ID, and caption.

## 4. Add a new case
Three files need a matching entry — use the same case ID (e.g. `MX-2026-014`) in all three:
- `index.html` — one row in the ledger table
- `timeline.html` — one `<article class="timeline-entry" id="mx-2026-014">` block
- `evidence.html` — one or more `<figure>` blocks for photos tied to that case

## 5. Get it indexed by Google fast
Waiting for organic crawling can take weeks. To speed it up:
1. Go to https://search.google.com/search-console and add your site (use the URL prefix
   method with your `github.io` URL).
2. Verify ownership — Search Console gives you an HTML file to add to the repo, or you
   can verify via the meta tag it provides (add it to the `<head>` of `index.html`).
3. Once verified, go to **Sitemaps** in the left menu and submit `sitemap.xml`.
4. Use **URL Inspection** on your homepage URL and click **Request Indexing**.
5. This typically gets the page indexed within a few days.

## 6. Build backlinks (helps ranking a lot)
A link from any other site pointing at yours is one of the strongest signals to Google
that a page is worth ranking. A few free, low-effort options:
- Post about it in the apartment's local subreddit or neighborhood Facebook group.
- Leave a Google Maps / Yelp / ApartmentRatings review for the complex that links to
  the site as your source of documentation.
- If a local tenants' rights organization has a resource page, ask if they'll link to it.

## A note on content
Stick to dated facts you can back up (what was reported, when, and the response) and
keep any opinions in a clearly separate, clearly labeled section. This keeps the page
useful and defensible.
