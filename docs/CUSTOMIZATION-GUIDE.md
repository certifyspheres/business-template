# Quick Customization Guide

This guide will help you quickly customize the BizPro template for your needs.

## 🎨 Change Brand Colors (5 minutes)

1. Open `assets/css/main.css`
2. Find the `:root` section at the top
3. Change these values:

```css
:root {
    --primary-color: #2563eb;    /* Your main brand color */
    --secondary-color: #7c3aed;  /* Your accent color */
}
```

**Color Picker Tools:**
- [Coolors.co](https://coolors.co)
- [Adobe Color](https://color.adobe.com)

## 📝 Update Site Content (10 minutes)

### Company Name
Search and replace "BizPro" with your company name in all HTML files.

### Contact Information
Update in footer of each HTML file:
- Email: `info@bizpro.com` → your email
- Phone: `+1 (555) 123-4567` → your phone
- Address: Update to your address

### Social Media Links
In footer, update `href="#"` with your actual social media URLs:

```html
<a href="https://facebook.com/yourpage" aria-label="Facebook">📘</a>
<a href="https://twitter.com/yourhandle" aria-label="Twitter">🐦</a>
```

## 🖼️ Add Your Images (15 minutes)

### Method 1: Replace Placeholders with Images

Find elements with placeholder backgrounds and add your images:

```html
<!-- Before -->
<div class="hero-placeholder"></div>

<!-- After -->
<div class="hero-placeholder" style="background-image: url('assets/images/hero.jpg'); background-size: cover; background-position: center;"></div>
```

### Method 2: Use <img> Tags

```html
<img src="assets/images/your-photo.jpg" alt="Description">
```

### Image Recommendations:
- **Hero images:** 1920x1080px
- **Portfolio items:** 800x600px
- **Blog images:** 1200x630px
- **Team photos:** 500x500px
- **Format:** JPG for photos, PNG for graphics, WebP for best performance

### Free Stock Photos:
- [Unsplash](https://unsplash.com)
- [Pexels](https://pexels.com)
- [Pixabay](https://pixabay.com)

## 🔤 Change Fonts (5 minutes)

### Using Google Fonts:

1. Visit [Google Fonts](https://fonts.google.com)
2. Select your fonts
3. Add to `<head>` in all HTML files:

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
```

4. Update in `assets/css/main.css`:

```css
body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
}
```

## 📱 Update Logo (5 minutes)

### Text Logo (Current)
In navigation, change "BizPro" to your company name.

### Image Logo
Replace text with image:

```html
<a href="index.html" class="logo">
    <img src="assets/images/logo.png" alt="Your Company" style="height: 40px;">
</a>
```

## 📄 Customize Pages

### Home Page
- Update hero title and subtitle
- Change feature icons and descriptions
- Update service offerings
- Replace testimonials with real ones

### Portfolio Page
- Add your projects
- Update project images and descriptions
- Modify filter categories

### Blog Page
- Add your blog posts
- Update dates and categories
- Change author information

### About Page
- Write your company story
- Add team members
- Update timeline with your milestones

### Contact Page
- Update contact information
- Modify form fields if needed
- Add Google Maps embed (see below)

## 🗺️ Add Google Maps (5 minutes)

1. Go to [Google Maps](https://www.google.com/maps)
2. Search for your location
3. Click "Share" → "Embed a map"
4. Copy the iframe code
5. Replace the map placeholder in `contact.html`:

```html
<div class="map-placeholder">
    <iframe 
        src="YOUR_GOOGLE_MAPS_EMBED_URL" 
        width="100%" 
        height="400" 
        style="border:0; border-radius: 12px;" 
        allowfullscreen="" 
        loading="lazy">
    </iframe>
</div>
```

## 📊 Add Google Analytics (5 minutes)

1. Create account at [Google Analytics](https://analytics.google.com)
2. Get your Measurement ID (looks like `G-XXXXXXXXXX`)
3. Add before `</head>` in all HTML files:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## 📧 Connect Contact Form (10 minutes)

### Option 1: Formspree (Easiest)

1. Sign up at [Formspree.io](https://formspree.io)
2. Create a new form
3. Update form in `contact.html`:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Option 2: Netlify Forms

If deploying to Netlify, just add:

```html
<form name="contact" method="POST" data-netlify="true">
```

## 🎯 SEO Optimization (15 minutes)

### 1. Update Meta Tags in Each Page

```html
<title>Your Page Title - Your Company</title>
<meta name="description" content="Your page description (150-160 characters)">
```

### 2. Update Open Graph Tags

```html
<meta property="og:title" content="Your Page Title">
<meta property="og:description" content="Your description">
<meta property="og:image" content="https://yoursite.com/og-image.jpg">
<meta property="og:url" content="https://yoursite.com">
```

### 3. Update Sitemap

Edit `sitemap.xml` and replace `yourwebsite.com` with your domain.

### 4. Update Robots.txt

Edit `robots.txt` and update the sitemap URL.

## 🌙 Customize Dark Mode (Optional)

Edit `assets/css/theme.css` to change dark mode colors:

```css
[data-theme="dark"] {
    --primary-color: #3b82f6;
    --bg-color: #111827;
    /* ... customize other colors */
}
```

## ✅ Pre-Launch Checklist

- [ ] Updated all company information
- [ ] Replaced all placeholder images
- [ ] Updated contact information
- [ ] Connected contact form
- [ ] Added Google Analytics
- [ ] Updated meta tags for SEO
- [ ] Updated sitemap.xml
- [ ] Tested on mobile devices
- [ ] Tested in different browsers
- [ ] Checked all links work
- [ ] Optimized images for web
- [ ] Added favicon
- [ ] Tested contact form
- [ ] Proofread all content

## 🚀 Ready to Launch?

See `DOCUMENTATION.md` for deployment instructions to:
- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages

## 💡 Tips

1. **Start Small:** Customize one section at a time
2. **Test Often:** Check your changes in the browser frequently
3. **Backup:** Keep a copy of the original template
4. **Mobile First:** Always test on mobile devices
5. **Performance:** Optimize images before uploading

## 🆘 Need Help?

- Check `DOCUMENTATION.md` for detailed guides
- Review `README.md` for quick reference
- Contact: support@bizpro.com

---

**Estimated Total Time:** 1-2 hours for basic customization
