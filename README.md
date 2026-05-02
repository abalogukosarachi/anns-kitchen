# Nri Oma Kitchen - Authentic Igbo Flavours

A modern, warm, and mobile-first website for **Nri Oma Kitchen**, an Eastern Nigerian / Igbo-style food ordering business. Built with Next.js, React, and Tailwind CSS, this MVP enables customers to browse the menu and place orders directly via WhatsApp.

## 🎯 Project Overview

**Nri Oma Kitchen** is a one-page landing website designed to:
- Showcase authentic Igbo food culture and cuisine
- Display a featured menu with prices and descriptions
- Enable quick WhatsApp ordering without payment processing
- Build trust through warm, premium branding
- Optimize for mobile-first ordering

**Key Features:**
- Responsive design optimized for mobile phones
- WhatsApp integration with pre-filled order messages
- Smooth scrolling navigation
- Sticky WhatsApp button for quick access
- High-quality food photography
- Warm African color palette (Palm Oil Red, Burnt Orange, Forest Green)
- Premium typography (Playfair Display + Poppins)

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ (check with `node --version`)
- pnpm (comes pre-installed, or install with `npm install -g pnpm`)

### Installation & Running Locally

1. **Clone or navigate to the project directory:**
   ```bash
   cd nri-oma-kitchen
   ```

2. **Install dependencies:**
   ```bash
   npm install
   # or
   pnpm install
   ```

3. **Start the development server:**
   ```bash
   npm run dev
   # or
   pnpm dev
   ```

4. **Open in browser:**
   - Local: `http://localhost:3000`
   - Network: Check terminal output for network URL

The site will auto-reload as you make changes.

## 📁 Project Structure

```
nri-oma-kitchen/
├── client/
│   ├── public/              # Static files (favicon, robots.txt)
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/
│   │   │   └── Home.tsx     # Main landing page (all sections)
│   │   ├── App.tsx          # Route configuration
│   │   ├── main.tsx         # React entry point
│   │   └── index.css        # Global styles & design tokens
│   └── index.html           # HTML template
├── server/                  # Backend placeholder (not used in MVP)
├── package.json             # Dependencies & scripts
└── README.md               # This file
```

## 🎨 Design System

### Color Palette
- **Primary (Palm Oil Red):** `#C84C1A` - Main brand color for CTAs and accents
- **Secondary (Burnt Orange):** `#D97706` - Complementary warm tone
- **Accent (Forest Green):** `#1F4620` - Earthy, fresh ingredient feel
- **Background (Cream):** `#FBF8F3` - Warm, inviting background
- **Text (Deep Charcoal):** `#1A1A1A` - High contrast for readability
- **Gold:** `#D4AF37` - Subtle premium accents

### Typography
- **Headers:** Playfair Display (serif) - Premium, artisanal feel
- **Body Text:** Poppins (sans-serif) - Modern, readable
- **Font Sizes:** Responsive scaling from mobile to desktop

### Component Styles
- **Menu Cards:** Rounded corners (16px), soft shadows, hover lift effect
- **Buttons:** Smooth transitions, active state feedback
- **Sections:** Generous whitespace, breathing room between content
- **Gallery:** Staggered layout with hover zoom effect

## 🔧 Customization Guide

### 1. Change the WhatsApp Number

**File:** `client/src/pages/Home.tsx`

Find this line at the top:
```typescript
const WHATSAPP_NUMBER = "+2348000000000";
```

Replace with your actual WhatsApp number (include country code):
```typescript
const WHATSAPP_NUMBER = "+234XXXXXXXXXX"; // Your number here
```

**Also update the phone number in the Contact section:**
Search for `Phone: +234 800 000 0000` and replace with your number.

### 2. Update Menu Items

**File:** `client/src/pages/Home.tsx`

Find the `menuItems` array (around line 30):
```typescript
const menuItems: MenuItem[] = [
  {
    id: "1",
    name: "Ofe Nsala",
    description: "White soup made with fresh catfish/goat meat and rich local spices.",
    price: 4500,
    image: "https://...", // Image URL
  },
  // ... more items
];
```

**To add a new item:**
```typescript
{
  id: "9",
  name: "Your Dish Name",
  description: "Description of your dish.",
  price: 5000,
  image: "https://your-image-url.com/image.jpg",
},
```

**To remove an item:** Simply delete the object from the array.

### 3. Update Contact Information

**File:** `client/src/pages/Home.tsx`

