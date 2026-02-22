# 🐾 Arlo's Pet Care Website

A modern, high-converting static marketing website for pet care services. Built with **zero build steps** using HTML5, Tailwind CSS, and DaisyUI.

## ✨ Features

- 🎨 **Trivially Re-themeable** - Change themes in seconds with 35+ DaisyUI options
- 📱 **Fully Responsive** - Mobile-first design that looks great on all devices
- ⚡ **Zero Build Required** - Pure HTML/CSS/JS with CDN dependencies
- 🚀 **Deploy Instantly** - Push to GitHub Pages or drag-and-drop to Netlify
- 📧 **Netlify Forms Ready** - Contact form pre-configured for Netlify
- ♿ **Accessible** - Semantic HTML5 and WCAG compliant
- 🎯 **SEO Optimized** - Meta tags and semantic structure

## 📁 Project Structure

```
arlospetcare/
├── index.html          # Home page (hero, services, testimonials, FAQ)
├── about.html          # About page (team, story, credentials)
├── services.html       # Services page (detailed pricing & offerings)
├── contact.html        # Contact page (form + contact info)
├── assets/
│   ├── images/         # Logo, photos, team pictures (use your own)
│   └── icons/          # SVG icons (optional)
├── styles/
│   └── custom.css      # Custom theme overrides
├── scripts/
│   └── main.js         # Mobile nav, FAQ accordion, interactions
└── README.md           # This file
```

## 🚀 Quick Start

### Local Development

1. **Clone the repository:**
   ```bash
   git clone https://github.com/rkrules/arlospetcare.git
   cd arlospetcare
   ```

2. **Serve locally** (choose one):
   ```bash
   # Option 1: Using npx (Node.js required)
   npx serve .
   
   # Option 2: Using Python
   python -m http.server 4173
   
   # Option 3: Using PHP
   php -S localhost:4173
   ```

3. **Open in browser:**
   ```
   http://localhost:4173
   ```

## 🎨 Change Theme (30 seconds!)

### Quick Theme Switch

Open any HTML file and change the `data-theme` attribute in the `<html>` tag:

```html
<!-- Change from emerald to any theme below -->
<html lang="en" data-theme="emerald">
```

### Available DaisyUI Themes

**Light Themes:**
- `light` - Clean, minimal default
- `emerald` - Fresh green (current)
- `cupcake` - Warm pastels
- `pastel` - Soft colors
- `valentine` - Pink & romantic
- `garden` - Nature-inspired
- `lofi` - Low contrast, calm
- `cmyk` - Print-inspired
- `autumn` - Warm oranges
- `acid` - Lime green
- `lemonade` - Yellow & fresh
- `winter` - Cool blues

**Dark Themes:**
- `dark` - Standard dark mode
- `synthwave` - Retro 80s
- `retro` - Vintage
- `cyberpunk` - Neon futuristic
- `halloween` - Orange & purple
- `forest` - Deep greens
- `aqua` - Underwater blues
- `black` - Pure black
- `luxury` - Gold accents
- `dracula` - Purple dark
- `business` - Professional dark
- `night` - Deep navy

**Full theme list:** https://daisyui.com/docs/themes/

### Custom Color Override

To use custom brand colors, edit `styles/custom.css`:

```css
@layer components {
  /* Your custom primary color */
  .btn-primary { 
    @apply bg-[#your-color] hover:bg-[#darker-shade]; 
  }
  
  /* Custom gradient */
  .hero { 
    @apply bg-gradient-to-r from-[#color1] to-[#color2]; 
  }
}
```

## 🚀 Deployment

### GitHub Pages (FREE)

1. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Source: Deploy from branch → `main`
   - Save

2. **Your site will be live at:**
   ```
   https://rkrules.github.io/arlospetcare
   ```

3. **Custom domain (optional):**
   - Add `CNAME` file with your domain
   - Configure DNS: `CNAME` → `rkrules.github.io`

### Netlify (FREE + Custom Domain)

