# Personal Portfolio Website

A modern, responsive portfolio website built with HTML, CSS, and JavaScript. Showcase your skills, projects, and experience with a clean, professional design.

## Features

- ✨ **Modern Design**: Clean, professional layout with smooth animations
- 📱 **Fully Responsive**: Looks great on desktop, tablet, and mobile devices
- 🔗 **GitHub Integration**: Automatically displays your GitHub repositories
- 📝 **Contact Form**: Functional contact form with validation
- 🎨 **Customizable**: Easy to customize colors, content, and styling
- ⚡ **Fast & Lightweight**: No heavy frameworks, pure vanilla JavaScript
- 🌐 **SEO Friendly**: Semantic HTML structure

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- A text editor (VS Code, Sublime Text, etc.)
- A GitHub account (optional, for project showcase)

### Installation

1. **Clone or download this repository**
   ```bash
   git clone <your-repo-url>
   cd portfolio-website
   ```

2. **Open the project**
   - Simply open `index.html` in your web browser, or
   - Use a local development server (recommended)

3. **Using a Local Development Server**

   **Option 1: Python**
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   ```

   **Option 2: Node.js (using http-server)**
   ```bash
   npx http-server -p 8000
   ```

   **Option 3: VS Code Live Server Extension**
   - Install the "Live Server" extension
   - Right-click on `index.html` and select "Open with Live Server"

4. **Access your site**
   - Open your browser and navigate to `http://localhost:8000`

## Customization

### 1. Update Personal Information

**In `index.html`:**
- Replace "Your Name" with your actual name
- Update the hero subtitle and description
- Modify the About Me section with your background
- Update contact information (email, phone, location)
- Replace social media links with your profiles

**Example:**
```html
<h1 class="hero-title">Hi, I'm <span class="highlight">John Doe</span></h1>
<p class="hero-subtitle">Full Stack Developer & Creative Problem Solver</p>
```

### 2. Configure GitHub Integration

**In `script.js`:**
- Find the `GITHUB_USERNAME` constant at the top
- Replace `'yourusername'` with your actual GitHub username

```javascript
const GITHUB_USERNAME = 'yourusername'; // Change this!
```

The website will automatically fetch and display your 6 most recently updated public repositories.

### 3. Customize Colors

**In `styles.css`:**
- Modify the CSS variables in the `:root` selector

```css
:root {
    --primary-color: #2563eb;      /* Main brand color */
    --primary-dark: #1e40af;       /* Darker shade */
    --secondary-color: #64748b;     /* Secondary color */
    --background-color: #ffffff;    /* Main background */
    --text-color: #1e293b;          /* Main text color */
    /* ... more variables */
}
```

### 4. Update Skills Section

**In `index.html`:**
- Modify the skills grid in the About section
- Add or remove skill items as needed

```html
<div class="skill-item">
    <i class="fab fa-react"></i>
    <span>React</span>
</div>
```

### 5. Customize Blog Posts

**In `index.html`:**
- Update the blog section with your actual blog posts
- Replace placeholder content with real articles
- Add links to your blog posts

### 6. Set Up Contact Form Backend

Currently, the contact form shows a success message but doesn't actually send emails. To make it functional:

