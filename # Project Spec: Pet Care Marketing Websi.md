# Project Spec: Pet Care Marketing Website

## Objective
- Build a high-converting, static marketing site for a local pet-care business (walking, sitting, boarding, grooming).
- Make it **trivially re-themeable** – client picks from 35+ DaisyUI themes or customizes colors in one file.
- Deploy instantly to GitHub Pages + Netlify via CDN (zero build step).
- Primary build on netlify to which domain would be configured, however, github pages should also be configured
- Professional, warm, trustworthy design that converts visitors to bookings.

## Tech Stack
```
HTML5 + Tailwind CSS + DaisyUI (CDN – NO BUILD REQUIRED)
<script src="https://cdn.tailwindcss.com"></script>
<script src="https://cdn.jsdelivr.net/npm/daisyui@4.12.10/dist/full.min.js"></script>
```
- Vanilla JS only for interactions (mobile nav toggle, FAQ expand/collapse)
- Theme switching: `<html data-theme="emerald|cupcake|your-custom">`
- 100% static – push to GitHub Pages

## Commands
```
# Local preview
npx serve .                    # or python -m http.server 4173
open http://localhost:4173

# Deploy
git add . && git commit -m "Update site" && git push origin main
# GitHub Pages auto-deploys from main branch
# Netlify: drag folder to app.netlify.com/drop
```

## Project Structure
```
├── index.html          # Home (main landing)
├── about.html          # Team, story, credentials  
├── services.html       # Detailed pricing/services
├── contact.html        # Form + contact info
├── assets/
│   ├── images/         # Logo, pet photos, team photos
│   └── icons/          # SVG icons (optional)
├── styles/
│   └── custom.css      # Theme overrides (if client wants custom colors)
├── scripts/
│   └── main.js         # Mobile nav, FAQ accordion
└── README.md           # Theme switching + deploy instructions
```

## Design System (DaisyUI)
**Core DaisyUI components you'll use:**
```
Navbar:     navbar bg-base-100
Hero:       hero min-h-screen bg-gradient-to-r
Cards:      card bg-base-200 shadow-xl
Buttons:    btn btn-primary btn-lg
Testimonial:card bg-base-200 p-6
FAQ:        collapse collapse-arrow border border-base-300
Form:       form-control input textarea btn
```

**Theme switching (client picks one line):**
```html
<!-- Swap any of these in <html> tag -->
<html data-theme="emerald">     <!-- Pet-friendly green -->
<html data-theme="cupcake">     <!-- Warm pastels -->
```

**Custom theme override (in `styles/custom.css`):**
```css
@layer components {
  .btn-primary { @apply bg-[#your-pet-pink] hover:bg-[#darker-pink]; }
  .hero { @apply bg-gradient-to-r from-[#pet-blue] to-[#pet-green]; }
}
```

## Page Requirements

### Home (`index.html`)
```
1. Sticky navbar: logo + links (Home, Services, About, Testimonials, FAQ, Contact)
2. Hero: 
   - H1: "Loving Pet Care You Can Trust"
   - Sub: "Daily walks • Overnight stays • Grooming • [City Name]"
   - Buttons: "Book Meet & Greet" + "View Services"
   - Large pet photo + trust badges
3. Services: 4-6 cards (Dog Walking, Drop-ins, Overnight, Grooming)
4. Why Us: 4 feature cards (Insured, GPS walks, Photo updates, Vet-trained)
5. Testimonials: 4 rotating cards (name + pet + quote + stars)
6. Service Area: Map + neighborhood list
7. FAQ: 6 collapsible questions
8. Final CTA: "Ready to meet your sitter?"
9. Footer: Contact + social icons
```

### About (`about.html`)
```
- Reuse navbar/footer
- "Our Story" section (300 words)
- Credentials (years, certs, memberships)
- Team: 3-4 member cards (photo, name, bio, pet preference)
```

### Services (`services.html`)
```
- Detailed service breakdown
- Pricing table or "From $X/hour" cards
- What's included lists
- Add-on options
```

### Contact (`contact.html`)
```
- Phone (tel:), email (mailto:), hours
- Static map image placeholder
- Netlify Forms-ready contact form:
  <form name="contact" data-netlify="true" data-netlify-honeypot="bot-field">
    Name, Email, Phone, Pet Type, Services, Message
  </form>
```

## Boundaries & Practices
```
✅ ALWAYS:
- Use DaisyUI semantic classes (btn, card, hero, etc.)
- Mobile-first responsive (DaisyUI handles 90%)
- Semantic HTML5 (header, nav, main, section, footer)
- <html data-theme="emerald"> for theme control

⚠️ ASK FIRST:
- Adding external JS libraries
- Major layout changes
- Custom color requests (use theme first)

🚫 NEVER:
- NPM dependencies or build steps
- Hard-coded colors (use DaisyUI theme system)
- Backend/database code
- Non-semantic div soup
```


## Deployment Instructions (in README.md)
```
## 🚀 Quick Deploy

### GitHub Pages (FREE)
1. Push to `main` branch
2. Settings → Pages → Source: Deploy from branch → main
3. Site: https://username.github.io/repo-name

### Netlify (FREE + Custom Domain)
1. Drag this folder to https://app.netlify.com/drop
2. OR connect GitHub repo
3. Domain Settings → Add custom domain
4. DNS: CNAME → your-netlify-site.netlify.app

## 🎨 Change Theme (30 seconds)
<html data-theme="cupcake">  ← Swap "emerald" for any of:
- emerald, cupcake, pastel, light, dark, synthwave, retro, cyberpunk...
Full list: https://daisyui.com/docs/themes/
```

## Instructions for Copilot
```
1. Generate ALL files per exact structure above
2. Use ONLY DaisyUI components (no raw Tailwind utilities where DaisyUI has semantic classes)
3. Put `<html data-theme="emerald">` with theme switcher comments
4. Make FAQ accordion + mobile nav work with vanilla JS
5. Contact form Netlify-ready (name attributes + data-netlify="true")
6. Responsive navbar collapses to hamburger on mobile
7. Use placeholder content I can easily replace
8. Output each file in ```html filename.ext ``` blocks
9. Include full README.md with deploy + theme instructions

Start with file tree, then generate files one by one.
```

