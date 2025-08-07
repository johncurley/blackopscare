# Black Ops Support Services Website

A modern, professional Hugo website for Black Ops Support Services, featuring comprehensive support and care services.

## Features

- **Responsive Design**: Mobile-first approach with contemporary styling
- **Service Showcase**: Detailed sections for all service categories
- **Client Reviews**: Dedicated testimonials section
- **Contact Forms**: Netlify-integrated contact form
- **Performance Optimized**: Fast loading with modern web practices
- **SEO Ready**: Proper meta tags and structured content

## Site Structure

```
├── hugo.yaml                 # Hugo configuration
├── netlify.toml              # Netlify deployment settings
├── content/
│   └── _index.md            # Homepage content
├── layouts/
│   ├── _default/
│   │   └── baseof.html      # Base template
│   └── index.html           # Homepage template
└── assets/
    └── css/
        └── main.css         # Main stylesheet
```

## Services Featured

- **Aged Care Support**: 24/7 assistance, respite care, daily assistance
- **Cleaning Services**: Residential, commercial, carpet cleaning, bond cleaning
- **Gardening Services**: Lawn care, weeding, hedge trimming, weed killing
- **Personal Training**: Home or gym sessions with equipment provided
- **Support Services**: Transport, community access, meal preparation
- **Personal Care**: Light cleaning, meals, appointment assistance

## Quick Start

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) (v0.121.0 or later)
- [Git](https://git-scm.com/)

### Local Development

1. **Clone or create your project directory**
   ```bash
   mkdir black-ops-website
   cd black-ops-website
   ```

2. **Create the Hugo site structure**
   ```bash
   hugo new site . --force
   ```

3. **Add the provided files** to their respective directories:
   - Copy `hugo.yaml` to root
   - Copy `netlify.toml` to root
   - Copy `_index.md` to `content/`
   - Copy `baseof.html` to `layouts/_default/`
   - Copy `index.html` to `layouts/`
   - Copy `main.css` to `assets/css/`

4. **Start the development server**
   ```bash
   hugo server -D
   ```

5. **View the site** at `http://localhost:1313`

## Deployment to Netlify

### Method 1: Git Repository (Recommended)

1. **Push to GitHub/GitLab**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin <your-repo-url>
   git push -u origin main
   ```

2. **Connect to Netlify**
   - Go to [Netlify](https://netlify.com)
   - Click "New site from Git"
   - Connect your repository
   - Build settings are automatically detected from `netlify.toml`

### Method 2: Drag and Drop

1. **Build the site locally**
   ```bash
   hugo --gc --minify
   ```

2. **Upload the `public` folder** to Netlify's drag-and-drop interface

## Customization

### Colors and Branding

Edit the CSS variables in `assets/css/main.css`:

```css
:root {
    --primary-color: #2563eb;      /* Main brand color */
    --primary-dark: #1d4ed8;       /* Darker variant */
    --secondary-color: #64748b;     /* Secondary text */
    --accent-color: #f59e0b;        /* Accent highlights */
}
```

### Contact Information

Update contact details in `hugo.yaml`:

```yaml
params:
  phone: '0498 052 843'
  email: 'info@blackopssupportservices.com.au'
```

### Adding Images

1. Create a `static/images/` directory
2. Add your images (logos, service photos, team photos)
3. Update the templates to reference them:
   ```html
   <img src="/images/logo.png" alt="Black Ops Support Services">
   ```

### Reviews Section

The reviews are currently static. To make them dynamic:

1. Create `data/reviews.yaml`:
   ```yaml
   - name: "Sarah M."
     role: "Aged Care Client"
     rating: 5
     text: "The team at Black Ops has been absolutely wonderful..."
   ```

2. Update the reviews section in `layouts/index.html` to loop through the data.

### Services

Services are currently in the template. To make them more manageable:

1. Create `data/services.yaml`
2. Move service categories there
3. Update the template to use data files

## Performance Features

- **CSS Minification**: Automatic via Hugo pipes
- **Image Optimization**: Ready for Hugo's image processing
- **Lazy Loading**: Can be added to images
- **Caching Headers**: Configured in `netlify.toml`
- **Modern CSS**: Grid, Flexbox, CSS Variables
- **Mobile Performance**: Optimized responsive design

## SEO Features

- **Meta Tags**: Proper title, description, viewport
- **Semantic HTML**: Proper heading hierarchy
- **Structured Data**: Ready for JSON-LD implementation
- **Fast Loading**: Performance-optimized assets
- **Mobile Friendly**: Responsive design

## Form Handling

The contact form uses Netlify Forms for easy submission handling. After deployment:

1. Forms will appear in your Netlify dashboard
2. You can set up email notifications
3. Add spam protection if needed

## Next Steps

1. **Add Real Content**: Replace placeholder text with actual content
2. **Add Images**: Upload and integrate real photos and logos
3. **Test Contact Form**: Verify form submissions work
4. **Set Up Analytics**: Add Google Analytics or similar
5. **SEO Optimization**: Add meta descriptions, structured data
6. **Performance Testing**: Use tools like Lighthouse
7. **Accessibility**: Test with screen readers, check contrast

## Support

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Netlify Documentation](https://docs.netlify.com/)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

## License

This template is provided as-is for the Black Ops Support Services website.