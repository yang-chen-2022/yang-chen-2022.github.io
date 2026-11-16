# Yang Chen | Materials and Structures Research

A responsive, modern research-group website built with HTML, CSS, and JavaScript. Deployed using GitHub Pages with no build step or external dependencies.

## Website Structure

The homepage includes:

1. **Navigation Header** - Large, easy-to-find menu at the top with links to main sections
2. **Banner Image** - Full-width banner section at the top of the page
3. **Overview Section** - Side-by-side image and descriptive text about your research
4. **Research Highlights** - Dynamic carousel/slider with left/right navigation and clickable slides
5. **Research Areas** - Grid of research topics (3 columns)
6. **News & Updates** - Latest news and announcements (3-column grid)
7. **Contact Section** - Call-to-action with link to research profile
8. **Footer** - Navigation back to top and site credits

## How to Edit and Customize

### Editing Content

1. **Edit the main file**: Open `index.html` in any text editor
2. **Make your changes**: Update text, links, and content
3. **Save the file**: The changes will be reflected when you push to GitHub

### Common Edits

#### Change Banner Image
In `index.html`, find the `.banner` section and replace the banner background:

```html
<section class="banner" id="top" aria-labelledby="banner-title">
```

Edit the CSS in `styles.css` to use your own banner image:

```css
.banner {
  background-image: url('path/to/your/banner-image.jpg');
  background-size: cover;
  background-position: center;
}
```

#### Replace Placeholder Images
Find lines like this in `index.html`:

```html
<img src="https://via.placeholder.com/500x300?text=Research+Overview" alt="Research overview placeholder">
```

Replace with your own image URL:

```html
<img src="path/to/your-image.jpg" alt="Description of image">
```

#### Add or Edit Research Highlights
Research highlights are in the `.research-highlights` section. Each slide is a `.slide` div:

```html
<div class="slide">
  <div class="slide-image">
    <img src="path/to/image.jpg" alt="Your research">
  </div>
  <div class="slide-content">
    <h3>Your Research Title</h3>
    <p>Your research description.</p>
    <a href="detail-page.html" class="slide-link">View Details →</a>
  </div>
</div>
```

Add more slides by copying the entire `<div class="slide">` block and updating the content. The slider automatically handles navigation with dots for each slide.

#### Edit News Items
News items are in the `.news-grid` section. Each news card has this structure:

```html
<article class="news-card">
  <div class="news-date">Nov 2024</div>
  <h3>Your News Title</h3>
  <p>Your news description.</p>
  <a href="news-link.html" class="read-more">Read More →</a>
</article>
```

Add more news by copying this entire block and updating dates, titles, and descriptions.

#### Update Navigation Menu
Edit the menu links in the header:

```html
<nav class="site-nav" aria-label="Main navigation">
  <a href="#overview">Home</a>
  <a href="#research">Research</a>
  <a href="#highlights">Highlights</a>
  <a href="#news">News</a>
  <a href="#contact">Contact</a>
</nav>
```

### Styling and Colors

All colors and styling are in `styles.css`. Key CSS classes:

- `.site-header` - Header styling and navigation
- `.banner` - Banner section styling
- `.overview` - Overview section styling
- `.research-highlights` - Research highlights slider
- `.news-grid` - News section styling
- `.button` - Button styling

Main color used: `#075b8d` (blue). To change the color scheme globally, search and replace this color code in `styles.css`.

### Responsive Design

The website is fully responsive and works on:
- Desktop (1024px and above)
- Tablet (760px - 1023px)
- Mobile (under 520px)

Responsive breakpoints are at the bottom of `styles.css`:

```css
@media (max-width: 1024px) { ... }
@media (max-width: 760px) { ... }
@media (max-width: 520px) { ... }
```

### Adding New Sections

To add a new section:

1. Add HTML in `index.html` inside the `<main>` tag:

```html
<section id="my-section">
  <div class="container">
    <h2>My Section Title</h2>
    <!-- Your content here -->
  </div>
</section>
```

2. Add CSS styling in `styles.css` for `.my-section` class
3. Add a navigation link in the header to point to `#my-section`

### Slider Functionality

The research highlights slider is powered by `slider.js`. It automatically:
- Rotates slides every 6 seconds
- Allows navigation with left/right buttons
- Allows clicking dots to jump to a specific slide
- Shows/hides slides smoothly with fade animation

No configuration needed - just edit the slide content in `index.html`.

## Publish the Site

1. In the repository, go to **Settings → Pages**
2. Under **Build and deployment**, choose **GitHub Actions** as the source
3. The workflow deploys on each push to `main`
4. Once deployed, the site is available at `https://yang-chen-2022.github.io`

## File Structure

```
.
├── index.html          # Main page - edit content here
├── styles.css          # All styling - edit colors/layout here
├── slider.js           # Slider functionality - usually no edits needed
└── README.md          # This file
```

## Tips

- **Use placeholder images**: Replace `https://via.placeholder.com/...` URLs with your own images or image hosting service (e.g., Imgur, your server)
- **Keep file names consistent**: If you add images, keep them in the same folder or note the correct path in `index.html`
- **Backup before major changes**: Git tracks changes automatically, so you can always revert if something breaks
- **Test locally**: Open `index.html` in your browser to preview changes before pushing to GitHub
- **Mobile first**: Always check how changes look on mobile phones using your browser's responsive design tool

## Support

For more information on HTML, CSS, and JavaScript:
- [MDN Web Docs](https://developer.mozilla.org/)
- [CSS-Tricks](https://css-tricks.com/)
- [W3Schools](https://www.w3schools.com/)

