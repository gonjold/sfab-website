# South FL Auto Brokers Website

Luxury recruitment website for South FL Auto Brokers — the exclusive broker partnership program for Toyota of Coconut Creek.

## Tech Stack

- **HTML5** - Semantic markup
- **CSS3** - Mobile-first, custom properties, modern features
- **Vanilla JavaScript** - No frameworks, minimal footprint
- **Hosting** - Netlify (free tier)
- **Forms** - Netlify Forms
- **Images** - Cloudinary CDN

## Project Structure

```
sfab-website/
├── index.html          # Main single-page site
├── css/
│   └── styles.css      # All styles (mobile-first)
├── js/
│   └── main.js         # Animations, form handling
├── images/             # Local image fallbacks
└── README.md           # This file
```

## Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/gonjold/sfab-website.git
   cd sfab-website
   ```

2. Start a local server (choose one):
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Node.js (if http-server is installed)
   npx http-server
   
   # VS Code Live Server extension
   # Right-click index.html > "Open with Live Server"
   ```

3. Open `http://localhost:8000` in your browser

## Deployment

The site auto-deploys to Netlify when changes are pushed to the `main` branch.

### Manual Deploy
```bash
git add .
git commit -m "Your commit message"
git push origin main
```

## Image Hosting

Images are hosted on Cloudinary. To add new images:

1. Upload to Cloudinary dashboard
2. Use responsive image URLs:
   ```html
   <img 
     src="https://res.cloudinary.com/YOUR_CLOUD/image/upload/w_800,f_auto,q_auto/image.jpg"
     srcset="
       https://res.cloudinary.com/YOUR_CLOUD/image/upload/w_400,f_auto,q_auto/image.jpg 400w,
       https://res.cloudinary.com/YOUR_CLOUD/image/upload/w_800,f_auto,q_auto/image.jpg 800w,
       https://res.cloudinary.com/YOUR_CLOUD/image/upload/w_1200,f_auto,q_auto/image.jpg 1200w"
     sizes="100vw"
     alt="Description"
     loading="lazy"
   >
   ```

## Forms

Forms are handled by Netlify Forms. The form in `index.html` includes:
- `data-netlify="true"` attribute
- `netlify-honeypot="bot-field"` for spam prevention
- Hidden honeypot field

Submissions appear in the Netlify dashboard under Forms.

## Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Deep Black | `#0D0D0D` | Primary background |
| Rich Black | `#1A1A1A` | Cards, secondary bg |
| Champagne Gold | `#C9A227` | Accents, CTAs |
| Soft Gold | `#D4AF37` | Hover states |
| White | `#FFFFFF` | Text, contrast |
| Warm Gray | `#8A8A8A` | Secondary text |

## Typography

- **Headlines**: Cormorant Garamond (serif)
- **Body**: Inter (sans-serif)
- **Accents/CTAs**: Montserrat (sans-serif)

## Browser Support

- Chrome (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)
- Edge (last 2 versions)
- iOS Safari (last 2 versions)
- Chrome for Android (last 2 versions)

## Performance Targets

- First Contentful Paint: < 1.5s
- Largest Contentful Paint: < 2.5s
- Total Page Size: < 2MB
- Mobile PageSpeed Score: 90+

## License

All rights reserved. © 2025 South FL Auto Brokers
