# BizPro Template - Complete Documentation

## Table of Contents

1. [Installation Guide](#installation-guide)
2. [Customization Guide](#customization-guide)
3. [Deployment Guide](#deployment-guide)
4. [SEO Configuration](#seo-configuration)
5. [Theme Configuration](#theme-configuration)
6. [Troubleshooting](#troubleshooting)

---

## Installation Guide

### Step 1: Download the Template

Download and extract the template files to your local machine.

### Step 2: File Structure Overview

```
bizpro/
├── index.html              # Home page
├── portfolio.html          # Portfolio listing
├── portfolio-detail.html   # Single project page
├── blog.html              # Blog listing
├── blog-post.html         # Single blog post
├── about.html             # About us page
├── contact.html           # Contact page
├── 404.html               # Error page
├── assets/
│   ├── css/
│   │   ├── main.css       # Main styles
│   │   └── theme.css      # Theme/dark mode styles
│   ├── js/
│   │   └── main.js        # JavaScript functionality
│   └── images/            # Your images go here
├── sitemap.xml            # SEO sitemap
├── robots.txt             # Search engine instructions
└── README.md              # Quick reference
```

### Step 3: Open in Browser

Simply open `index.html` in your web browser to view the template.

### Step 4: Use a Local Server (Recommended)

For best results, use a local development server:

**Option 1: VS Code Live Server**
- Install "Live Server" extension in VS Code
- Right-click `index.html` and select "Open with Live Server"

**Option 2: Python Server**
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000`

**Option 3: Node.js Server**
```bash
npx serve
```

---

## Customization Guide

### Changing Colors

Edit the CSS variables in `assets/css/main.css`:

```css
:root {
    --primary-color: #2563eb;      /* Main brand color */
    --secondary-color: #7c3aed;    /* Accent color */
    --text-color: #1f2937;         /* Main text */
    --text-light: #6b7280;         /* Secondary text */
    --bg-color: #ffffff;           /* Background */
    --bg-alt: #f9fafb;            /* Alternate background */
}
```

### Changing Typography

Update font families in `assets/css/main.css`:

```css
body {
    font-family: 'Your Font', -apple-system, BlinkMacSystemFont, sans-serif;
}
```

To use Google Fonts, add to `<head>` in HTML files:

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
```

### Updating Content

#### Text Content
Simply edit the HTML files and replace placeholder text with your content.

#### Images
Replace placeholder backgrounds with your images:

**Method 1: Inline Styles**
```html
<div class="hero-placeholder" style="background-image: url('assets/images/hero.jpg');"></div>
```

**Method 2: CSS**
```css
.hero-placeholder {
    background-image: url('../images/hero.jpg');
    background-size: cover;
    background-position: center;
}
```

#### Logo
Replace the text logo in the header:

```html
<a href="index.html" class="logo">
    <img src="assets/images/logo.png" alt="BizPro">
</a>
```

### Navigation Menu

Edit navigation in each HTML file:

```html
<ul class="nav-menu" id="navMenu">
    <li><a href="index.html" class="nav-link">Home</a></li>
    <li><a href="portfolio.html" class="nav-link">Portfolio</a></li>
    <!-- Add more menu items -->
</ul>
```

### Footer

Update footer content in each HTML file:

```html
<footer class="footer">
    <div class="container">
        <!-- Update contact info, links, social media -->
    </div>
</footer>
```

### Adding New Pages

1. Duplicate an existing HTML file
2. Update the `<title>` and meta tags
3. Modify content as needed
4. Add link to navigation menu
5. Update `sitemap.xml`

### Contact Form

The contact form currently uses JavaScript to handle submissions. To connect to a backend:

**Option 1: Formspree**
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

**Option 2: Netlify Forms**
```html
<form name="contact" method="POST" data-netlify="true">
```

**Option 3: Custom Backend**
Update the form handler in `assets/js/main.js`

---

## Deployment Guide

### Option 1: GitHub Pages (Free)

1. Create a GitHub repository
2. Push your template files
3. Go to Settings > Pages
4. Select branch (usually `main`)
5. Click Save
6. Your site will be live at `https://username.github.io/repo-name`

**Custom Domain:**
- Add a `CNAME` file with your domain
- Configure DNS settings with your domain provider

### Option 2: Netlify (Free)

1. Sign up at [netlify.com](https://netlify.com)
2. Drag and drop your project folder
3. Site is live instantly!
4. Get a free subdomain or connect custom domain

**Continuous Deployment:**
- Connect your GitHub repository
- Auto-deploy on every push

### Option 3: Vercel (Free)

1. Sign up at [vercel.com](https://vercel.com)
2. Import your GitHub repository
3. Deploy with one click
4. Free SSL and custom domain support

### Option 4: Cloudflare Pages (Free)

1. Sign up at [pages.cloudflare.com](https://pages.cloudflare.com)
2. Connect your Git repository
3. Configure build settings (none needed for static site)
4. Deploy

### Option 5: Traditional Hosting

Upload files via FTP to any web hosting provider:
- Bluehost
- SiteGround
- HostGator
- GoDaddy
- etc.

---

## SEO Configuration

### Meta Tags

Update in each HTML file's `<head>`:

```html
<meta name="description" content="Your page description">
<meta name="keywords" content="keyword1, keyword2, keyword3">
<meta name="author" content="Your Name">
```

### Open Graph (Social Media)

```html
<meta property="og:title" content="Your Page Title">
<meta property="og:description" content="Your description">
<meta property="og:image" content="https://yoursite.com/image.jpg">
<meta property="og:url" content="https://yoursite.com">
```

### Twitter Cards

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Your Page Title">
<meta name="twitter:description" content="Your description">
<meta name="twitter:image" content="https://yoursite.com/image.jpg">
```

### Sitemap

Update `sitemap.xml` with your actual domain and pages:

```xml
<loc>https://yourdomain.com/page.html</loc>
<lastmod>2024-12-06</lastmod>
```

### Google Analytics

Add before closing `</head>` tag:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Schema Markup

Add structured data for better SEO:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "BizPro",
  "url": "https://yourwebsite.com",
  "logo": "https://yourwebsite.com/logo.png"
}
</script>
```

---

## Theme Configuration

### Light/Dark Mode

The template includes automatic theme switching. Users' preferences are saved in localStorage.

**Customize Dark Mode Colors:**

Edit `assets/css/theme.css`:

```css
[data-theme="dark"] {
    --primary-color: #3b82f6;
    --text-color: #f9fafb;
    --bg-color: #111827;
    /* ... more variables */
}
```

**Disable Dark Mode:**

Remove or comment out the theme toggle button in HTML files:

```html
<!-- <button class="theme-toggle" id="themeToggle">...</button> -->
```

### Layout Options

**Boxed Layout:**

Add to `assets/css/main.css`:

```css
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

body {
    background: #f0f0f0;
}

.container {
    background: white;
}
```

**Full Width:**

```css
.container {
    max-width: 100%;
    padding: 0 40px;
}
```

---

## Troubleshooting

### Images Not Showing

- Check file paths are correct
- Ensure images are in `assets/images/` folder
- Use relative paths: `assets/images/photo.jpg`

### Dark Mode Not Working

- Check JavaScript is enabled
- Verify `main.js` is loaded
- Clear browser cache

### Mobile Menu Not Opening

- Ensure `main.js` is loaded
- Check browser console for errors
- Verify nav IDs match JavaScript selectors

### Form Not Submitting

- Check form action attribute
- Verify backend endpoint
- Test with browser console open

### Styling Issues

- Clear browser cache
- Check CSS file paths
- Verify no conflicting styles
- Use browser DevTools to inspect

### Performance Issues

- Optimize images (use WebP format)
- Minify CSS and JavaScript
- Enable caching
- Use a CDN for assets

---

## Additional Resources

### Recommended Tools

- **Image Optimization:** TinyPNG, Squoosh
- **Icons:** Font Awesome, Heroicons
- **Fonts:** Google Fonts
- **Testing:** Google PageSpeed Insights, GTmetrix
- **SEO:** Google Search Console, Ahrefs

### Support

For additional help:
- Email: support@bizpro.com
- Documentation: Check README.md
- Community: GitHub Issues

---

## Changelog

### Version 1.0.0 (December 2024)
- Initial release
- 8 complete pages
- Light/dark mode
- Fully responsive
- SEO optimized