**Option 1: Use a Form Service**
- [Formspree](https://formspree.io/) - Free tier available
- [EmailJS](https://www.emailjs.com/) - Send emails directly from JavaScript
- [Netlify Forms](https://www.netlify.com/products/forms/) - If hosting on Netlify

**Option 2: Create Your Own Backend**
- Set up a server endpoint (Node.js, Python, PHP, etc.)
- Update the fetch call in `script.js` to point to your endpoint

**Example with EmailJS:**
```javascript
// Install: npm install @emailjs/browser
import emailjs from '@emailjs/browser';

// In form submission handler:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', formData, 'YOUR_PUBLIC_KEY')
    .then(() => {
        showFormMessage('Message sent successfully!', 'success');
    });
```

## File Structure

```
portfolio-website/
│
├── index.html          # Main HTML file
├── styles.css          # All styling and responsive design
├── script.js           # JavaScript functionality
└── README.md          # This file
```

## Deployment

### Option 1: GitHub Pages (Free)

1. Push your code to a GitHub repository
2. Go to repository Settings → Pages
3. Select the branch (usually `main` or `master`)
4. Your site will be available at `https://yourusername.github.io/repository-name`

### Option 2: Netlify (Free)

1. Sign up at [Netlify](https://www.netlify.com/)
2. Drag and drop your project folder, or
3. Connect your GitHub repository for automatic deployments

### Option 3: Vercel (Free)

1. Sign up at [Vercel](https://vercel.com/)
2. Import your GitHub repository
3. Deploy with one click

### Option 4: Traditional Web Hosting

- Upload all files via FTP to your web hosting provider
- Ensure `index.html` is in the root directory

## Learning Resources

### HTML & CSS

1. **MDN Web Docs** - [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) & [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
   - Comprehensive, official documentation
   - Great for reference and learning

2. **freeCodeCamp** - [Responsive Web Design](https://www.freecodecamp.org/learn/2022/responsive-web-design/)
   - Free, interactive courses
   - Hands-on projects

3. **CSS-Tricks** - [CSS-Tricks.com](https://css-tricks.com/)
   - Tutorials, guides, and articles
   - Great for learning modern CSS techniques

4. **W3Schools** - [HTML Tutorial](https://www.w3schools.com/html/) & [CSS Tutorial](https://www.w3schools.com/css/)
   - Beginner-friendly
   - Interactive examples

### JavaScript

1. **MDN Web Docs** - [JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
   - Complete JavaScript reference
   - Best practices and examples

2. **JavaScript.info** - [javascript.info](https://javascript.info/)
   - Modern JavaScript tutorial
   - From basics to advanced topics

3. **freeCodeCamp** - [JavaScript Algorithms and Data Structures](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/)
   - Free, comprehensive course
   - Practice with projects

4. **Eloquent JavaScript** - [eloquentjavascript.net](https://eloquentjavascript.net/)
   - Free online book
   - Deep dive into JavaScript concepts

### Responsive Design

1. **A List Apart** - [Responsive Web Design](https://alistapart.com/article/responsive-web-design/)
   - Original article on responsive design
   - Foundational concepts

2. **CSS Grid Guide** - [css-tricks.com/snippets/css/complete-guide-grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
   - Complete guide to CSS Grid
   - Essential for modern layouts

3. **Flexbox Guide** - [css-tricks.com/snippets/css/a-guide-to-flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
   - Complete guide to Flexbox
   - Perfect for component layouts

### GitHub & Version Control

1. **GitHub Guides** - [guides.github.com](https://guides.github.com/)
   - Official GitHub tutorials
   - Learn Git and GitHub basics

2. **Atlassian Git Tutorial** - [atlassian.com/git/tutorials](https://www.atlassian.com/git/tutorials)
   - Comprehensive Git tutorial
   - From beginner to advanced

### Web APIs

1. **MDN Web APIs** - [developer.mozilla.org/en-US/docs/Web/API](https://developer.mozilla.org/en-US/docs/Web/API)
   - Documentation for all web APIs
   - Including Fetch API for GitHub integration

2. **GitHub REST API** - [docs.github.com/en/rest](https://docs.github.com/en/rest)
   - Official GitHub API documentation
   - Learn how to fetch repository data

### Design & UX

1. **Canva Design School** - [canva.com/designschool](https://www.canva.com/designschool/)
   - Free design tutorials
   - Learn design principles

2. **Google Material Design** - [material.io/design](https://material.io/design)
   - Design system and guidelines
   - Modern UI/UX principles

### Additional Tools & Resources

1. **Font Awesome** - [fontawesome.com](https://fontawesome.com/)
   - Icon library (already included in this project)
   - Free icons for your projects

2. **Google Fonts** - [fonts.google.com](https://fonts.google.com/)
   - Free web fonts
   - Easy to integrate

3. **Color Palette Generators**
   - [Coolors.co](https://coolors.co/)
   - [Adobe Color](https://color.adobe.com/)

4. **Code Editors**
   - [VS Code](https://code.visualstudio.com/) - Recommended
   - [Sublime Text](https://www.sublimetext.com/)
   - [Atom](https://atom.io/)

## Browser Support

This portfolio website works on all modern browsers:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Troubleshooting

### GitHub Projects Not Showing

1. Check that `GITHUB_USERNAME` is set correctly in `script.js`
2. Ensure your repositories are public
3. Check browser console for errors
4. Verify your internet connection

### Contact Form Not Working

- The form currently shows a success message but doesn't send emails
- See "Set Up Contact Form Backend" section above for solutions

### Styles Not Loading

- Ensure `styles.css` is in the same directory as `index.html`
- Check that the path in the HTML `<link>` tag is correct
- Clear your browser cache

### Mobile Menu Not Working

- Ensure `script.js` is loaded correctly
- Check browser console for JavaScript errors
- Verify that all IDs match between HTML and JavaScript

## Contributing

Feel free to fork this project and customize it for your own portfolio! If you make improvements that could benefit others, pull requests are welcome.

## License

This project is open source and available under the [MIT License](https://opensource.org/licenses/MIT).

## Support

If you have questions or need help:
1. Check the troubleshooting section above
2. Review the learning resources
3. Search for similar issues online
4. Ask in web development communities (Stack Overflow, Reddit r/webdev, etc.)

## Next Steps

1. ✅ Customize the content with your information
2. ✅ Set up GitHub integration
3. ✅ Configure contact form backend
4. ✅ Deploy your portfolio
5. ✅ Share it with the world!

---

**Happy Coding! 🚀**
