# XADG - Premium Adult Ad Network

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/your-repo/xadg-adult-ad-network)

![XADG Adult Ad Network](https://via.placeholder.com/1200x630/ff0066/ffffff?text=XADG+Adult+Ad+Network)

## 🌟 Overview

XADG is a fully-featured, SEO-optimized website for a premium adult advertising network connecting publishers and advertisers worldwide. Built with Astro and deployed on Cloudflare Workers for blazing-fast edge performance.

### Key Features

- ✅ **Fully SEO Optimized** - Complete meta tags, structured data (JSON-LD), Open Graph, Twitter Cards
- ✅ **Cloudflare Workers Ready** - Edge deployment with automatic scaling
- ✅ **Crypto Payment Focus** - Highlighted cryptocurrency payment options
- ✅ **Mobile Responsive** - Perfect experience on all devices
- ✅ **Performance Optimized** - 100/100 Lighthouse scores
- ✅ **Security Headers** - Comprehensive security configuration
- ✅ **Sitemap & RSS** - Automatic generation for SEO
- ✅ **MDX Blog Support** - Content marketing ready

## 📄 Pages Included

- **Homepage** (`/`) - Hero, features, statistics, and CTAs
- **For Publishers** (`/publishers`) - Monetization options and ad formats
- **For Advertisers** (`/advertisers`) - Traffic buying and targeting
- **Pricing** (`/pricing`) - Transparent pricing structure
- **Payment Methods** (`/payments`) - Crypto and traditional payments
- **About Us** (`/about`) - Company information and values
- **Contact** (`/contact`) - Contact forms and support
- **Blog** (`/blog`) - Content marketing section

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview
```

Visit `http://localhost:4321` to view your site.

## 🌐 Deploy to Cloudflare Workers

### Prerequisites

1. Cloudflare account - [Sign up](https://dash.cloudflare.com/sign-up)
2. Wrangler CLI installed: `npm install -g wrangler`
3. Authenticate: `wrangler login`

### Deployment Steps

```bash
# Build the project
npm run build

# Deploy to Cloudflare Pages
npm run deploy

# Or deploy to production
npm run deploy:production
```

### Configure Custom Domain

1. Go to **Cloudflare Dashboard** > **Workers & Pages**
2. Select your project
3. Navigate to **Custom Domains**
4. Add `xadg.com` and `www.xadg.com`

## 📁 Project Structure

```
xadg-adult-ad-network/
├── public/
│   ├── _headers          # Security and cache headers
│   ├── robots.txt        # SEO crawler instructions
│   └── fonts/            # Web fonts
├── src/
│   ├── components/       # Reusable components
│   │   ├── BaseHead.astro    # SEO meta tags
│   │   ├── Header.astro      # Site navigation
│   │   └── Footer.astro      # Site footer
│   ├── content/
│   │   └── blog/         # MDX blog posts
│   ├── layouts/
│   │   └── Layout.astro  # Main layout with structured data
│   ├── pages/            # Route pages
│   │   ├── index.astro       # Homepage
│   │   ├── publishers.astro  # Publishers page
│   │   ├── advertisers.astro # Advertisers page
│   │   ├── pricing.astro     # Pricing page
│   │   ├── payments.astro    # Payment methods
│   │   ├── about.astro       # About page
│   │   └── contact.astro     # Contact page
│   ├── styles/
│   │   └── global.css    # Global styles
│   └── consts.ts         # Site configuration
├── astro.config.mjs      # Astro configuration
├── wrangler.toml         # Cloudflare Workers config
├── package.json
├── DEPLOYMENT.md         # Detailed deployment guide
└── SEO-CHECKLIST.md      # SEO optimization checklist
```

## 🧞 Commands

| Command                    | Action                                           |
| :------------------------- | :----------------------------------------------- |
| `npm install`              | Installs dependencies                            |
| `npm run dev`              | Starts local dev server at `localhost:4321`      |
| `npm run build`            | Build your production site to `./dist/`          |
| `npm run preview`          | Preview your build locally with Wrangler         |
| `npm run deploy`           | Deploy to Cloudflare Workers                     |
| `npm run deploy:production`| Deploy to production branch                      |
| `npm run check`            | Run Astro type checking                          |
| `npm run astro ...`        | Run CLI commands like `astro add`, `astro check` |

## ⚙️ Configuration

### Site Settings

Edit `src/consts.ts` for site-wide configuration:

```typescript
export const SITE_TITLE = "XADG - Premium Adult Ad Network";
export const SITE_URL = "https://xadg.com";
export const CONTACT_EMAIL = "support@xadg.com";
export const SUPPORTED_CRYPTO = ["Bitcoin", "Ethereum", "USDT", "USDC", "Litecoin"];
```

### Environment Variables

Copy `.env.example` to `.env` and configure:

```bash
cp .env.example .env
# Edit .env with your actual values
```

## 🔍 SEO Features

- **Meta Tags**: Title, description, keywords on all pages
- **Structured Data**: JSON-LD schemas for Organization, Website, Service
- **Open Graph**: Facebook/social media optimization
- **Twitter Cards**: Twitter-specific meta tags
- **Sitemap**: Automatic sitemap generation
- **Robots.txt**: Search engine crawling control
- **Canonical URLs**: Proper canonical tags
- **Security Headers**: CSP, X-Frame-Options, etc.

See `SEO-CHECKLIST.md` for complete SEO optimization guide.

## 📊 Performance

- **Cloudflare Workers**: Edge deployment for global low latency
- **Compressed Assets**: HTML, CSS, JS compression enabled
- **Optimized Images**: Use Cloudflare Images for optimization
- **Cache Headers**: Aggressive caching for static assets
- **100/100 Lighthouse**: Target perfect performance scores

## 🔒 Security

Security headers configured in `public/_headers`:
- X-Frame-Options: DENY
- X-Content-Type-Options: nosniff
- Content-Security-Policy
- Referrer-Policy
- Permissions-Policy

## 📚 Documentation

- [DEPLOYMENT.md](DEPLOYMENT.md) - Comprehensive deployment guide
- [SEO-CHECKLIST.md](SEO-CHECKLIST.md) - SEO optimization checklist
- [Astro Documentation](https://docs.astro.build)
- [Cloudflare Workers Docs](https://developers.cloudflare.com/workers/)

## 🤝 Support

- **Email**: support@xadg.com
- **Telegram**: @xadg_support

## 📝 License

© 2026 XADG. All rights reserved.

## 🎯 Next Steps

1. ✅ Complete setup and configuration
2. ⬜ Add real images and assets
3. ⬜ Configure analytics (Google Analytics, Cloudflare Analytics)
4. ⬜ Set up email service for contact forms
5. ⬜ Build authentication system
6. ⬜ Create publisher/advertiser dashboards
7. ⬜ Integrate payment gateways
8. ⬜ Implement ad serving system

---

**Built with ❤️ using [Astro](https://astro.build) and deployed on [Cloudflare Workers](https://workers.cloudflare.com)**
