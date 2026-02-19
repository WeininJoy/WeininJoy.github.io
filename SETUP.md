# Setup Guide for Your Academic Portfolio Website

This is a clean, minimalist academic portfolio website ready for deployment on GitHub Pages.

## Quick Start

### 1. Personalize Your Content

Edit `index.html` and replace the following placeholders:

- **Line 4**: Change "Your Name - Academic Portfolio" to your actual name
- **Lines 28-30**: Update your name, title, and affiliation
- **Line 50**: Update your research interests
- **Lines 54-76**: Add your actual publications
- **Lines 80-102**: Add your projects
- **Lines 108-110**: Add your contact information
- **Line 124**: Update the copyright year and name

### 2. Add Your Profile Picture

Replace `images/profile.jpg` with your own profile photo. Recommended specs:
- Square image (e.g., 500x500px or larger)
- JPG or PNG format
- Good quality headshot

### 3. Update Social Links

Edit `index.html` lines 119-122 to add your social media profiles:
- Twitter/X
- GitHub
- LinkedIn
- Email

Replace `#` with your actual profile URLs.

### 4. Deploy to GitHub Pages

#### Option A: Create a new repository

1. Create a new repository on GitHub named `username.github.io` (replace `username` with your GitHub username)
2. Initialize git in this directory:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Academic portfolio website"
   git branch -M main
   git remote add origin https://github.com/username/username.github.io.git
   git push -u origin main
   ```
3. Your site will be live at `https://username.github.io`

#### Option B: Use a project repository

1. Create a new repository on GitHub with any name (e.g., `portfolio`)
2. Initialize git and push:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Academic portfolio website"
   git branch -M main
   git remote add origin https://github.com/username/portfolio.git
   git push -u origin main
   ```
3. Go to Settings → Pages → Source → Select "main" branch
4. Your site will be live at `https://username.github.io/portfolio`

## Customization

### Colors

Edit `assets/css/portfolio.css` to change colors:
- Line 97: Navigation hover color
- Line 161: Section heading border color
- Line 191, 211, 225: Link colors

### Fonts

The site uses system fonts for optimal performance. To use custom fonts:
1. Add Google Fonts import at the top of `portfolio.css`
2. Update the `font-family` on line 17

### Layout

The maximum content width is set to 800px (line 23 of `portfolio.css`). Adjust this for a wider or narrower layout.

## File Structure

```
├── index.html              # Main HTML file
├── assets/
│   ├── css/
│   │   ├── main.css       # Original template CSS (still loaded for icons)
│   │   └── portfolio.css  # Your custom academic portfolio CSS
│   └── js/                # JavaScript files
├── images/
│   └── profile.jpg        # Your profile picture
└── SETUP.md              # This file
```

## Tips

- Keep your content concise and professional
- Update publications regularly
- Use high-quality images
- Test your site locally by opening `index.html` in a browser
- Check mobile responsiveness

## Credits

- Template: HTML5 UP Arcana (modified)
- Icons: Font Awesome
- Design: Custom academic portfolio layout

## Need Help?

- GitHub Pages documentation: https://pages.github.com/
- Font Awesome icons: https://fontawesome.com/icons
- Markdown guide for additional pages: https://www.markdownguide.org/
