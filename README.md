index.html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <!-- SEO meta -->
  <title>Accessible Semantic Sample — HTML5, Accessibility & SEO Best Practices</title>
  <meta name="description" content="A concise accessible and semantic HTML5 example demonstrating best practices for structure, headings, accessibility attributes, and SEO-friendly metadata.">
  <link rel="canonical" href="https://example.com/index.html">
  <meta name="robots" content="index, follow">

  <!-- Open Graph / Social -->
  <meta property="og:title" content="Accessible Semantic Sample — HTML5 Best Practices">
  <meta property="og:description" content="Semantic HTML5 template with accessibility enhancements and SEO-friendly metadata.">
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://example.com/index.html">
  <meta property="og:image" content="https://example.com/preview-image.png">

  <!-- Structured data (Schema.org) for improved SEO -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "WebSite",
    "name": "Accessible Semantic Sample",
    "url": "https://example.com/",
    "description": "Sample HTML5 page demonstrating semantic structure, accessibility, and SEO best practices."
  }
  </script>

  <!-- Simple styles for demonstration (kept inline for single-file delivery) -->
  <style>
    :root{font-family:system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial;line-height:1.5;color:#111}
    a:focus, button:focus, input:focus {outline:3px solid Highlight; outline-offset:2px}
    header, main, footer, nav, article, aside {padding:1rem}
    .container{max-width:900px;margin:0 auto;padding:1rem}
    nav ul{list-style:none;padding:0;margin:0;display:flex;gap:0.5rem}
    nav a{display:inline-block;padding:0.25rem 0.5rem;text-decoration:none}
    .hero{background:#f5f5f5;padding:1rem;border-radius:8px}
    .sr-only{position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;clip:rect(0 0 0 0);white-space:nowrap;border:0}
  </style>
</head>
<body>
  <!-- Skip link for keyboard users -->
  <a class="sr-only" href="#main-content">Skip to main content</a>

  <div class="container">
    <header role="banner" aria-label="Main header">
      <h1>Accessible Semantic Sample</h1>
      <p class="hero" id="intro">This single-file HTML demonstrates semantic HTML5 elements, correct heading hierarchy, accessibility enhancements, and SEO-friendly metadata.</p>

      <nav role="navigation" aria-label="Primary navigation">
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#features">Features</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>

    <main id="main-content" role="main" aria-labelledby="main-heading">
      <h2 id="main-heading">Why semantic HTML & accessibility matter</h2>
      <article aria-labelledby="article-heading">
        <h3 id="article-heading">Benefits for users and search engines</h3>
        <p>Semantic HTML improves the structure and meaning of your pages, helping assistive technologies (screen readers, braille displays), search engines, and maintenance by developers. Using elements such as <code>&lt;header&gt;</code>, <code>&lt;nav&gt;</code>, <code>&lt;main&gt;</code>, <code>&lt;article&gt;</code>, and <code>&lt;footer&gt;</code> communicates intent clearly.</p>

        <section id="features" aria-labelledby="features-heading">
          <h4 id="features-heading">Key accessibility and SEO features in this file</h4>
          <ul>
            <li>Document language declared with <code>lang</code>.</li>
            <li>Descriptive <code>&lt;title&gt;</code> and <code>meta description</code> for SEO.</li>
            <li>Skip link for keyboard users and visible focus styles.</li>
            <li>Meaningful heading hierarchy (H1 → H2 → H3 → H4).</li>
            <li>Accessible form controls with explicit <code>&lt;label&gt;</code>s and <code>aria-describedby</code>s.</li>
            <li>Structured data (JSON-LD) for better search result representation.</li>
          </ul>
        </section>

        <figure aria-labelledby="figure-caption">
          <img src="https://example.com/sample-screen.png" alt="Screenshot of a semantic HTML structure diagram" width="800" height="400">
          <figcaption id="figure-caption">Figure: Example semantic page structure to help screen reader users and improve SEO.</figcaption>
        </figure>
      </article>

      <aside aria-labelledby="aside-heading">
        <h3 id="aside-heading">Quick tips</h3>
        <ul>
          <li>Use descriptive link text (avoid "click here").</li>
          <li>Keep meta descriptions concise (120–160 characters).</li>
          <li>Provide alt text for all informative images; decorative images should have empty alt (<code>alt=""</code>).</li>
        </ul>
      </aside>

      <section id="contact" aria-labelledby="contact-heading">
        <h2 id="contact-heading">Contact / Example form</h2>
        <form action="/submit" method="post" aria-describedby="form-desc">
          <p id="form-desc">Use this form to request more information. Fields are labelled and keyboard-accessible.</p>

          <div>
            <label for="name">Full name</label>
            <input id="name" name="name" type="text" required aria-required="true" placeholder="Jane Doe">
          </div>

          <div>
            <label for="email">Email address</label>
            <input id="email" name="email" type="email" required aria-required="true" placeholder="you@example.com">
          </div>

          <div>
            <label for="message">Message</label>
            <textarea id="message" name="message" rows="4" aria-describedby="message-help"></textarea>
            <small id="message-help">Tell us why you'd like more information (optional).</small>
          </div>

          <button type="submit">Send request</button>
        </form>
      </section>

    </main>

    <footer role="contentinfo">
      <p>&copy; <time datetime="2025-09-17">2025</time> Accessible Semantic Sample — <a href="/privacy">Privacy</a></p>
    </footer>
  </div>
</body>
</html>
