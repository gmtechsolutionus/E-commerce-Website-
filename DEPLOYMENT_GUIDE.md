# 🚀 JERSEY SOCIETY Theme - Deployment Guide

## ✅ What's Been Completed

### 1. Theme Structure ✓
All Shopify theme files have been created and committed to the branch:
- **Branch**: `cursor/build-jersey-society-shopify-theme-with-themeflow-df89`
- **Directory**: `/theme/`
- **18 theme files** created and tracked

### 2. Build Pipeline ✓
- Tailwind CSS installed and configured
- Build script added to `package.json`
- GitHub Actions workflow created at `.github/workflows/build-theme.yml`
- PostCSS configuration added

### 3. Theme Files Created ✓

**Layout:**
- ✅ `theme.liquid` - Base layout

**Sections (9):**
- ✅ `header.liquid` - Sticky glassy header with search & cart
- ✅ `footer.liquid` - Auto-populated Shopify policy links
- ✅ `hero-feature.liquid` - Homepage hero
- ✅ `featured-collection.liquid` - Product showcase
- ✅ `main-product.liquid` - Product detail page
- ✅ `collection-products.liquid` - Product grid
- ✅ `collection-banner.liquid` - Collection header
- ✅ `related-products.liquid` - Related items
- ✅ `cart-items.liquid` - Shopping cart

**Templates (4 JSON):**
- ✅ `index.json` - Homepage
- ✅ `product.json` - Product page
- ✅ `collection.json` - Collection page
- ✅ `cart.json` - Cart page

**Assets:**
- ✅ `theme.css` - Complete dark/neon design system
- ✅ `theme.js` - JavaScript enhancements

---

## 🎯 Next Steps: ThemeFlow Deployment

### Step 1: Connect to ThemeFlow

1. **Go to ThemeFlow App**: https://apps.shopify.com/themeflow (or your ThemeFlow dashboard)

2. **Add New Theme Deployment**:
   - Repository: `<your-github-repo>`
   - Branch: `cursor/build-jersey-society-shopify-theme-with-themeflow-df89`
   - Directory: `/theme`
   - Build Command (optional): `npm ci && npm run build:theme`

3. **Configure Auto-Deploy**:
   - Enable automatic deployment on push
   - Set target Shopify store: `<your-store>.myshopify.com`

### Step 2: Configure Shopify Store

#### A. Set Up Policies (REQUIRED)
Go to **Shopify Admin → Settings → Policies** and fill in:

1. **Shipping Policy**
   - Click "Create from template" or write custom policy
   - This will be auto-linked in footer

2. **Refund Policy**
   - Set your return/exchange terms
   - Auto-linked in footer

3. **Terms of Service**
   - Define terms and conditions
   - Auto-linked in footer

4. **Privacy Policy**
   - GDPR/privacy compliance text
   - Auto-linked in footer

#### B. Create Pages (RECOMMENDED)
Go to **Shopify Admin → Online Store → Pages** and create:

1. **About Page**
   - Handle: `about`
   - URL will be: `/pages/about`

2. **Contact Page**
   - Handle: `contact`
   - URL will be: `/pages/contact`

3. **Size Guide**
   - Handle: `size-guide`
   - URL will be: `/pages/size-guide`

4. **FAQs**
   - Handle: `faq`
   - URL will be: `/pages/faq`

#### C. Set Up Collections
1. **Create "Featured Jerseys" collection** (or any collection)
2. **Edit homepage** in theme customizer
3. **Configure Featured Collection section** to show your products

### Step 3: Deploy & Activate

1. **Push to GitHub** (already done - theme is committed)

2. **ThemeFlow will auto-deploy** to your Shopify store

3. **Go to Shopify Admin → Online Store → Themes**

4. **Preview the new theme** (JERSEY SOCIETY)

5. **Publish when ready**

---

## 🔐 Your Shopify API Credentials

**Store Access:**
- **Admin API Token**: `[Stored securely - check your Shopify Admin]`
- **API Key**: `[Stored securely - check your Shopify Admin]`
- **Secret Key**: `[Stored securely - check your Shopify Admin]`

⚠️ **Security Note**: Access your API credentials in Shopify Admin → Settings → Apps and sales channels → Develop apps. Never commit credentials to repositories.

---

## 🎨 Theme Features

### Design System
- **Dark Mode**: Cyberpunk aesthetic (`#0B0F14` background)
- **Neon Accents**: Cyan (`#00E5FF`) + Pink (`#FF3DCC`)
- **Glassmorphism**: Backdrop-blur cards
- **Sticky Header**: Always-visible navigation
- **Responsive**: Mobile-first design

### Pages Included
- ✅ Homepage with hero + featured products
- ✅ Product detail pages
- ✅ Collection browsing with pagination
- ✅ Shopping cart with quantity controls
- ✅ Search functionality
- ✅ Related products section

### Online Store 2.0 Features
- Section-based architecture
- JSON templates for easy customization
- Drag-and-drop section management
- No code required for basic edits

---

## 🛠️ Customization Options

### In Shopify Theme Editor
1. Go to **Online Store → Themes → Customize**
2. Available settings:
   - Upload custom logo
   - Edit tagline
   - Configure featured collections
   - Add/remove/reorder sections

### Advanced Customization
Edit files in `/theme/` directory and push to GitHub:

**Styling:**
- Edit `/theme/assets/theme.css` for design changes
- Modify color variables in `:root` section

**Layout:**
- Edit section files in `/theme/sections/`
- Update templates in `/theme/templates/`

**Features:**
- Add JavaScript to `/theme/assets/theme.js`

---

## 📋 Pre-Launch Checklist

- [ ] ThemeFlow connected to GitHub repo
- [ ] Shopify policies configured (Shipping, Returns, Terms, Privacy)
- [ ] Pages created (About, Contact, Size Guide, FAQ)
- [ ] Collections set up with products
- [ ] Featured collection configured on homepage
- [ ] Theme deployed via ThemeFlow
- [ ] Theme previewed in Shopify
- [ ] Test checkout flow
- [ ] Mobile responsiveness verified
- [ ] Theme published to live store

---

## 🐛 Troubleshooting

### Theme Not Deploying?
1. Check ThemeFlow dashboard for build errors
2. Verify branch name is correct
3. Ensure `/theme` directory path is set
4. Check GitHub Actions workflow status

### Broken Links in Footer?
- Ensure all 4 policies are filled in Shopify Admin
- Policies must be saved and published

### Featured Collection Not Showing?
1. Create at least one collection in Shopify
2. Add products to the collection
3. In theme customizer, select the collection for "Featured Collection" section

### Build Errors?
```bash
# Run locally to test
npm install
npm run build:theme
```

---

## 📚 Resources

- [Shopify Theme Development](https://shopify.dev/themes)
- [Liquid Reference](https://shopify.dev/api/liquid)
- [Online Store 2.0 Guide](https://shopify.dev/themes/architecture)
- [ThemeFlow Documentation](https://themeflow.com/docs)

---

## 🎉 You're All Set!

The **JERSEY SOCIETY** theme is ready to deploy. Follow the steps above to:
1. Connect ThemeFlow
2. Configure your Shopify store
3. Deploy and publish

**Questions?** Check the troubleshooting section or Shopify/ThemeFlow documentation.

---

**JERSEY SOCIETY** — Future-Made Jerseys. Zero Compromise. 🏀⚡
