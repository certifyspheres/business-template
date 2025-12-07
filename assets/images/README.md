# Images Folder

Place your images in this folder.

## Recommended Image Sizes

### Hero/Banner Images
- **Size:** 1920x1080px
- **Format:** JPG or WebP
- **Max file size:** 200KB (optimized)

### Portfolio/Project Images
- **Size:** 800x600px or 1200x800px
- **Format:** JPG or WebP
- **Max file size:** 150KB

### Blog Featured Images
- **Size:** 1200x630px (optimal for social sharing)
- **Format:** JPG or WebP
- **Max file size:** 150KB

### Team Photos
- **Size:** 500x500px (square)
- **Format:** JPG or PNG
- **Max file size:** 100KB

### Logo
- **Size:** Variable (maintain aspect ratio)
- **Format:** PNG or SVG (SVG preferred for scalability)
- **Background:** Transparent

### Favicon
- **Size:** 512x512px
- **Format:** PNG
- Use [favicon.io](https://favicon.io) to generate all required sizes

## Image Optimization Tools

- [TinyPNG](https://tinypng.com) - Compress PNG and JPG
- [Squoosh](https://squoosh.app) - Advanced image optimization
- [ImageOptim](https://imageoptim.com) - Mac app for optimization
- [JPEG Optimizer](http://jpeg-optimizer.com) - Online JPEG compression

## Free Stock Photo Resources

- [Unsplash](https://unsplash.com) - High-quality free photos
- [Pexels](https://pexels.com) - Free stock photos and videos
- [Pixabay](https://pixabay.com) - Free images and videos
- [Burst by Shopify](https://burst.shopify.com) - Free business photos

## Usage in HTML

### Background Image
```html
<div style="background-image: url('assets/images/hero.jpg'); background-size: cover; background-position: center;"></div>
```

### Image Tag
```html
<img src="assets/images/photo.jpg" alt="Description" loading="lazy">
```

### CSS Background
```css
.hero {
    background-image: url('../images/hero.jpg');
    background-size: cover;
    background-position: center;
}
```

## Tips

1. **Always optimize images** before uploading to reduce file size
2. **Use descriptive filenames:** `team-photo-john-smith.jpg` not `IMG_1234.jpg`
3. **Add alt text** for accessibility and SEO
4. **Use lazy loading** for images below the fold
5. **Consider WebP format** for better compression (with JPG fallback)
6. **Maintain aspect ratios** to avoid distortion
7. **Use CDN** for large sites with many images

## Current Placeholders

The template currently uses CSS gradients as placeholders. Replace these with your actual images by:

1. Adding your image files to this folder
2. Updating the HTML/CSS to reference your images
3. Removing or modifying the placeholder gradient backgrounds
