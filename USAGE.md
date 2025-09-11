# My Themes - Usage Guide

This repository has been cleaned up and reorganized for easy reuse across projects.

## What Was Cleaned Up

### Removed Redundancy
- ❌ Complex build system with multiple CSS files
- ❌ Over-engineered gradient system (4+ variants → 2 simple ones)
- ❌ Math/equation specific styling
- ❌ Streamlit and framework-specific overrides
- ❌ Complex icon system
- ❌ Search functionality CSS
- ❌ Feature box components

### Simplified Structure
- ✅ Single CSS file per theme
- ✅ Clear, minimal HTML structure
- ✅ Two gradient text utility classes
- ✅ Theme toggle functionality
- ✅ Background image switching

## Current Structure

```
my-themes/
├── themes/
│   └── clean/              # Clean minimal theme
│       ├── theme.css       # Complete theme stylesheet
│       ├── index.html      # Demo/template
│       └── README.md       # Theme-specific docs
├── clean-theme.css         # Standalone version (root level)
├── clean-theme.html        # Standalone demo (root level)
└── USAGE.md               # This file
```

## How to Use in Your Projects

### Option 1: Copy Theme Files
1. Copy the entire `themes/clean/` folder to your project
2. Include `theme.css` in your HTML
3. Use the HTML structure from `index.html`

### Option 2: Use Standalone Files
1. Copy `clean-theme.css` and `clean-theme.html` to your project
2. Rename and modify as needed

### Option 3: Direct Link (for testing)
```html
<link rel="stylesheet" href="https://raw.githubusercontent.com/eigenscribe/my-themes/main/themes/clean/theme.css">
```

## Quick Start Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Project</title>
    <link rel="stylesheet" href="path/to/theme.css">
</head>
<body>
    <!-- Theme Toggle -->
    <input type="checkbox" id="theme-switch" class="theme-switch__input">
    <label for="theme-switch" class="theme-switch__label">
        <span></span>
    </label>
    
    <!-- Your Content -->
    <main>
        <div class="wrapper">
            <h1 class="gradient_text1">Your Title</h1>
            <p>Your content here...</p>
            <h2 class="gradient_text2">Subtitle</h2>
        </div>
    </main>
</body>
</html>
```

## Available CSS Classes

- `.gradient_text1` - Blue to purple gradient text
- `.gradient_text2` - Cyan to blue gradient text  
- `.wrapper` - Centers content with max-width
- `.theme-switch__*` - Theme toggle components

## Customization

### Change Background Images
Edit the CSS variables:
```css
:root {
    --bg-image: url(your-light-background.jpg);
}

.theme-switch__input:checked ~ main {
    --bg-image: url(your-dark-background.jpg);
}
```

### Change Colors
Modify the gradient and text color variables in the CSS file.

### Change Fonts
Update the Google Fonts import and font-family declarations.

## Legacy Files

The original complex structure is still in the repository under:
- `static/theme/css/` - Original modular CSS files
- `templates/` - Original Flask templates
- `scripts/` - Build system

These can be removed if you only need the clean theme.