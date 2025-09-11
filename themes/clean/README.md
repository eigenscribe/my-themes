# Clean Theme

A minimal, reusable CSS theme with light/dark mode toggle functionality.

## Features

- **Theme Toggle**: Sun/moon switch in top-left corner
- **Background Switching**: Different background images for light/dark themes
- **Gradient Text**: Two utility classes for gradient text effects
- **Glassy Containers**: Glassmorphism effects with backdrop blur
- **Profile Layout**: Ready-to-use profile section with avatar and social links
- **Responsive Design**: Works on all screen sizes
- **Minimal Structure**: Clean, easy-to-understand CSS
- **Reusable**: Drop into any project

## Usage

1. Include `theme.css` in your HTML:
   ```html
   <link rel="stylesheet" href="theme.css">
   ```

2. Add the theme toggle switch:
   ```html
   <input type="checkbox" id="theme-switch" class="theme-switch__input">
   <label for="theme-switch" class="theme-switch__label">
       <span></span>
   </label>
   ```

3. Use the profile and projects structure:
   ```html
   <main>
       <div class="container centered">
           <header class="perfil">
               <img src="avatar.jpg" alt="Profile Avatar">
               <div class="title">
                   <h1 class="gradient_text1">Your Name</h1>
                   <h3>Your Title</h3>
                   <p>#your #tags</p>
                   <!-- Social icons here -->
               </div>
           </header>

           <main class="projetos">
               <div class="container-projetos">
                   <h4 class="gradient_text2">Projects</h4>
                   <p class="line-1">Your description</p>
                   <ol>
                       <li><a href="#">🎨 Project 1</a></li>
                       <li><a href="#">🌈 Project 2</a></li>
                   </ol>
               </div>
           </main>
       </div>
   </main>
   ```

## CSS Classes

### Gradient Text
- `.gradient_text1` - Blue to purple gradient
- `.gradient_text2` - Cyan to blue gradient

### Layout
- `.container` - Main container with max-width
- `.centered` - Centers content vertically and horizontally
- `.perfil` - Profile section with glassy effect
- `.container-projetos` - Projects section with glassy effect
- `.link-icon` - Social media icon styling

### Glassy Effects
All containers automatically have glassmorphism effects with:
- Semi-transparent backgrounds
- Backdrop blur filters
- Subtle borders and shadows

## Customization

### Colors
Modify the CSS variables in `:root` and `[data-theme="dark"]` to change colors:

```css
:root {
    --bg: white;
    --text: black;
    --gradDark: hsl(144, 100%, 89%);
    --gradLight: hsl(42, 94%, 76%);
    --bg-image: url(your-light-background.jpg);
}
```

### Background Images
Replace the background image URLs in the CSS variables:
- Light theme: `--bg-image` in `:root`
- Dark theme: `--bg-image` in `[data-theme="dark"]`

### Fonts
The theme uses Google Fonts. Modify the `@import` statement to change fonts:
```css
@import url('https://fonts.googleapis.com/css2?family=YourFont&display=swap');
```

## File Structure
```
themes/clean/
├── theme.css      # Main theme stylesheet
├── index.html     # Demo page
└── README.md      # This file
```