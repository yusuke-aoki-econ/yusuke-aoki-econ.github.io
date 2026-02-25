# Yusuke Aoki - Personal Academic Website

A static personal website hosted on GitHub Pages. Built with plain HTML, CSS, and JavaScript (no frameworks).

## File Structure

```
yusuke-aoki-econ.github.io/
├── index.html          # Home page
├── research.html       # Research page
├── presentation.html   # Presentation page
├── media.html          # Media & Commentary page
├── css/
│   └── style.css       # All styles
├── js/
│   └── main.js         # Navigation and interactivity
├── images/
│   ├── profile.jpg     # Profile photo
│   └── ogp.png         # OGP share image (1200x630)
├── files/
│   └── cv.pdf          # CV PDF (add your own)
├── .nojekyll           # Disables Jekyll processing
└── README.md
```

## Deploying to GitHub Pages

1. Push this repository to GitHub as `<username>.github.io`.
2. Go to **Settings** > **Pages** in your GitHub repository.
3. Under **Source**, select **Deploy from a branch**.
4. Choose `main` branch and `/ (root)` folder, then click **Save**.
5. Your site will be live at `https://<username>.github.io/` within a few minutes.

## Site URL

The site is hosted at `https://yusuke-aoki-econ.github.io/`.

## Updating Content

### Adding a New Paper (Research Page)

Open `research.html` and add a new entry inside the appropriate section:

```html
<div class="research-item">
  <div class="paper-title">
    <a href="https://link-to-paper.com">Paper Title Here</a>
  </div>
  <div class="authors">with Coauthor A, Coauthor B, and Coauthor C</div>
  <div class="venue">Journal Name, Volume, Year.</div>
</div>
```

For work in progress (no link), simply omit the `<a>` tag:

```html
<div class="research-item">
  <div class="paper-title">Paper Title Here</div>
  <div class="authors">with Coauthor A and Coauthor B</div>
</div>
```

### Adding a New Presentation

Open `presentation.html` and add:

```html
<div class="presentation-item">
  <div class="paper-title">
    <a href="https://link-to-paper.com">Paper Title</a>
  </div>
  <ul class="presentation-list">
    <li><a href="#">Conference Name (Location)</a></li>
  </ul>
</div>
```

### Adding a Media Entry

Open `media.html` and add a new `<li>` inside the `<ul class="contributions-list">`:

```html
<li>
  <span class="contrib-title" lang="ja"><a href="https://link.com">Title</a></span>
  <span class="contrib-meta" lang="ja">Publication, Date</span>
</li>
```

### Adding an Outlet to the Media List

Edit the `<p class="media-outlets">` paragraph in `media.html` to include the new outlet name.

## Replacing the Profile Photo

1. Prepare your photo (recommended: square, at least 400x400 pixels, JPG format).
2. Replace `images/profile.jpg` with your new photo, keeping the same filename.
3. If using a different filename, update the `<img src="...">` in `index.html`.
4. Commit and push.

## Adding Your CV

1. Place your CV PDF in the `files/` directory as `cv.pdf`.
2. If using a different filename, update the `href` in the CV floating button across all HTML files.

## Enabling Google Analytics

In each HTML file, find the commented-out Google Analytics block in `<head>`:

```html
<!-- TODO: Replace GA_MEASUREMENT_ID with your actual Google Analytics Measurement ID -->
<!--
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
...
-->
```

Replace `GA_MEASUREMENT_ID` with your actual measurement ID (e.g., `G-XXXXXXXXXX`) and uncomment the block.

## TODO Checklist

Search for `TODO` comments across the HTML files to find all placeholder items:
- [ ] CV PDF (`files/cv.pdf`)
- [ ] Google Analytics measurement ID (GA4)
- [ ] OGP share image — replace `images/ogp.png` with a custom design if desired
