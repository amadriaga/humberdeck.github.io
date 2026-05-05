# Humberdeck Website

A modern, responsive website for humberdeck.com built with HTML, CSS, and JavaScript, optimized for Cloudflare Pages.

## 🚀 Features

- **Responsive Design** - Works perfectly on desktop, tablet, and mobile
- **Fast Loading** - Optimized for performance
- **Modern UI** - Clean and professional design
- **Contact Form** - Ready for Email Worker integration
- **SEO Friendly** - Proper meta tags and semantic HTML
- **Security Headers** - Pre-configured security headers for Cloudflare Pages

## 📁 Project Structure

```
humberdeck/
├── index.html          # Homepage
├── about.html          # About page
├── contact.html        # Contact page with form
├── styles.css          # All styles
├── script.js           # JavaScript functionality
├── _headers            # Cloudflare Pages security headers
└── README.md           # This file
```

## 🌐 Deployment to Cloudflare Pages

### Option 1: Git Integration (Recommended)

1. **Create a Git repository:**
   ```powershell
   cd humberdeck
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. **Push to GitHub/GitLab:**
   ```powershell
   git remote add origin https://github.com/yourusername/humberdeck.git
   git push -u origin main
   ```

3. **Deploy on Cloudflare Pages:**
   - Go to [Cloudflare Dashboard](https://dash.cloudflare.com)
   - Navigate to **Pages**
   - Click **Create a project** → **Connect to Git**
   - Select your repository
   - Configure build settings:
     - **Build command:** (leave empty)
     - **Build output directory:** /
   - Click **Save and Deploy**

4. **Configure custom domain:**
   - In Pages project settings, go to **Custom domains**
   - Add **humberdeck.com** and **www.humberdeck.com**
   - Cloudflare will automatically configure DNS

### Option 2: Direct Upload

1. Go to Cloudflare Pages
2. Click **Create a project** → **Direct Upload**
3. Upload all files from the humberdeck folder
4. Configure custom domain as above

## 📧 Email Integration

The contact form is ready but needs an Email Worker to function:

1. **Set up Email Routing** (see `../email-setup-guide.md`)
2. **Deploy Email Worker** (see `../email-worker-example.js`)
3. **Update script.js** with your Email Worker URL:
   ```javascript
   const response = await fetch('https://email.humberdeck.com', {
   ```

## 🎨 Customization

### Colors
Edit CSS variables in `styles.css`:
```css
:root {
    --primary-color: #3b82f6;
    --secondary-color: #10b981;
    /* ... */
}
```

### Content
- Edit HTML files directly for page content
- Update navigation links in each HTML file's `<nav>` section
- Modify footer information in each page

### Pages
To add new pages:
1. Copy an existing HTML file
2. Update content
3. Add link to navigation in all pages

## 🔒 Security

Security headers are automatically applied via `_headers` file:
- X-Frame-Options: DENY
- X-Content-Type-Options: nosniff
- Content Security Policy
- And more...

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 🛠️ Local Development

Simply open `index.html` in your browser, or use a local server:

```powershell
# Using Python
python -m http.server 8000

# Using Node.js http-server
npx http-server
```

Then visit `http://localhost:8000`

## 📝 To-Do

- [ ] Deploy to Cloudflare Pages
- [ ] Configure custom domain (humberdeck.com)
- [ ] Set up Email Routing
- [ ] Deploy Email Worker for contact form
- [ ] Add favicon
- [ ] Add social media links
- [ ] Set up analytics (optional)
- [ ] Add blog section (optional)

## 📄 License

© 2026 Humberdeck. All rights reserved.

## 🤝 Support

For questions or issues, email: contact@humberdeck.com
