SC153/0169/2024
KIVAI ERIC YALO

# Inkspark Blog

A minimal static blog (Inkspark-blog). This README explains the repository structure and walks through the code step‑by‑step so you (or contributors) can understand how each part works and where to change things. Screenshots placeholders are included for you to replace with actual images.

---

Table of contents
- About
- Quick start
- Project structure
- index.html — step-by-step code walkthrough
  - head (meta, styles, fonts)
  - layout (header, navigation, hero, posts list, sidebar, footer)
  - post markup explained
  - scripts and behavior
- Screenshots (placeholders)
- Contributing
- License

---

About
A simple static blog delivered as HTML/CSS The main entry point is `index.html`.



index.html — step-by-step code walkthrough
Below is a generic annotated breakdown of a typical static blog `index.html`. Open your repository's `index.html` and compare each section.

1) Document head — meta, title, and styles
- Purpose: declares page title, character set, viewport, links to CSS and fonts, and provides SEO meta tags.
- Typical snippet:
  ```html
  <!doctype html>
  <html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Inkspark — Blog</title>
    <meta name="description" content="Short description for search engines" />
    <!-- CSS -->
    <link rel="stylesheet" href="styles.css" />
    <!-- Favicons, fonts -->
    <link rel="icon" href="favicon.ico" />
  </head>
  ```
- Explanation:
  - `<!doctype html>`: enables standards mode.
  - `<meta charset>`: sets encoding to UTF-8.
  - `<meta name="viewport">`: ensures the site is responsive on mobile.
  - `<title>`: appears in browser tabs and search engine results.
  - `link rel="stylesheet"`: includes your CSS file(s).
  - screenshot(<img width="870" height="609" alt="image" src="https://github.com/user-attachments/assets/844fe802-272b-4a7e-baef-e58194c0bb4c" />

  - 

2) Layout — header, navigation, hero
- Header / nav: contains site logo/title and links to categories or pages.
  ```html
  <header class="site-header">
    <div class="container">
      <a class="logo" href="/">Inkspark</a>
      <nav class="main-nav">
        <a href="#posts">Blog</a>
        <a href="/about.html">About</a>
      </nav>
    </div>
  </header>
  ```
  Explanation:
  - `.logo` is the clickable site title — change text or replace with an image.
  - `.main-nav` holds navigation links. For multi-page sites, update `href` accordingly.
Here is the screenshot(![2](https://github.com/user-attachments/assets/9c69463d-b542-4c1b-84b4-94c154085810)




3) Posts list (main content)
- Typical pattern for each post (static HTML):
  ```html
  <main id="posts">
    <article class="post">
      <h2 class="post-title"><a href="post-1.html">Post title</a></h2>
      <p class="post-meta">Jan 30, 2026 · Author</p>
      <p class="post-excerpt">A short summary or excerpt of the post content...</p>
      <a class="read-more" href="post-1.html">Read more →</a>
    </article>
    <!-- Repeat article blocks for each post -->
  </main>
  ```
- Explanation (line-by-line):
  - `<main id="posts">`: main content region for accessibility and layout.
  - `<article class="post">`: semantic container for a single blog post preview.
  - `<h2 class="post-title">`: title; usually links to the full post page.
  - `<p class="post-meta">`: metadata like date and author.
  - `<p class="post-excerpt">`: short excerpt or summary.
  - `<a class="read-more">`: link to the single-post page.
 
    Here is the screenshot(<img width="1228" height="535" alt="image" src="https://github.com/user-attachments/assets/4b92acf9-832e-48d7-b4ba-f13966d85313"

    
5) Footer
- Typical content: copyright, links to social, theme credits.
  ```html
  <footer class="site-footer">
    <p>© 2026 Inkspark. All rights reserved.</p>
  </footer>
  ```
Here is the screenshot(<img width="1349" height="300" alt="image" src="https://github.com/user-attachments/assets/1a610eab-0220-4566-bcdb-d4a8069b1653" />

6) Scripts and behavior
- If `index.html` includes scripts, they may:
  - Provide interactivity (menu toggle, search).
  - Fetch posts via JSON (e.g., `fetch('/posts.json')`) and render them.
  - Add analytics or performance optimizations.
- Typical placement:
  ```html
  <!-- placed at bottom for performance -->
  <script src="scripts/main.js"></script>
  ```
- How to inspect:
  - Open `scripts/main.js` (if present) and look for `document.querySelector`, `addEventListener`, `fetch()`, or templating functions that insert HTML into the DOM.

Post markup — annotated example
```html
<article class="post">
  <!-- Title: clickable link to the full article -->
  <h2 class="post-title"><a href="post-1.html">How to Write a README</a></h2>
  <!-- Meta: date, author -->
  <p class="post-meta">Jan 30, 2026 · Kyalo-ai</p>
  <!-- Excerpt: short summary that encourages clicking "Read more" -->
  <p class="post-excerpt">This guide explains how to write a README step-by-step...</p>
  <!-- Read more: link to the post details -->
  <a class="read-more" href="post-1.html">Read more →</a>
</article>
```

Accessibility & SEO notes
- Use semantic HTML: `<main>`, `<article>`, `<nav>`, `<header>`, `<footer>`.
- Add `alt` attributes to images.
- Ensure color contrast for text.
- Add meaningful `<title>` and meta description.
- Use heading hierarchy (`h1` on page, then `h2` for sections).

Screenshots


Homepage
![Homepage screenshot](<img width="1346" height="650" alt="image" src="https://github.com/user-attachments/assets/5139b4da-fb6c-43ca-bee5-78f1eeb0229f" />

)
code screenshot code(<img width="930" height="358" alt="image" src="https://github.com/user-attachments/assets/80929e42-5dd1-4497-ab06-9806278c0de4" />
code screenshot(<img width="877" height="378" alt="image" src="https://github.com/user-attachments/assets/9d998f79-917e-4a9b-a832-3a1f0c6e7380" />



Post page
![Post page screenshot](<img width="461" height="620" alt="image" src="https://github.com/user-attachments/assets/9e671836-340a-4324-98cd-d622ae6e76e5" />
)

Admin / Editing workflow (optional)
![Editing screenshot](screenshots/editing.png)

Animation code style(<img width="769" height="199" alt="image" src="https://github.com/user-attachments/assets/8a5bfc70-975b-45e9-881f-516841495dc6" />
animation code(<img width="456" height="491" alt="image" src="https://github.com/user-attachments/assets/2f539f16-a922-4f63-8980-ced7cf6732c3" />

whole blog(<img width="1334" height="731" alt="image" src="https://github.com/user-attachments/assets/36fc7bad-5b5c-4e47-bdab-bcbda1fbf20e" />


