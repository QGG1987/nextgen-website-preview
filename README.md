# NextGen Marketing Hub Website

> Agency website for https://nextgenmarketinghub.top

## Quick Start (Local)

```bash
npm install
npm run dev
# Open http://localhost:3001
```

## Deployment Options

### Option 1: Vercel (Recommended)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Set custom domain in Vercel dashboard:
# nextgenmarketinghub.top
```

### Option 2: Netlify

```bash
# Install Netlify CLI
npm i -g netlify-cli

# Deploy
netlify deploy --prod

# Set custom domain in Netlify dashboard
```

### Option 3: Cloudflare Pages

1. Go to Cloudflare Dashboard → Pages
2. Connect to GitHub repo
3. Deploy settings: Build command = (none), Output directory = `.`
4. Add custom domain

## DNS Setup (for nextgenmarketinghub.top)

Add these records at your domain registrar:

### For Vercel:
```
Type: A
Name: @
Value: 76.76.21.21

Type: CNAME
Name: www
Value: cname.vercel-dns.com
```

### For Netlify:
```
Type: A
Name: @
Value: 75.2.60.5

Type: CNAME
Name: www
Value: your-site.netlify.app
```

### For Cloudflare:
```
Type: CNAME
Name: @
Value: your-site.pages.dev

Type: CNAME
Name: www
Value: your-site.pages.dev
```

## File Structure

```
website/
├── index.html          # Main website (single page)
├── package.json        # Node config
└── README.md           # This file
```

## Customization

### Update Contact Info
Edit `index.html` and replace:
- `hello@nextgenmarketinghub.top` → your email
- `(555) 123-4567` → your phone
- Update form submission endpoint

### Connect Form Submissions
Options:
1. **Formspree**: `<form action="https://formspree.io/f/YOUR_ID" method="POST">`
2. **Netlify Forms**: Add `netlify` attribute to form
3. **Custom API**: Point to your own backend

### Add Analytics
Add before `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXX');
</script>

<!-- Facebook Pixel -->
<script>
  !function(f,b,e,v,n,t,s){...}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', 'YOUR_PIXEL_ID');
  fbq('track', 'PageView');
</script>
```

## Performance

- Single HTML file = instant load
- Tailwind via CDN (can be inlined for production)
- No heavy JavaScript
- Mobile-first responsive design

## SEO Checklist

- [x] Meta description
- [x] Open Graph tags
- [x] Semantic HTML
- [x] Fast loading
- [x] Mobile responsive
- [ ] Add Google Search Console verification
- [ ] Add sitemap.xml
- [ ] Submit to Google

---

*Last updated: 2026-03-14*
