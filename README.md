# 360Learning Hero Widget Template

A branded hero widget for embedding on a client's 360Learning demo homepage. Customise the brand colour and button links, deploy to GitHub Pages, then drop the embed code into the platform.

---

## What you need

- A free [GitHub account](https://github.com/signup)
- The client's primary brand colour (as a hex code, e.g. `#0057FF`)

---

## Step 1 — Create your own copy

1. Go to the template repo on GitHub
2. Click **Use this template** → **Create a new repository**
3. Name it something like `acme-hero-widget` (use the client name)
4. Set visibility to **Public** (required for free GitHub Pages hosting)
5. Click **Create repository**

---

## Step 2 — Customise the colours

1. Open `index.html` in GitHub (click the file, then the pencil ✏️ icon to edit)
2. At the very top of the `<style>` block, find this section:

```css
:root {
  --brand:       #00b28a;
  --brand-hover: #009e7a;
  --brand-light: #e8faf4;
}
```

3. Replace the three values:
   - **`--brand`** → the client's primary brand colour
   - **`--brand-hover`** → a slightly darker shade of the same colour (for button hover states)
   - **`--brand-light`** → a very light tint of the same colour (for icon backgrounds)

> **Tip:** If you only know the main colour, use [color-hex.com](https://www.color-hex.com) to find darker and lighter shades. Search for the client's hex code and it will show you a full range of tints and shades to pick from.

---

## Step 3 — Update the button links

Still in `index.html`, find the two lines marked `<!-- EDIT: Replace href ... -->` and update the `href` values to the relevant pages on the client's demo site:

```html
<!-- EDIT: Replace href with the relevant URL from the client's demo site -->
<a class="btn-primary" href="YOUR_URL_HERE" ...>Share your expertise</a>

<!-- EDIT: Replace href with the relevant URL from the client's demo site -->
<a class="btn-secondary" href="YOUR_URL_HERE" ...>Take a 2-min tour</a>
```

4. Click **Commit changes** at the bottom of the page

---

## Step 4 — Enable GitHub Pages

1. In your repo, go to **Settings** (top navigation bar) → **Pages**
2. Under **Branch**, select `main` and click **Save**
3. After ~30 seconds, your widget will be live at:
   `https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPO-NAME/`

---

## Step 5 — Embed in 360Learning

Paste the following into the 360Learning homepage HTML widget, then replace the `src` URL with your live GitHub Pages URL from Step 4:

```html
<iframe
  class="lw_hero_widget"
  src="https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPO-NAME/"
  frameborder="0"
  scrolling="no"
  allowtransparency="true">
</iframe>

<style>
.lw_hero_widget {
  border: none;
  width: 100%;
  height: 345px;
  display: block;
  background: transparent;
}
</style>
```

---

## Making further changes

Any time you edit `index.html` and commit, GitHub Pages will rebuild automatically. Allow ~30 seconds for changes to go live.
