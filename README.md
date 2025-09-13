# RODI's BBQ Website

A modern, responsive website for RODI's BBQ business, designed to showcase premium smoked meats and services. Built for deployment on Azure Static Web Apps.

## 🍖 Features

- **Responsive Design**: Mobile-first approach optimized for all devices
- **BBQ-Themed Styling**: Warm color palette with reds, browns, and oranges
- **Photo Gallery**: Showcase your smoked meats with interactive gallery
- **Menu & Pricing**: Display your signature meats and pricing
- **Contact Form**: Allow customers to get in touch
- **Fast Loading**: Optimized for Azure Static Web Apps deployment

## 🎨 Design Highlights

- Modern CSS Grid and Flexbox layouts
- Smooth scroll animations and hover effects
- Mobile-responsive navigation
- BBQ-appropriate color scheme:
  - Primary Red: #C4161C
  - Burnt Orange: #CC5500
  - Golden Yellow: #DAA520
  - Warm Brown: #8B4513
  - Charcoal: #2F2F2F

## 📋 Current Menu & Pricing

- **Premium Brisket**: $22.50 per lb
- **Beef Back Ribs**: $40 per rack
- **Half Chicken**: $15 each

## 🚀 Deployment to Azure Static Web Apps

### Prerequisites
- Azure account
- GitHub repository
- Azure Static Web Apps resource

### Setup Steps

1. **Fork/Clone this repository** to your GitHub account

2. **Create Azure Static Web App**:
   - Go to [Azure Portal](https://portal.azure.com)
   - Create a new "Static Web App" resource
   - Connect to your GitHub repository
   - Set build configuration:
     - App location: `/`
     - Api location: (leave empty)
     - Output location: (leave empty)

3. **Configure GitHub Actions**:
   - Azure will automatically add the deployment workflow
   - The workflow file is already included in `.github/workflows/azure-static-web-apps.yml`
   - Add the `AZURE_STATIC_WEB_APPS_API_TOKEN` to your repository secrets

4. **Deploy**:
   - Push changes to the `main` branch
   - GitHub Actions will automatically build and deploy

### Manual Deployment
If you prefer manual deployment:
```bash
# Install Azure Static Web Apps CLI
npm install -g @azure/static-web-apps-cli

# Build and deploy
swa deploy
```

## 📸 Adding Your Photos

### Required Images
Replace the placeholder images in the `/images` directory:

1. **hero-bbq-bg.jpg** - Hero section background (1920x1080px)
2. **brisket-placeholder.jpg** - Brisket photo (800x600px)
3. **ribs-placeholder.jpg** - Beef ribs photo (800x600px)
4. **chicken-placeholder.jpg** - Half chicken photo (800x600px)
5. **gallery-1-placeholder.jpg** - Gallery image 1 (800x800px)
6. **gallery-2-placeholder.jpg** - Gallery image 2 (800x800px)
7. **gallery-3-placeholder.jpg** - Gallery image 3 (800x800px)
8. **gallery-4-placeholder.jpg** - Gallery image 4 (800x800px)

### Image Guidelines
- Use high-quality, well-lit photos
- Keep file sizes under 500KB for optimal performance
- Consider using WebP format for better compression
- Maintain consistent lighting and color temperature
- Focus on texture, color, and appetizing qualities

## 🛠️ Local Development

### Running Locally
1. Clone the repository:
```bash
git clone <your-repo-url>
cd rodis-bbq-website
```

2. Open with a local server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

3. Open `http://localhost:8000` in your browser

### File Structure
```
RODI's BBQ/
├── index.html              # Main website file
├── styles.css              # All styling and responsive design
├── script.js               # Interactive functionality
├── staticwebapp.config.json # Azure Static Web Apps configuration
├── images/                 # Photo directory
│   └── README.md          # Image guidelines
├── .github/
│   ├── copilot-instructions.md
│   └── workflows/
│       └── azure-static-web-apps.yml
└── README.md              # This file
```

## ✨ Customization

### Updating Content
- **Business Info**: Edit contact details in `index.html`
- **Pricing**: Update prices in the menu section
- **Services**: Modify the services section as needed
- **Colors**: Adjust the CSS custom properties in `styles.css`

### Adding New Menu Items
1. Add a new `.menu-item` div in the menu section
2. Include image, title, description, and price
3. Add corresponding image to `/images` directory

### Styling Changes
All styles are in `styles.css` with CSS custom properties for easy theming:
```css
:root {
    --primary-red: #C4161C;
    --burnt-orange: #CC5500;
    /* ... other variables */
}
```

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Android Chrome)

## 🔧 Performance Optimizations

- Optimized CSS with modern features
- Efficient JavaScript with intersection observers
- Lazy loading for images
- Proper caching headers configured
- Compressed and minified assets

## 📞 Contact & Support

For questions about this website template or Azure deployment:
- Check [Azure Static Web Apps documentation](https://docs.microsoft.com/azure/static-web-apps/)
- Review [GitHub Actions documentation](https://docs.github.com/actions)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

**Happy BBQing! 🔥**