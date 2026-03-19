# KDP TikTok Profit Accelerator

A modern, high-converting website for Amazon KDP authors to discover trending niches, generate viral TikTok scripts, and scale their publishing business.

## Features

- **Trend Dashboard**: Real-time trending BookTok niches with growth metrics and viral potential scores
- **AI Script Generator**: Generate TikTok-ready hooks based on book title, genre, and target audience
- **Resource Hub**: Curated list of recommended tools for KDP authors
- **Responsive Design**: Fully optimized for desktop, tablet, and mobile devices
- **Modern UI**: Dark mode design with neon accents and smooth animations

## Tech Stack

- **React 18** - UI framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Framer Motion** - Animations
- **Vite** - Build tool
- **GitHub Pages** - Hosting

## Getting Started

### Prerequisites

- Node.js 18+ and npm/pnpm installed

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/kdp-tiktok-accelerator.git
cd kdp-tiktok-accelerator
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

The site will be available at `http://localhost:5173`

## Building for Production

```bash
npm run build
```

This creates an optimized build in the `dist/` folder.

## Deployment to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository named `kdp-tiktok-accelerator`
2. Clone this project into that repository

### Step 2: Push to GitHub

```bash
git remote add origin https://github.com/yourusername/kdp-tiktok-accelerator.git
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository settings
2. Navigate to **Pages** section
3. Under "Build and deployment":
   - Source: Select "GitHub Actions"
   - The workflow file (`.github/workflows/deploy.yml`) will automatically deploy your site

### Step 4: Configure Custom Domain

1. In your repository settings, go to **Pages**
2. Under "Custom domain", enter `kdptiktok.com`
3. Update your domain's DNS settings to point to GitHub Pages:
   - Add an `A` record pointing to GitHub's IP addresses
   - Or add a `CNAME` record pointing to `yourusername.github.io`

GitHub will automatically create a `CNAME` file in your repository.

## Project Structure

```
src/
├── components/
│   ├── Navbar.tsx           # Navigation bar
│   ├── HeroSection.tsx       # Hero section with CTA
│   ├── TrendDashboard.tsx    # Trending niches table
│   ├── ScriptGenerator.tsx   # AI script generator
│   ├── Blueprint.tsx         # Features and testimonials
│   ├── Resources.tsx         # Recommended tools
│   └── Footer.tsx            # Footer with disclaimer
├── pages/
│   └── Index.tsx             # Main page layout
├── App.tsx                   # App component
├── main.tsx                  # Entry point
└── index.css                 # Global styles
```

## Customization

### Update Content

- **Trending Niches**: Edit `src/components/TrendDashboard.tsx` - modify the `niches` array
- **Script Templates**: Edit `src/components/ScriptGenerator.tsx` - modify the `hookTemplates` array
- **Resources**: Edit `src/components/Resources.tsx` - modify the `resources` array
- **Contact Info**: Edit `src/components/Footer.tsx` - update email and website

### Styling

The site uses Tailwind CSS with custom CSS variables for theming. Modify `src/index.css` to change colors:

```css
:root {
  --background: 222 84% 5%;
  --foreground: 210 40% 96%;
  --primary: 280 85% 60%;
  --accent: 0 100% 50%;
  /* ... other colors ... */
}
```

## Legal Disclaimer

This website is an independent resource and is NOT affiliated, associated, authorized, endorsed by, or in any way officially connected with TikTok, ByteDance, Amazon.com, or any of their subsidiaries or affiliates. All trademarks are the property of their respective owners.

## License

MIT License - feel free to use this project for your own purposes.

## Support

For issues or questions, please open an issue on GitHub or contact us at kdptiktokmastery@gmail.com

## Changelog

### v1.0.0 (Initial Release)
- Initial project setup
- All core components implemented
- GitHub Pages deployment configured
- Custom domain support
