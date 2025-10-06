# JERSEY SOCIETY - Shopify Theme

A modern, futuristic Online Store 2.0 theme built for ThemeFlow deployment.

## 🎨 Features

- **Modern Glassmorphic UI**: Sticky glassy header with neon accents
- **Dark Theme**: Cyberpunk-inspired dark background with cyan/pink gradients
- **Responsive Design**: Mobile-first approach with clean breakpoints
- **Online Store 2.0**: Section-based architecture with JSON templates
- **Policy Integration**: Auto-pulls Shipping, Returns, Terms, and Privacy from Shopify Admin
- **ThemeFlow Ready**: Optimized for GitHub Actions deployment

## 📁 Structure

```
/theme
├── /layout
│   └── theme.liquid              # Base layout
├── /sections
│   ├── header.liquid             # Sticky navigation
│   ├── footer.liquid             # Footer with policy links
│   ├── hero-feature.liquid       # Homepage hero
│   ├── featured-collection.liquid
│   ├── main-product.liquid       # Product detail page
│   ├── collection-products.liquid
│   ├── collection-banner.liquid
│   ├── related-products.liquid
│   └── cart-items.liquid
├── /snippets
│   └── product-card.liquid       # Reusable product card
├── /templates
│   ├── index.json                # Homepage template
│   ├── product.json              # Product page template
│   ├── collection.json           # Collection page template
│   └── cart.json                 # Cart page template
├── /config
│   └── settings_schema.json      # Theme settings
└── /assets
    ├── theme.css                 # Main stylesheet
    └── theme.js                  # JavaScript enhancements
```

## 🚀 Setup with ThemeFlow

### 1. ThemeFlow Configuration
- **Branch**: `main` (or your deployment branch)
- **Directory**: `/theme`
- **Build Step** (optional): `npm ci && npm run build:theme`

### 2. Shopify Admin Setup
1. Go to **Settings → Policies**
2. Fill in:
   - Shipping Policy
   - Refund/Returns Policy
   - Terms of Service
   - Privacy Policy
3. Create Pages for:
   - About (`/pages/about`)
   - Contact (`/pages/contact`)
   - Size Guide (`/pages/size-guide`)
   - FAQs (`/pages/faq`)

### 3. Optional: Tailwind Build Pipeline

If you want to use Tailwind utilities:

```bash
# Install dependencies
npm install -D tailwindcss postcss autoprefixer

# Build theme CSS
npm run build:theme
```

The GitHub Actions workflow (`.github/workflows/build-theme.yml`) will auto-compile on push.

## 🎨 Design System

### Colors
```css
--bg: #0B0F14        /* Dark background */
--card: #121824      /* Card background */
--text: #E6F1FF      /* Primary text */
--muted: #8AA0B7     /* Muted text */
--primary: #00E5FF   /* Cyan accent */
--accent: #FF3DCC    /* Pink accent */
```

### Components
- `.card` - Glassmorphic card with subtle border
- `.btn` - Primary button with neon border
- `.logo` - Gradient text logo
- `.header-sticky` - Sticky header with backdrop blur
- `.input` - Styled form input
- `.page-width` - Max-width container (1200px)

## 📝 Customization

### Theme Settings
Edit in Shopify Admin → Online Store → Themes → Customize:
- Logo image
- Tagline text

### Homepage Sections
Edit `/theme/templates/index.json` to add/remove sections:
```json
{
  "sections": {
    "hero": { "type": "hero-feature" },
    "featured": { "type": "featured-collection" }
  },
  "order": ["hero", "featured"]
}
```

### Styling
- **Quick edits**: Modify `/theme/assets/theme.css`
- **Advanced**: Use Tailwind in `src/tailwind.css` and run build

## 🔧 Development

### Local Testing
```bash
# Install Shopify CLI
npm install -g @shopify/cli @shopify/theme

# Connect to your store
shopify theme dev --store=your-store.myshopify.com

# Preview at localhost:9292
```

### Theme Check (Linting)
```bash
shopify theme check
```

## 🚢 Deployment

### Via ThemeFlow (Recommended)
1. Commit changes to your branch
2. Push to GitHub
3. ThemeFlow auto-deploys to Shopify

### Manual Deploy
```bash
shopify theme push --path=./theme
```

## 📦 What's Included

✅ Sticky header with search + cart  
✅ Footer with auto-populated policy links  
✅ Homepage hero + featured collection  
✅ Product detail page  
✅ Collection browsing + pagination  
✅ Shopping cart with quantity updates  
✅ Related products section  
✅ Responsive product cards  
✅ Dark mode + neon aesthetics  
✅ Online Store 2.0 compatible  
✅ ThemeFlow ready  

## 🔗 API Credentials

**Note**: Keep these secure and never commit to public repos.

To access your API credentials:
1. Go to **Shopify Admin → Settings → Apps and sales channels**
2. Click **"Develop apps"**
3. Select your app or create a new one
4. Get your Admin API access token, API key, and API secret key

## 📚 Resources

- [Shopify Theme Development](https://shopify.dev/themes)
- [Liquid Reference](https://shopify.dev/api/liquid)
- [ThemeFlow Documentation](https://themeflow.com/docs)

---

**JERSEY SOCIETY** — Future-Made Jerseys. Zero Compromise.
