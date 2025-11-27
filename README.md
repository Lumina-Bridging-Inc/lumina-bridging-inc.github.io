# Lumina Bridging

Professional website for Lumina Bridging Inc., showcasing our healthcare AI and automation solutions.

## 🚀 Quick Start

This is a static website built with HTML, CSS, and JavaScript - no build process needed!

### Local Development

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Lumina-Bridging-Inc/lumina-bridging-inc.github.io.git
   cd lumina-bridging-inc.github.io
   ```

2. **View locally:**
   - Option A: Open `index.html` directly in your browser
   - Option B: Run a local server (Python):
     ```bash
     python -m http.server 8000
     # Visit http://localhost:8000
     ```

   - Option C: Run a local server (Node.js):
     ```bash
     npx http-server
     # Visit http://localhost:8080
     ```

## 📦 Project Structure

```
lumina-bridging-inc.github.io/
├── index.html              # Main website HTML
├── assets/
│   ├── style.css          # Styling (light/dark mode support)
│   ├── script.js          # Interactive features
│   └── images/            # Logo, screenshots (optional)
├── README.md              # This file
└── _config.yml            # Jekyll configuration (optional)
```

## 🌐 Deployment to GitHub Pages

### Option 1: Automatic (Recommended)

1. **Create/Push to GitHub**
   ```bash
   # If not already a git repo
   git init
   git add .
   git commit -m "Initial commit: Lumina Bridging website"
   git branch -M main
   git remote add origin https://github.com/Lumina-Bridging-Inc/lumina-bridging-inc.github.io.git
   git push -u origin main
   ```

2. **Enable GitHub Pages**
   - Go to your repository settings
   - Navigate to "Pages" section
   - Select "Deploy from a branch"
   - Choose `main` branch and `/root` directory
   - Click Save

3. **Your site will be live at:**
   ```
   https://lumina-bridging-inc.github.io
   ```

### Option 2: Manual Using GitHub CLI

```bash
# Install GitHub CLI if not already installed
# https://cli.github.com

gh repo create lumina-bridging-inc.github.io --public --source=. --remote=origin --push
```

### Option 3: Using GitHub Desktop

1. Clone or create the repository in GitHub Desktop
2. Make your changes locally
3. Commit and push to `main` branch
4. Enable GitHub Pages in repository settings

## 🎨 Features

- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Dark Mode Support**: Automatically adapts to user's system preference
- **Smooth Animations**: Fade-in effects and smooth scrolling
- **Fast Performance**: Lightweight, no external dependencies
- **Accessible**: Semantic HTML and WCAG-compliant
- **SEO Friendly**: Proper meta tags and structure

## 📝 Customization

### Update Content

Edit `index.html` to modify:
- Company name and description
- Solution details and features
- Project information and links
- Contact information
- Footer content

### Customize Styling

Edit `assets/style.css` to change:
- Color scheme (modify CSS variables in `:root`)
- Fonts and typography
- Spacing and layout
- Animations and transitions

### Modify Behavior

Edit `assets/script.js` to add:
- Custom analytics tracking
- Form validation
- Additional interactions
- Third-party integrations

## 🎯 Key Sections

### Hero Section
- Main headline and call-to-action buttons
- Gradient background for visual appeal

### About Section
- Company mission and values
- Foundation story

### Solutions Section
- Four main AI-powered solutions
- Solution type (pay-as-you-go vs subscription)
- Key features for each solution

### Features Section
- Six key differentiators
- Why organizations should choose Lumina Bridging

### Projects Section
- Featured open-source projects
- Technology tags
- Links to GitHub repositories

### Technology Stack Section
- AI & Machine Learning tools
- Backend & databases
- Frontend & UI technologies
- Security & compliance measures

### Contact Section
- GitHub organization link
- Contact information
- Call to action

## 🔧 Configuration

### Optional: Jekyll Configuration

If using Jekyll, update `_config.yml`:

```yaml
title: Lumina Bridging
description: Healthcare AI & Automation Solutions
url: https://lumina-bridging-inc.github.io
theme: null  # We're using custom CSS
```

### Optional: Custom Domain

1. Purchase a domain (e.g., luminabridging.com)
2. In repository settings > Pages, add custom domain
3. Update DNS records (see GitHub Pages documentation)

## 📱 Mobile Optimization

The site is fully responsive with breakpoints at:
- Desktop: 1200px+
- Tablet: 768px - 1199px
- Mobile: < 768px

Test on multiple devices:
- Chrome DevTools device emulation
- Physical devices
- BrowserStack for comprehensive testing

## ♿ Accessibility

Features include:
- Semantic HTML structure
- ARIA labels where needed
- Keyboard navigation support
- Color contrast compliance
- Screen reader friendly

## 📊 Analytics (Optional)

To add Google Analytics:

1. Create Google Analytics property
2. Get your Measurement ID
3. Add to `assets/script.js`:

```javascript
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR_MEASUREMENT_ID');
</script>
```

## 🚨 Troubleshooting

### Site not updating after push?
- Wait 1-2 minutes for GitHub Pages to rebuild
- Check Actions tab for build status
- Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)

### Styles not loading?
- Check that `assets/style.css` path is correct
- Verify file is committed and pushed to GitHub
- Inspect browser console for errors

### Links not working?
- Ensure all links are relative paths (e.g., `#about`, not `index.html#about`)
- Verify section IDs match link targets

## 📚 Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [HTML Best Practices](https://developer.mozilla.org/en-US/docs/Learn/HTML)
- [CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/)

## 📄 License

This website is the intellectual property of Lumina Bridging Inc.

## 🤝 Contributing

For contributions or issues:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📧 Contact

For inquiries about Lumina Bridging:
- Visit our [GitHub Organization](https://github.com/Lumina-Bridging-Inc)
- Check our [Projects](https://github.com/orgs/Lumina-Bridging-Inc/repositories)

---

**Lumina Bridging Inc.** - Healthcare AI & Automation Solutions
Built with ❤️ for healthcare innovation
