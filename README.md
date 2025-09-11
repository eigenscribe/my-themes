# My Themes

A clean, reusable theme collection for webpages and apps.

## 🎨 Clean Theme

A minimal theme with light/dark mode toggle, perfect for static websites and web applications.

### Features
- ✅ Theme toggle switch (sun/moon icons)
- ✅ Background image switching
- ✅ Gradient text utility classes
- ✅ Glassy container effects (glassmorphism)
- ✅ Profile layout with avatar and social links
- ✅ Responsive design
- ✅ Easy to customize and reuse

### Quick Demo
View the live demo: [Clean Theme Demo](https://8001--0199361a-f12b-7e11-8441-c50cdb8227fd.us-east-1-01.gitpod.dev)

### Usage
```html
<link rel="stylesheet" href="themes/clean/theme.css">
```

See [USAGE.md](USAGE.md) for complete integration guide.

## 📁 Repository Structure

```
my-themes/
├── themes/clean/          # ← Use this for new projects
│   ├── theme.css         # Complete theme stylesheet  
│   ├── index.html        # Demo/template
│   └── README.md         # Theme documentation
├── clean-theme.css       # Standalone version
├── clean-theme.html      # Standalone demo
└── USAGE.md             # Integration guide
```

## 🚀 Getting Started

1. **Copy the theme**: Download `themes/clean/` folder
2. **Include CSS**: Add `theme.css` to your HTML
3. **Add toggle**: Copy the theme switch HTML structure
4. **Customize**: Modify colors, fonts, and backgrounds as needed

## 🔧 Customization

The theme uses CSS variables for easy customization:

```css
:root {
    --bg: white;
    --text: black;
    --bg-image: url(your-background.jpg);
}
```

## 📚 Documentation

- [USAGE.md](USAGE.md) - Complete integration guide
- [themes/clean/README.md](themes/clean/README.md) - Theme-specific documentation

---

## 🥧 Legacy Flask App (Optional)

The original Flask demo is still available:

### Setup
```bash
cd ~/Desktop/Scriber-Labs/my-themes
git pull origin main
source .venv/bin/activate
```

### Build stylesheet
```bash
python scripts/build_bundle.py
```

### Run
```bash
python main.py
```

