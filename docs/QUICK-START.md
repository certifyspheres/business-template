# 🚀 Quick Start Guide - BizPro Template

Get your website up and running in 15 minutes!

## Step 1: Download & Extract (1 minute)

1. Download the template
2. Extract to a folder on your computer
3. Open the folder in your code editor (VS Code recommended)

## Step 2: Preview Locally (2 minutes)

**Option A: Double-click**
- Simply open `index.html` in your browser

**Option B: Use Live Server (Recommended)**
- Install "Live Server" extension in VS Code
- Right-click `index.html` → "Open with Live Server"

## Step 3: Customize Colors (3 minutes)

1. Open `assets/css/main.css`
2. Find the `:root` section (line 8)
3. Change these two colors:

```css
:root {
    --primary-color: #2563eb;    /* Change to your brand color */
    --secondary-color: #7c3aed;  /* Change to your accent color */
}
```

**Need color ideas?** Visit [coolors.co](https://coolors.co)

## Step 4: Update Content (5 minutes)

### Company Name
- Search for "BizPro" in all files
- Replace with your company name

### Contact Info (in footer of each HTML file)
```html
<li>📧 info@bizpro.com</li>          <!-- Your email -->
<li>📞 +1 (555) 123-4567</li>        <!-- Your phone -->
<li>📍 123 Business St, Suite 100</li> <!-- Your address -->
```

### Hero Section (index.html)
```html
<h1 class="hero-title">Your Headline Here</h1>
<p class="hero-subtitle">Your subtitle here</p>
```

## Step 5: Add Your Images (4 minutes)

1. Place your images in `assets/images/` folder
2. Replace placeholders:

```html
<!-- Before -->
<div class="hero-placeholder"></div>

<!-- After -->
<div class="hero-placeholder" 
     style="background-image: url('assets/images/hero.jpg'); 
            background-size: cover; 
            background-position: center;">
</div>
```

**Image sizes:**
- Hero: 1920x1080px
- Portfolio: 800x600px
- Blog: 1200x630px

**Free images:** [unsplash.com](https://unsplash.com), [pexels.com](https://pexels.com)

## Step 6: Deploy (5 minutes)

### Easiest: Netlify Drag & Drop

1. Go to [netlify.com](https://netlify.com)
2. Sign up (free)
3. Drag your entire folder to the deploy zone
4. Done! Your site is live

### Alternative: GitHub Pages

1. Create GitHub account
2. Create new repository
3. Upload your files
4. Settings → Pages → Enable
5. Your site: `username.github.io/repo-name`

---

## ✅ You're Done!

Your website is now live. Here's what to do next:

### Immediate Next Steps
- [ ] Test on mobile device
- [ ] Share with friends for feedback
- [ ] Add Google Analytics (see CUSTOMIZATION-GUIDE.md)
- [ ] Submit to Google Search Console

### When You Have More Time
- [ ] Add real testimonials
- [ ] Write blog posts
- [ ] Add portfolio projects
- [ ] Connect contact form to email
- [ ] Optimize images
- [ ] Add custom domain

---

## 📚 Need More Help?

- **Detailed customization:** See `CUSTOMIZATION-GUIDE.md`
- **Full documentation:** See `DOCUMENTATION.md`
- **Deployment options:** See `DEPLOYMENT.md`
- **All features:** See `FEATURES.md`

---

## 🆘 Common Issues

### Images not showing?
- Check file paths: `assets/images/photo.jpg`
- Make sure images are in the correct folder

### Colors not changing?
- Clear browser cache (Ctrl+Shift+R or Cmd+Shift+R)
- Make sure you edited `assets/css/main.css`

### Mobile menu not working?
- Make sure `assets/js/main.js` is loaded
- Check browser console for errors

### Form not submitting?
- See CUSTOMIZATION-GUIDE.md for form setup
- Need backend service like Formspree

---

## 💡 Pro Tips

1. **Start simple** - Don't try to customize everything at once
2. **Test often** - Check your changes in the browser frequently
3. **Mobile first** - Always test on mobile devices
4. **Optimize images** - Use [tinypng.com](https://tinypng.com) before uploading
5. **Backup** - Keep a copy of the original template

---

## 🎯 Customization Priority

Do these in order for best results:

1. ✅ Colors (3 min)
2. ✅ Company name (2 min)
3. ✅ Contact info (2 min)
4. ✅ Hero section (3 min)
5. ✅ Images (5 min)
6. ✅ About page (10 min)
7. ✅ Services (10 min)
8. ✅ Portfolio (15 min)
9. ✅ Blog posts (20 min)
10. ✅ Forms & integrations (15 min)

**Total time for full customization:** 2-3 hours

---

## 🚀 Launch Checklist

Before going live, make sure:

- [ ] All "BizPro" references updated
- [ ] Contact information correct
- [ ] All links work
- [ ] Images optimized and loaded
- [ ] Tested on mobile
- [ ] Tested in Chrome, Firefox, Safari
- [ ] Meta tags updated (title, description)
- [ ] Google Analytics added
- [ ] Contact form connected
- [ ] Favicon added
- [ ] 404 page works
- [ ] Sitemap updated with your domain

---

## 📞 Support

Need help? We're here for you!

- **Email:** support@bizpro.com
- **Response time:** Within 24 hours
- **Documentation:** Check the included guides

---

**Congratulations!** 🎉

You now have a professional business website. Share it with the world!

---

**Last Updated:** December 6, 2024
