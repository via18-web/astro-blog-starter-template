# XADG - Premium Adult Ad Network Website

## 🚀 Features

- **Fully SEO Optimized**: Meta tags, Open Graph, Twitter Cards, JSON-LD structured data
- **Cloudflare Workers Ready**: Configured for edge deployment with Astro + Cloudflare adapter
- **Crypto Payments Focus**: Highlighted cryptocurrency payment options throughout
- **Responsive Design**: Mobile-first approach with modern UI/UX
- **Performance Optimized**: Fast loading with compression, caching headers, and asset optimization
- **Security Headers**: Comprehensive security headers for production deployment

## 📄 Pages Included

- **Home** (`/`) - Hero section, features, statistics, CTAs
- **Publishers** (`/publishers`) - Monetization options, ad formats, revenue info
- **Advertisers** (`/advertisers`) - Traffic buying, targeting options, campaign tools
- **Pricing** (`/pricing`) - Transparent pricing for both publishers and advertisers
- **Payments** (`/payments`) - Cryptocurrency and traditional payment methods
- **About** (`/about`) - Company information, mission, values
- **Contact** (`/contact`) - Contact forms and support options
- **Blog** (`/blog`) - Content marketing section

## 🛠️ Technology Stack

- **Framework**: Astro 5.x
- **Hosting**: Cloudflare Workers
- **Styling**: Custom CSS with CSS Variables
- **Type Safety**: TypeScript
- **Content**: MDX for blog posts

## 📦 Installation

\`\`\`bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
\`\`\`

## 🌐 Deployment to Cloudflare Workers

### Prerequisites

1. Cloudflare account
2. Wrangler CLI installed: \`npm install -g wrangler\`
3. Authenticate: \`wrangler login\`

### Deploy Steps

\`\`\`bash
# Build the project
npm run build

# Deploy to Cloudflare Workers
npx wrangler pages deploy dist

# Or use the deploy script
npm run deploy
\`\`\`

### Configure Custom Domain

1. Go to Cloudflare Dashboard > Workers & Pages
2. Select your project
3. Go to Custom Domains
4. Add \`xadg.com\` and \`www.xadg.com\`

## ⚙️ Configuration

### Site Settings

Edit \`src/consts.ts\` to update:

\`\`\`typescript
export const SITE_TITLE = "XADG - Premium Adult Ad Network";
export const SITE_URL = "https://xadg.com";
export const CONTACT_EMAIL = "support@xadg.com";
export const SUPPORTED_CRYPTO = ["Bitcoin", "Ethereum", "USDT", "USDC", "Litecoin"];
\`\`\`

### Astro Config

\`astro.config.mjs\` is already configured for Cloudflare Workers:

\`\`\`javascript
export default defineConfig({
  site: "https://xadg.com",
  adapter: cloudflare({
    platformProxy: { enabled: true }
  }),
  compressHTML: true
});
\`\`\`

## 🔍 SEO Optimization

### Implemented SEO Features

1. **Meta Tags**: Complete title, description, keywords for all pages
2. **Open Graph**: Facebook/social media sharing optimization
3. **Twitter Cards**: Twitter-specific meta tags
4. **JSON-LD Structured Data**: Organization, Website, Service, Breadcrumb schemas
5. **Canonical URLs**: Proper canonical tags on all pages
6. **Robots.txt**: Search engine crawling instructions
7. **Sitemap**: Automatic sitemap generation via Astro sitemap plugin
8. **Security Headers**: \`_headers\` file with CSP, X-Frame-Options, etc.

### SEO Best Practices

- Semantic HTML structure
- Descriptive alt tags (add to images)
- Internal linking throughout
- Mobile-responsive design
- Fast loading times (Cloudflare Workers edge deployment)
- HTTPS by default (Cloudflare)

## 🔒 Security Features

The \`public/_headers\` file includes:

- X-Frame-Options: DENY
- X-Content-Type-Options: nosniff
- Content-Security-Policy
- Referrer-Policy
- Permissions-Policy

## 🎨 Customization

### Colors

Edit CSS variables in \`src/layouts/Layout.astro\`:

\`\`\`css
:root {
  --primary: #ff0066;
  --secondary: #6c00ff;
  --dark: #0a0a0a;
  --gradient: linear-gradient(135deg, #ff0066 0%, #6c00ff 100%);
}
\`\`\`

### Navigation

Update navigation in \`src/components/Header.astro\`:

\`\`\`javascript
const navItems = [
  { name: 'Home', href: '/' },
  { name: 'Publishers', href: '/publishers' },
  // Add more items
];
\`\`\`

## 📊 Analytics Integration

Add your analytics code to \`src/layouts/Layout.astro\`:

\`\`\`html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
\`\`\`

## 🎯 Performance Optimization

- **Cloudflare CDN**: Global edge network for fast delivery
- **Compressed Assets**: HTML, CSS, JS automatically compressed
- **Image Optimization**: Use Cloudflare Images for automatic optimization
- **Cache Headers**: Aggressive caching for static assets
- **Lazy Loading**: Implement for images and heavy content

## 📱 Mobile Optimization

- Responsive breakpoints in CSS
- Touch-friendly navigation
- Mobile-optimized forms
- Fast mobile performance

## 🔄 Content Updates

### Update Pages

Edit files in \`src/pages/\`:
- \`index.astro\` - Homepage
- \`publishers.astro\` - Publishers page
- \`advertisers.astro\` - Advertisers page
- etc.

### Add Blog Posts

Create new MDX files in \`src/content/blog/\`:

\`\`\`mdx
---
title: 'Your Post Title'
description: 'Post description'
pubDate: 'Feb 01 2026'
---

Your content here...
\`\`\`

## 🧪 Testing

\`\`\`bash
# Run Astro checks
npm run astro check

# Build and preview
npm run build && npm run preview

# Test locally with Wrangler
npx wrangler pages dev dist
\`\`\`

## 📈 Monitoring

1. **Cloudflare Analytics**: Built-in traffic analytics
2. **Web Vitals**: Monitor Core Web Vitals in Cloudflare
3. **Error Tracking**: Set up Sentry or similar
4. **Uptime Monitoring**: Use UptimeRobot or Pingdom

## 🤝 Support & Contact

- **Email**: support@xadg.com
- **Telegram**: @xadg_support
- **Documentation**: [Internal wiki or docs]

## 📝 License

© 2026 XADG. All rights reserved.

## 🚨 Important Notes

1. **Adult Content Warning**: Ensure all pages have 18+ warnings where appropriate
2. **Compliance**: Ensure compliance with adult content regulations in target markets
3. **Payment Processing**: Integrate actual crypto payment gateways (not included in this template)
4. **User Authentication**: Add login/signup functionality (not included)
5. **Dashboard**: Build publisher/advertiser dashboards separately

## 🔗 Useful Resources

- [Astro Documentation](https://docs.astro.build)
- [Cloudflare Workers Docs](https://developers.cloudflare.com/workers/)
- [Cloudflare Pages](https://developers.cloudflare.com/pages/)
- [Schema.org for SEO](https://schema.org/)

## 🎉 Next Steps

1. ✅ Deploy to Cloudflare Workers
2. ✅ Configure custom domain (xadg.com)
3. ⬜ Add real images and assets
4. ⬜ Set up analytics tracking
5. ⬜ Configure email service for contact forms
6. ⬜ Build authentication system
7. ⬜ Create publisher/advertiser dashboards
8. ⬜ Integrate payment gateways
9. ⬜ Set up advertising tracking system
10. ⬜ Add GDPR/privacy compliance features

---

**Built with ❤️ for xadg.com - Premium Adult Ad Network**
