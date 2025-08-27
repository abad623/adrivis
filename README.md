# Adrivis - AI-Powered Business Intelligence

A professional landing page for Adrivis, an AI-powered business intelligence platform that transforms complex e-commerce data into clear, actionable insights delivered via weekly email reports.

## 🚀 Features

- **Vivid, Modern Design**: Eye-catching color palette with professional gradients and animations
- **Realistic Email Report Mockup**: Detailed preview showing AI insights, revenue tracking, and competitor analysis
- **Professional Email Collection**: Integrated with ConvertKit, Formspree, and Zoho Forms options
- **Social Proof & Credibility**: Testimonials, statistics, and trust indicators
- **Engaging Visual Elements**: Custom SVG icons and interactive hover effects
- **Responsive Layout**: Optimized for all devices (desktop, tablet, mobile)
- **GitHub Pages Ready**: Static site optimized for GitHub Pages hosting
- **SEO Optimized**: Proper meta tags and semantic HTML structure

## 🛠️ Technology Stack

- **HTML5**: Semantic markup with accessibility in mind
- **CSS3**: Modern styling with CSS Grid, Flexbox, and animations
- **Vanilla JavaScript**: Form validation and interactive features
- **Google Fonts**: Inter font family for professional typography

## 📁 Project Structure

```
adrivis/
├── index.html          # Main landing page
├── styles.css          # All CSS styles and responsive design
├── script.js           # JavaScript functionality
└── README.md           # Project documentation
```

## 🎨 Design Features

- **Hero Section**: Compelling headline with vivid gradients and realistic email report preview
- **Email Report Mockup**: Detailed screenshot showing revenue, best sellers, AI insights, and competitor analysis
- **Value Proposition**: Clear explanation of benefits with custom SVG icons and engaging animations
- **Social Proof Section**: Customer testimonials, statistics, and trust indicators on dark background
- **How It Works**: Step-by-step process visualization with gradient icons
- **Professional Forms**: Multiple email collection options (ConvertKit, Formspree, Zoho)
- **Vivid Color Palette**: Modern blue, purple, and cyan gradients throughout
- **Responsive Design**: Mobile-first approach with breakpoints
- **Advanced Animations**: 3D transforms, hover effects, and smooth transitions

## 🚀 Deployment to GitHub Pages

1. **Create a new repository** on GitHub named `adrivis` (or your preferred name)

2. **Push your code** to the repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Adrivis landing page"
   git branch -M main
   git remote add origin https://github.com/yourusername/adrivis.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to your repository settings
   - Scroll down to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

4. **Access your site** at: `https://yourusername.github.io/adrivis`

## 📧 Form Data Collection

The current implementation shows a success modal when users submit the waitlist form. To collect actual data, you'll need to:

1. **Set up a backend service** (e.g., Netlify Forms, Formspree, or custom API)
2. **Update the form submission** in `script.js` to send data to your endpoint
3. **Configure email notifications** to receive new signups

### Example backend integration:

```javascript
// Replace the setTimeout in handleFormSubmit with:
fetch('/api/waitlist', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify(data)
})
.then(response => response.json())
.then(result => {
    showSuccessMessage(data);
})
.catch(error => {
    console.error('Error:', error);
    showErrorMessage();
});
```

## 🎯 Key Messaging

The landing page incorporates your suggested messaging:

- **"Your data. Decoded by AI."** - Main hero headline
- **"Turn complex business metrics into simple, actionable insights"** - Hero subtitle
- **"Tired of confusing dashboards?"** - Problem statement
- **"Early Access • Limited Spots Available"** - Urgency/exclusivity
- **"Join the waitlist and be the first to try Adrivis"** - Clear call-to-action

## 🔧 Customization

### Colors
The design uses a professional color palette:
- Primary: `#6366f1` (Indigo)
- Secondary: `#8b5cf6` (Purple)
- Text: `#1f2937` (Dark Gray)
- Background: `#ffffff` (White)

### Fonts
- Primary font: Inter (Google Fonts)
- Fallbacks: System fonts for performance

### Logo
The SVG logo is embedded inline and can be easily customized by modifying the SVG code in `index.html`.

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📈 Performance

- Optimized images and assets
- Minimal external dependencies
- Efficient CSS and JavaScript
- Fast loading times

## 🤝 Contributing

This is a static landing page project. To make changes:

1. Edit the HTML, CSS, or JavaScript files
2. Test locally by opening `index.html` in a browser
3. Commit and push changes to update the live site

## 📄 License

This project is for Adrivis business use. All rights reserved.

---

**Adrivis** - Transforming business data into actionable insights with AI.