Search for the Contact Section and update:
- **Phone:** `+234 800 000 0000` → Your phone number
- **WhatsApp:** `+234 800 000 0000` → Your WhatsApp number
- **Location:** `Enugu / Lagos (Placeholder)` → Your actual location
- **Hours:** `Monday - Saturday, 9:00 AM - 8:00 PM` → Your hours
- **Instagram:** `@nriomakitchen` → Your Instagram handle

### 4. Update Business Name & Branding

**File:** `client/index.html`
```html
<title>Nri Oma Kitchen - Authentic Igbo Flavours</title>
```

**File:** `client/src/pages/Home.tsx`
- Update the header logo text
- Update footer brand name
- Update all references to "Nri Oma Kitchen"

### 5. Add Your Own Images

1. **Generate or upload high-quality food images** (JPG or PNG)
2. **Store images externally** (Cloudinary, Unsplash, or your own server)
3. **Replace image URLs** in the code:
   - Hero image: Search for `hero-banner` URL
   - Menu card images: Update URLs in `menuItems` array
   - Gallery images: Update URLs in `galleryItems` array

### 6. Customize Colors

**File:** `client/src/index.css`

Find the `:root` section and update color variables:
```css
:root {
  --primary: #C84C1A;           /* Change to your primary color */
  --accent: #D97706;            /* Change to your accent color */
  --secondary: #1F4620;         /* Change to your secondary color */
  --background: #FBF8F3;        /* Change background color */
  /* ... more colors ... */
}
```

## 📱 Mobile Optimization

The website is fully responsive and optimized for mobile ordering:
- **Sticky header** with navigation
- **Sticky WhatsApp button** (appears after scrolling)
- **Touch-friendly buttons** with large tap targets
- **Optimized images** for fast loading
- **Single-column layout** on mobile, multi-column on desktop

## 🚀 Deployment to Vercel

### Option 1: Using Vercel CLI

1. **Install Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Deploy from project directory:**
   ```bash
   vercel
   ```

3. **Follow the prompts** to connect your GitHub account and deploy.

### Option 2: Using GitHub Integration

1. **Push your code to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Nri Oma Kitchen website"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/nri-oma-kitchen.git
   git push -u origin main
   ```

2. **Go to [vercel.com](https://vercel.com)** and sign in with GitHub
3. **Click "Add New Project"** and select your repository
4. **Vercel will auto-detect Next.js** and configure settings
5. **Click "Deploy"** and your site goes live!

### Option 3: Using Manus Hosting (Recommended)

If you're using Manus, you can deploy directly through the platform:
1. Click the **Publish** button in the Management UI
2. Manus handles hosting, SSL, and custom domains
3. Your site is live instantly with no additional configuration

## 📝 Scripts

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview

# Check TypeScript types
npm run check

# Format code with Prettier
npm run format
```

## 🎯 Next Steps (Future Features)

This MVP focuses on WhatsApp ordering. Future enhancements could include:
- Online payment integration (Stripe, Paystack)
- Delivery tracking
- Customer accounts & order history
- Email notifications
- Admin dashboard for menu management
- Real-time availability updates

## 💡 Tips for Success

1. **Keep menu updated:** Regularly update prices and availability
2. **Respond quickly on WhatsApp:** Fast responses build customer trust
3. **Add real photos:** Replace placeholder images with actual food photos
4. **Test on mobile:** Always test the site on real phones before sharing
5. **Share on social media:** Link to your website from Instagram and Facebook
6. **Gather feedback:** Ask customers what dishes they'd like to see

## 🛠️ Troubleshooting

**Port 3000 already in use:**
```bash
# Use a different port
npm run dev -- --port 3001
```

**Images not loading:**
- Check image URLs are correct and publicly accessible
- Ensure URLs start with `https://`
- Test URLs in browser directly

**WhatsApp button not working:**
- Verify phone number format includes country code (e.g., +234...)
- Test the WhatsApp link in browser first
- Ensure phone number is valid and has WhatsApp installed

**Styling looks off:**
- Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Restart dev server (`npm run dev`)
- Check that all CSS files are properly imported

## 📞 Support & Questions

For questions about customization or deployment:
- Check the code comments in `Home.tsx` for detailed explanations
- Review Tailwind CSS documentation: [tailwindcss.com](https://tailwindcss.com)
- Review React documentation: [react.dev](https://react.dev)

## 📄 License

This project is open-source and available for personal and commercial use.

---

**Built with ❤️ for Nri Oma Kitchen**

*Authentic Igbo Flavours, Freshly Made for You.*
