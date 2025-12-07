# Header & Footer Includes Guide

## Overview

This template now supports reusable header and footer components using JavaScript includes. This makes it easier to maintain consistent navigation and footer across all pages.

## 📁 File Structure

```
project/
├── includes/
│   ├── header.html          # Reusable header component
│   └── footer.html          # Reusable footer component
├── assets/
│   └── js/
│       ├── includes.js      # Script to load includes
│       └── main.js          # Main functionality
├── template.html            # Template showing how to use includes
└── [all other HTML pages]
```

## 🚀 How to Use Includes

### Method 1: Using Includes (Recommended for New Pages)

1. **Create a new HTML page** using `template.html` as a starting point

2. **Add placeholder divs** where you want header and footer:
```html
<body>
    <!-- Header Include -->
    <div id="header-placeholder"></div>

    <!-- Your content here -->
    <main>
        <!-- Page content -->
    </main>

    <!-- Footer Include -->
    <div id="footer-placeholder"></div>

    <!-- Load includes first, then main.js -->
    <script src="assets/js/includes.js"></script>
    <script src="assets/js/main.js"></script>
</body>
```

3. **That's it!** The header and footer will be automatically loaded.

### Method 2: Direct HTML (Current Pages)

Existing pages still use direct HTML for header and footer. This works fine but requires updating each page individually when making changes.

## ✨ Benefits of Using Includes

### Advantages:
- ✅ **Single Source of Truth** - Update header/footer in one place
- ✅ **Consistency** - All pages automatically have the same header/footer
- ✅ **Easy Maintenance** - Change navigation once, applies everywhere
- ✅ **Faster Development** - Copy template.html for new pages
- ✅ **Automatic Active Links** - Current page is automatically highlighted

### Considerations:
- ⚠️ Requires JavaScript enabled
- ⚠️ Needs a web server (won't work with file:// protocol)
- ⚠️ Slight delay in loading (usually imperceptible)

## 🔧 Customizing Includes

### To Update Header:

Edit `includes/header.html`:
```html
<!-- Change logo -->
<span class="logo-text">Your Company</span>

<!-- Add/remove navigation items -->
<li><a href="new-page.html" class="nav-link">New Page</a></li>
```

### To Update Footer:

Edit `includes/footer.html`:
```html
<!-- Update company info -->
<h3>Your Company</h3>
<p>Your company description</p>

<!-- Update contact info -->
<li>📧 your-email@company.com</li>
```

## 📝 Converting Existing Pages

To convert an existing page to use includes:

### Step 1: Replace Header
```html
<!-- OLD -->
<header class="header" id="header">
    <!-- Full header HTML -->
</header>

<!-- NEW -->
<div id="header-placeholder"></div>
```

### Step 2: Replace Footer
```html
<!-- OLD -->
<footer class="footer">
    <!-- Full footer HTML -->
</footer>

<!-- NEW -->
<div id="footer-placeholder"></div>
```

### Step 3: Update Scripts
```html
<!-- Add includes.js BEFORE main.js -->
<script src="assets/js/includes.js"></script>
<script src="assets/js/main.js"></script>
```

## 🎯 Active Navigation Link

The includes system automatically highlights the current page in navigation:

```javascript
// Automatically sets .active class on current page link
// No manual configuration needed!
```

## 🌐 Server Requirements

### Development:
Use any local server:
```bash
# Python
python -m http.server 8000

# Node.js
npx serve

# VS Code
Use Live Server extension
```

### Production:
Works on all standard web servers:
- Apache
- Nginx
- GitHub Pages
- Netlify
- Vercel
- Any static hosting

## 🐛 Troubleshooting

### Header/Footer Not Loading?

1. **Check browser console** for errors
2. **Verify file paths** - includes/ folder must be in root
3. **Use a web server** - file:// protocol won't work
4. **Check includes.js** is loaded before main.js

### Active Link Not Working?

The script automatically detects the current page. If it's not working:
- Check that nav links have class `nav-link`
- Verify the href matches the filename exactly

### Styling Issues?

Make sure CSS is loaded before the includes:
```html
<link rel="stylesheet" href="assets/css/main.css">
<link rel="stylesheet" href="assets/css/theme.css">
```

## 📊 Comparison

| Feature | Direct HTML | Includes |
|---------|-------------|----------|
| Maintenance | Update each file | Update once |
| Consistency | Manual sync | Automatic |
| Page Load | Instant | ~50ms delay |
| JavaScript | Not required | Required |
| File Protocol | Works | Doesn't work |
| Best For | Simple sites | Multi-page sites |

## 🎨 Customization Examples

### Example 1: Add New Navigation Item

Edit `includes/header.html`:
```html
<ul class="nav-menu" id="navMenu">
    <li><a href="index.html" class="nav-link">Home</a></li>
    <li><a href="services.html" class="nav-link">Services</a></li> <!-- NEW -->
    <li><a href="portfolio.html" class="nav-link">Portfolio</a></li>
    <!-- ... -->
</ul>
```

### Example 2: Update Footer Copyright

Edit `includes/footer.html`:
```html
<p>&copy; <span id="currentYear"></span> Your Company. All rights reserved.</p>
```

### Example 3: Change Social Links

Edit `includes/footer.html`:
```html
<div class="social-links">
    <a href="https://facebook.com/yourpage" aria-label="Facebook">📘</a>
    <a href="https://twitter.com/yourhandle" aria-label="Twitter">🐦</a>
    <!-- Add more or update URLs -->
</div>
```

## 🚀 Quick Start for New Pages

1. Copy `template.html`
2. Rename it (e.g., `services.html`)
3. Update the `<title>` and meta tags
4. Add your content in the `<main>` section
5. Done! Header and footer are automatic

## 📝 Notes

- **Current Year**: Automatically updated in footer
- **Active Links**: Automatically highlighted
- **Theme Switcher**: Works automatically
- **Mobile Menu**: Works automatically
- **All JavaScript**: Initialized automatically

## 🔄 Migration Strategy

### Option 1: Gradual Migration
- Keep existing pages as-is
- Use includes for new pages only
- Migrate old pages when updating them

### Option 2: Full Migration
- Convert all pages at once
- More consistent
- Easier long-term maintenance

### Recommended: Option 1
Start with new pages, migrate existing pages gradually.

## 💡 Best Practices

1. **Always use includes for new pages**
2. **Test on a local server** during development
3. **Keep includes simple** - just header and footer
4. **Update includes** when changing navigation
5. **Check all pages** after updating includes

## 📞 Support

For questions about includes:
- Check this guide
- Review `template.html` for example
- Check browser console for errors
- Contact: support@certifysphere.com

---

**Created by:** [CertifySphere](https://certifysphere.com/)  
**Version:** 1.2.0  
**Date:** December 6, 2024
