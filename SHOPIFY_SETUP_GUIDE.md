# 🎵 THE GALLERY - Shopify Theme Setup Guide

## Overview
This is a custom Shopify theme for a clothing and accessories store featuring:
- ⚡ Neon red and powder blue cracked lightning effects
- 💨 Light fog effect activated by clicking products
- 🎵 Integrated music player for MP3 uploads
- 🎨 Paisley-framed product collage with gold engraving
- ☁️ Spinning animated clouds with color pulse
- 🌈 Elegant Old English typography

---

## Prerequisites
- Shopify store account (any plan)
- Access to Shopify Admin Dashboard
- Basic knowledge of Shopify theme structure

---

## Installation Steps

### Step 1: Upload Theme to Shopify

1. Go to **Shopify Admin** → **Sales channels** → **Online Store** → **Themes**
2. Click **"Add an unpublished theme"**
3. Choose **"Upload ZIP file"**
4. Create a folder structure and zip the following files:
   ```
   shopify-theme/
   └── layout/
       └── theme.liquid
   ```

### Step 2: Add the Liquid Template

1. Copy the content from `shopify-theme-template.liquid`
2. In Shopify Admin, go to **Online Store** → **Themes**
3. Click on your theme → **"Edit code"**
4. In the **Layout** section, find `theme.liquid`
5. Replace the content with our template
6. Click **"Save"**

### Step 3: Create Required Collections

The theme expects two collections:

1. **Clothing Collection**
   - Go to **Products** → **Collections**
   - Click **"Create collection"**
   - Name: `Clothing`
   - Handle: `clothing`
   - Add your clothing products
   - Click **"Save"**

2. **Accessories Collection**
   - Click **"Create collection"**
   - Name: `Accessories`
   - Handle: `accessories`
   - Add your accessory products
   - Click **"Save"**

### Step 4: Publish Your Theme

1. Go to **Online Store** → **Themes**
2. Find your theme in the list
3. Click the **"..."** menu
4. Select **"Publish"**
5. Your store is now live! 🎉

---

## Features & Usage

### 🎵 Music Player
- **Upload MP3s**: Click "Choose File" in the music player
- **Support formats**: MP3, WAV, M4A
- **Multiple uploads**: Select multiple files at once
- **Playlist management**: Click to play any track, click ✕ to delete
- **Controls**: Play, Pause, Stop buttons
- **Volume slider**: Adjust from 0-100%
- **Progress bar**: Click to seek through track
- **Auto-advance**: Next track plays automatically when current ends
- **Minimize**: Click "−" to minimize player for better browsing

### 💨 Fog Effect
- **Activation**: Click on any product card
- **Duration**: Fog appears for 3 seconds then fades
- **Effect**: Light white fog with floating particles

### ⚡ Lightning Effects
- **Automatic**: Runs continuously in background
- **Neon colors**: Red and blue gradient
- **Random placement**: Bolts appear randomly across screen

### ☁️ Spinning Clouds
- **Location**: Below "THE GALLERY" header
- **Color pulse**: Alternates between red and sky blue
- **Animation**: Continuous floating motion

### 🎨 Product Display
- **Paisley frames**: Cream background with gold patterns
- **Gold border**: Double border with engraving effect
- **Hover effect**: Slight zoom on hover
- **Price display**: Automatically pulls from Shopify products
- **Product images**: Auto-resizes to 300x300px

---

## Customization Guide

### Change Colors

**Lightning color** (line ~35):
```liquid
background: linear-gradient(to bottom, #ff0080, #00d9ff);
/* Change #ff0080 to your neon red, #00d9ff to your powder blue */
```

**Frame color** (line ~230):
```liquid
background: rgba(245, 245, 220, 0.95);
/* Change to your preferred cream shade */
```

**Gold accents** (line ~237):
```liquid
border: 3px double #d4af37;
/* Change #d4af37 to your preferred gold */
```

### Adjust Product Grid

**Change number of columns** (line ~310):
```liquid
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
/* Change 250px to adjust column width */
```

**Change products shown per collection** (line ~360):
```liquid
{% for product in collections.clothing.products limit: 6 %}
/* Change limit: 6 to show more/fewer products */
```

### Modify Music Player Size

**Width adjustment** (line ~115):
```css
width: 350px;
/* Change 350px to desired width */
```

---

## Troubleshooting

### Products Not Showing
- ✓ Verify collections are named `clothing` and `accessories` (exact spelling)
- ✓ Make sure you've added products to each collection
- ✓ Products must be published in Shopify

### Music Player Not Working
- ✓ Supported formats: MP3, WAV, M4A
- ✓ Check browser console for errors (F12 → Console)
- ✓ Ensure files are under 50MB each
- ✓ Browser must allow local file access

### Fog Effect Not Showing
- ✓ Click directly on product cards
- ✓ Check browser compatibility (works in all modern browsers)
- ✓ Verify z-index isn't conflicting with other elements

### Lightning Not Appearing
- ✓ The effect should be continuous
- ✓ If missing, check if JavaScript is enabled
- ✓ Clear browser cache and refresh

---

## Mobile Optimization

The theme is fully responsive and includes:
- ✓ Mobile-friendly music player
- ✓ Responsive product grid
- ✓ Touch-friendly buttons
- ✓ Optimized for screens 320px and above

---

## Performance Tips

1. **Image optimization**: Compress product images before uploading
2. **Music files**: Keep MP3s under 10MB for fast loading
3. **Browser cache**: Clear cache if experiencing issues
4. **CDN**: Shopify automatically serves images via CDN

---

## Advanced: Custom CSS

To add custom styles:

1. Go to **Online Store** → **Themes** → **Edit code**
2. Create a new CSS file: `assets/custom-styles.css`
3. Add your CSS
4. Link it in the `<head>` section of `theme.liquid`:
   ```liquid
   {{ 'custom-styles.css' | asset_url | stylesheet_tag }}
   ```

---

## Advanced: Spotify Integration (Future)

To integrate Spotify in the future:

1. Create a Spotify Developer account
2. Generate API credentials
3. Replace the music player section with Spotify Web API
4. Implement OAuth for user authentication

*This is a placeholder for future implementation*

---

## File Structure

Your repository should contain:
```
shopify-clothing-accessories/
├── README.md (this file)
├── index.html (original version)
├── joke-generator.html
└── shopify-theme-template.liquid
```

---

## Support & Resources

- **Shopify Theme Guide**: https://shopify.dev/themes
- **Liquid Language**: https://shopify.dev/api/liquid
- **Shopify Forums**: https://community.shopify.com/

---

## License & Credits

**THE GALLERY Theme** - Custom Design
- Created for 860Dom
- All features included: Lightning, Fog, Music Player, Paisley Frames
- Responsive and mobile-optimized

---

## Next Steps

1. ✅ Install theme in Shopify
2. ✅ Create Clothing & Accessories collections
3. ✅ Add your products with images
4. ✅ Publish theme
5. ✅ Upload MP3 files to music player
6. 🎉 Enjoy your new store!

---

**Questions?** Check the troubleshooting section or refer to official Shopify documentation.
