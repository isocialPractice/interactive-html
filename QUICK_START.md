# Quick Start Guide: Using the Template System

## For Users

### Navigation
- **Fixed Top Menu**: Always visible at the top of every page
- **Dropdown Categories**: Hover over category names to see tool list
- **Mobile Menu**: Tap the ☰ icon on small screens
- **Home Button**: Click the logo or 🏠 Home to return to the landing page

### Keyboard Shortcuts (Recommended Addition)
- `Escape`: Close dropdown menus
- `Tab`: Navigate through menu items
- `/`: Focus search box (on index.html)

## For Developers

### Adding a New Tool Page

1. **Copy an existing HTML file** as a template:
   ```bash
   cp electronics-ohms-law-calculator.html new-tool.html
   ```

2. **Update the head section** (between `<!-- InstanceBeginEditable name="head" -->` tags):
   ```html
   <title>Your New Tool Name</title>
   <style>
       /* Your page-specific styles */
   </style>
   ```

3. **Update the page content** (between `<!-- InstanceBeginEditable name="page" -->` tags):
   ```html
   <div class="container">
       <!-- Your tool HTML -->
   </div>
   ```

4. **Add to navigation**:
   - Edit `Templates/page.html` and add your new tool link
   - Run `html-dwt-cmd update-all Templates/page.html --auto-apply`
   - All 15+ pages will be updated automatically

5. **Link the template** (if creating from scratch):
   - Add `<!-- InstanceBegin template="/Templates/page.html" -->` at the top
   - Add `<!-- InstanceEnd -->` at the bottom

### Modifying Global Styles

Edit `style.css` to change:
- **Colors**: Update CSS variables at the top (`:root` section)
- **Typography**: Modify font-family, sizes, weights
- **Navigation**: Change `.site-nav` and related classes
- **Components**: Update button, input, card styles

### Customizing Per-Page Styles

Add styles in the `<!-- InstanceBeginEditable name="head" -->` section:
```html
<style>
    /* Override global styles for this page only */
    .container {
        max-width: 1200px; /* Wider container for this page */
    }
</style>
```

### Updating the Navigation Menu

#### Option 1: Using html-dwt-cmd (Recommended)

The easiest way to update navigation across all pages:

1. **Install html-dwt-cmd** (one-time setup):
   ```bash
   git clone https://github.com/isocialPractice/html-dwt-cmd-template.git
   cd html-dwt-cmd-template
   npm install
   npm run compile
   npm link  # Makes command available globally
   ```

2. **Edit the master template** (`Templates/page.html`):
   - Modify the navigation menu HTML
   - Change links, add/remove items, update text

3. **Update all pages automatically**:
   ```bash
   html-dwt-cmd update-all Templates/page.html --auto-apply
   ```

This will update all 15+ HTML files in seconds, preserving each page's unique content.

#### Option 2: Manual Editing

To add/remove/modify menu items manually, update this section in each HTML file:
```html
<nav class="site-nav">
    <div class="nav-container">
        <!-- Menu structure -->
    </div>
</nav>
```

**Note**: Manual editing is tedious for 15+ files. Use html-dwt-cmd instead.

### Color Usage Guidelines

| Element | Color Variable | Hex Code |
|---------|---------------|----------|
| Primary buttons, links | `--color-primary` | #0066CC |
| Headings, dark text | `--color-primary-dark` | #004080 |
| Success states | `--color-secondary` | #00A86B |
| Warning/accent | `--color-accent` | #FF6B35 |
| Highlights, info boxes | `--color-primary-light` | #E6F2FF |
| Body text | `--color-text` | #1A1A1A |
| Secondary text | `--color-text-secondary` | #6C757D |

### Component Classes

| Class | Purpose | Example |
|-------|---------|---------|
| `.container` | Main content wrapper | Centered, max-width, padded |
| `.controls` | Input group grid | Responsive columns |
| `.control-group` | Individual input section | Background, border, padding |
| `.results` | Output display area | Highlighted background |
| `.info-box` | Information callout | Left border, background |
| `.btn` | Button styling | Primary color, hover effect |

### Responsive Breakpoints

```css
/* Mobile: < 768px */
@media (max-width: 768px) {
    /* Mobile-specific styles */
}

/* Tablet: 768px - 1024px */
@media (min-width: 768px) and (max-width: 1024px) {
    /* Tablet-specific styles */
}

/* Desktop: > 1024px */
@media (min-width: 1024px) {
    /* Desktop-specific styles */
}
```

## Testing Checklist

Before deploying changes:

- [ ] Test on Chrome, Firefox, Safari, Edge
- [ ] Test on mobile device (or browser dev tools)
- [ ] Verify all navigation links work
- [ ] Check that favicon appears
- [ ] Validate HTML (W3C validator)
- [ ] Test keyboard navigation
- [ ] Verify dropdown menus work on hover
- [ ] Check mobile menu toggle button
- [ ] Test with different screen sizes
- [ ] Verify no console errors

## Common Issues & Solutions

### Navigation menu not showing
**Problem**: CSS not loading
**Solution**: Check that `<link rel="stylesheet" href="style.css">` is in the `<head>`

### Favicon not appearing
**Problem**: Incorrect path or browser cache
**Solution**: Hard refresh (Ctrl+Shift+R) or clear browser cache

### Dropdown menus not working
**Problem**: CSS hover state not applying
**Solution**: Check that `.nav-dropdown:hover .dropdown-menu` rule exists in style.css

### Mobile menu toggle not working
**Problem**: JavaScript onclick not executing
**Solution**: Verify the onclick handler is correct: `onclick="document.querySelector('.nav-menu').classList.toggle('active')"`

### Styles look different on mobile
**Problem**: Missing viewport meta tag
**Solution**: Ensure `<meta name="viewport" content="width=device-width, initial-scale=1.0">` is present

## Deployment

### GitHub Pages
1. Push all files to your repository
2. Go to Settings → Pages
3. Select branch (usually `main`) and root directory
4. Save and wait for deployment
5. Access at: `https://username.github.io/repository-name/`

### Local Testing
```bash
# Simple HTTP server (Python 3)
python -m http.server 8000

# Access at http://localhost:8000
```

### Performance Optimization
- CSS is already minified-ready (remove comments and whitespace)
- SVG favicon is vector (scales perfectly, tiny file size)
- No external dependencies (faster loading)
- Single CSS file (one HTTP request)

## Maintenance Schedule

### Weekly
- Check for broken links
- Test on latest browser versions

### Monthly
- Review analytics for popular tools
- Consider UX improvements based on usage
- Update README with any new tools

### Quarterly
- Review and update color schemes if needed
- Audit accessibility compliance
- Update documentation

---

**Need Help?** Check the `TEMPLATE_IMPLEMENTATION.md` file for full technical details.
