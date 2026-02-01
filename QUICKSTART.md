# 🚀 Quick Start Guide - XADG Adult Ad Network

## Prerequisites

- Node.js 18.x or higher
- npm or yarn
- Cloudflare account (free)
- Git (optional)

## Step 1: Install Dependencies

```bash
cd astro-blog-starter-template
npm install
```

This will install:
- Astro 5.16.2
- Cloudflare Workers adapter
- MDX support
- Sitemap generator
- All required dependencies

## Step 2: Environment Setup

```bash
# Copy environment template
cp .env.example .env

# Edit .env with your configuration (optional for development)
```

## Step 3: Start Development Server

```bash
npm run dev
```

Visit http://localhost:4321 to see your site.

### What You'll See

- Homepage with hero section, features, and CTAs
- Publishers page with monetization details
- Advertisers page with traffic buying info
- Pricing page with transparent rates
- Payment methods page with crypto options
- About and Contact pages

## Step 4: Build for Production

```bash
npm run build
```

This creates a `dist/` folder with optimized static files ready for Cloudflare Workers.

## Step 5: Deploy to Cloudflare

### Option A: Manual Deployment

```bash
# Install Wrangler CLI globally
npm install -g wrangler

# Login to Cloudflare
wrangler login

# Deploy
npm run deploy
```

### Option B: Automatic Deployment via Dashboard

1. Go to https://dash.cloudflare.com
2. Navigate to **Workers & Pages** > **Create Application**
3. Connect your Git repository
4. Set build command: `npm run build`
5. Set output directory: `dist`
6. Click **Deploy**

## Step 6: Configure Custom Domain

1. In Cloudflare Dashboard, go to your Pages project
2. Click **Custom Domains**
3. Add your domain: `xadg.com`
4. Add www subdomain: `www.xadg.com`
5. Wait for DNS propagation (usually instant with Cloudflare)

## 🎨 Customization

### Update Site Information

Edit `src/consts.ts`:

```typescript
export const SITE_TITLE = "XADG - Premium Adult Ad Network";
export const SITE_URL = "https://xadg.com";
export const CONTACT_EMAIL = "support@xadg.com";
```

### Change Colors

Edit `src/layouts/Layout.astro`:

```css
:root {
  --primary: #ff0066;      /* Change primary color */
  --secondary: #6c00ff;    /* Change secondary color */
  --dark: #0a0a0a;
}
```

### Add Your Logo

1. Place logo files in `public/` folder
2. Update `src/components/Header.astro`:

```astro
<a href="/" class="logo">
  <img src="/logo.png" alt="XADG Logo" />
</a>
```

### Update Content

- Homepage: Edit `src/pages/index.astro`
- Publishers: Edit `src/pages/publishers.astro`
- Advertisers: Edit `src/pages/advertisers.astro`
- Other pages: Edit corresponding `.astro` files in `src/pages/`

## 📝 Add Blog Posts

Create new files in `src/content/blog/`:

```mdx
---
title: 'Your Blog Post Title'
description: 'Brief description of your post'
pubDate: 'Feb 01 2026'
heroImage: '/blog-placeholder-1.jpg'
---

Your blog content in Markdown or MDX format...
```

## 🔍 SEO Setup

### 1. Submit to Search Engines

**Google Search Console**
1. Go to https://search.google.com/search-console
2. Add property: `xadg.com`
3. Verify ownership (DNS or HTML tag)
4. Submit sitemap: `https://xadg.com/sitemap-index.xml`

**Bing Webmaster Tools**
1. Go to https://www.bing.com/webmasters
2. Add site: `xadg.com`
3. Verify ownership
4. Submit sitemap: `https://xadg.com/sitemap-index.xml`

### 2. Set Up Analytics

Add Google Analytics to `src/layouts/Layout.astro`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## 🧪 Testing

### Local Testing

```bash
# Test development build
npm run dev

# Test production build locally
npm run build
npm run preview
```

### SEO Validation

1. **PageSpeed Insights**: https://pagespeed.web.dev/
2. **Mobile-Friendly Test**: https://search.google.com/test/mobile-friendly
3. **Rich Results Test**: https://search.google.com/test/rich-results
4. **Security Headers**: https://securityheaders.com/

## 🐛 Troubleshooting

### Build Errors

```bash
# Clear cache and rebuild
rm -rf node_modules dist .astro
npm install
npm run build
```

### TypeScript Errors

```bash
# Run type checking
npm run check
```

### Deployment Issues

```bash
# View Wrangler logs
wrangler pages tail

# Check build output
ls -la dist/
```

## 📚 Next Steps

1. ✅ Site is live on Cloudflare Workers
2. ⬜ Add real content and images
3. ⬜ Set up Google Analytics
4. ⬜ Submit to search engines
5. ⬜ Configure email service for contact form
6. ⬜ Add payment gateway integration
7. ⬜ Build authentication system
8. ⬜ Create admin dashboard

## 📞 Need Help?

- **Documentation**: See `DEPLOYMENT.md` and `SEO-CHECKLIST.md`
- **Astro Docs**: https://docs.astro.build
- **Cloudflare Docs**: https://developers.cloudflare.com/pages/
- **Support**: support@xadg.com

## 🎉 Success!

Your XADG adult ad network website is now live and optimized for:
- ✅ Search engines (SEO)
- ✅ Performance (Cloudflare Workers)
- ✅ Security (Headers configured)
- ✅ Mobile devices (Responsive)
- ✅ Social sharing (Open Graph)

**Now go drive traffic and grow your ad network!** 🚀

---

**Deployment Time**: ~10 minutes
**Difficulty**: Easy
**Cost**: Free (Cloudflare Workers free tier)