**Method 1: Drag & Drop**
1. Go to https://app.netlify.com/drop
2. Drag entire project folder
3. Done! Site live in seconds

**Method 2: GitHub Integration**
1. Go to https://app.netlify.com
2. New site from Git → Choose repository
3. Build settings: Leave empty (no build needed!)
4. Deploy

**Enable Netlify Forms:**
- Forms automatically work once deployed to Netlify
- View submissions: Netlify Dashboard → Forms

**Custom Domain:**
1. Netlify Dashboard → Domain Settings
2. Add custom domain
3. Configure DNS as instructed

### Other Hosting Options

- **Vercel:** Connect GitHub repo, zero config needed
- **Cloudflare Pages:** Push to Git, instant deploy
- **AWS S3 + CloudFront:** Static site hosting
- **Firebase Hosting:** `firebase deploy`

## 📝 Customization Guide

### Replace Placeholder Content

1. **Images:**
   - Replace Unsplash/placeholder images with your own
   - Add to `assets/images/`
   - Update `src` attributes in HTML

2. **Contact Information:**
   - Search for `(555) 123-4567` and replace
   - Search for `hello@arlospetcare.com` and replace
   - Update `123 Pet Lane, Metro City` with real address

3. **Business Details:**
   - Update service area neighborhoods
   - Modify pricing in `services.html`
   - Update team bios in `about.html`
   - Change "since 2018" to your founding year

4. **Social Media:**
   - Update social links in footer
   - Replace with actual Facebook, Instagram, Twitter URLs

### Add/Remove Services

Edit `services.html` and `index.html` service cards:

```html
<div class="card bg-base-100 shadow-xl">
  <figure class="px-10 pt-10">
    <i class="fas fa-your-icon text-6xl text-primary"></i>
  </figure>
  <div class="card-body items-center text-center">
    <h3 class="card-title">Your Service Name</h3>
    <p>Description of your service...</p>
    <div class="card-actions">
      <a href="services.html#your-service" class="btn btn-primary btn-sm">Learn More</a>
    </div>
  </div>
</div>
```

### Modify FAQ

Edit FAQ section in `index.html`:

```html
<div class="collapse collapse-arrow bg-base-100 border border-base-300">
  <input type="checkbox" class="faq-toggle" />
  <div class="collapse-title text-xl font-medium">
    Your Question Here?
  </div>
  <div class="collapse-content">
    <p>Your answer here...</p>
  </div>
</div>
```

## 🛠️ Tech Stack

- **HTML5** - Semantic markup
- **Tailwind CSS v3** - Utility-first CSS framework (CDN)
- **DaisyUI v4.12** - Component library (CDN)
- **Font Awesome 6** - Icons (CDN)
- **Vanilla JavaScript** - No frameworks, pure JS

**No build tools, no npm, no webpack!** Everything runs directly in the browser.

## 🎯 Best Practices

### ✅ DO:
- Use DaisyUI semantic classes (`btn`, `card`, `hero`, etc.)
- Change theme via `data-theme` attribute
- Keep mobile-first responsive design
- Use semantic HTML5 elements
- Test all pages on mobile devices

### ⚠️ AVOID:
- Hard-coded colors (use DaisyUI theme variables)
- Inline styles (use Tailwind classes)
- jQuery or other heavy libraries
- Build tools unless absolutely necessary

## 📱 Browser Support

- ✅ Chrome/Edge (last 2 versions)
- ✅ Firefox (last 2 versions)
- ✅ Safari (last 2 versions)
- ✅ Mobile Safari (iOS 12+)
- ✅ Chrome Mobile (Android 8+)

## 🤝 Contributing

Feel free to fork this project and customize it for your pet care business!

## 📄 License

This project is open source and available for personal and commercial use.

## 🐕 Credits

Built with love for pets and their humans by the Arlo's Pet Care team.

---

**Questions?** Contact us at hello@arlospetcare.com or call (555) 123-4567

🐾 Made with ❤️ for furry friends everywhere
