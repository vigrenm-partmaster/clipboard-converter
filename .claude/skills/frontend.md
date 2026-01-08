# Frontend Theme System Skill

This skill documents the theme system for the clipboard converter frontend.

## Available Themes

The application supports 6 themes, selectable via the "Theme" button in the top-right corner.

### 1. Win 3.1 (Windows 3.1 / Retro)

Classic Windows 3.1 aesthetic with 3D beveled buttons.

**Colors:**
- Background: `#c0c0c0` (classic gray)
- Panels: `#c0c0c0` (gray)
- Input fields: `#fff` (white)
- Header: `#000080` (navy blue)
- Text: `#000` (black)
- Borders: 3D beveled (`#fff` light, `#808080` dark)

**Style:**
- No rounded corners (`border-radius: 0`)
- 3D beveled borders for buttons and panels
- System fonts (Arial, MS Sans Serif)
- No shadows or gradients

### 2. White (Light Theme)

Clean, modern light theme with subtle styling.

**Colors:**
- Background: `#e8e8e8` (light gray)
- Panels: `#fff` (white)
- Input fields: `#fff` (white)
- Header: `#fff` (white) with blue text
- Title text: `#2563eb` (blue)
- Body text: `#333` (dark gray)
- Buttons: `#e0e0e0` (light gray) with black borders

**Style:**
- Rounded corners (`border-radius: 3px`)
- Clean, minimal appearance
- No beveled borders

### 3. Black (Dark Theme)

Dark theme, opposite of the white theme.

**Colors:**
- Background: `#1a1a1a` (dark gray)
- Panels: `#000` (black)
- Input fields: `#000` (black)
- Header: `#000` (black) with blue text
- Title text: `#60a5fa` (light blue)
- Body text: `#f0f0f0` (light gray)
- Buttons: `#333` (dark gray)

**Style:**
- Rounded corners (`border-radius: 3px`)
- White borders on buttons and inputs
- Dark, high-contrast appearance
- No beveled borders

### 4. IFS (Corporate)

IFS branded corporate theme.

**Colors:**
- Background: `#f4f2f4` (light purple-gray)
- Panels: `#ffffff` (white)
- Header: `#FFAA35` (orange)
- Text: `#1a1b1d` (near black)
- Toast: `#8427e2` (purple)

**Style:**
- Rounded corners (`border-radius: 3px`)
- Clean corporate appearance

### 5. Crystal White (Modern Apple-inspired Light)

Modern glassmorphism theme inspired by Apple's crystal design language.

**Colors:**
- Background: Linear gradient from `#f5f5f7` to `#e8e8ed`
- Panels: `rgba(255, 255, 255, 0.72)` (semi-transparent white)
- Input fields: `rgba(255, 255, 255, 0.9)`
- Text: `#1d1d1f` (Apple's near-black)
- Accent: `rgba(0, 122, 255, 0.9)` (Apple blue)

**Style:**
- Large rounded corners (`border-radius: 12px`)
- Glassmorphism with `backdrop-filter: blur(20px)`
- Soft box shadows
- Smooth hover transitions
- System font stack (-apple-system, SF Pro Display)
- No beveled borders - flat modern design

### 6. Crystal Black (Modern Apple-inspired Dark)

Dark glassmorphism theme matching Apple's dark mode crystal aesthetic.

**Colors:**
- Background: Linear gradient from `#1d1d1f` to `#0d0d0d`
- Panels: `rgba(44, 44, 46, 0.72)` (semi-transparent dark)
- Input fields: `rgba(28, 28, 30, 0.9)`
- Text: `#f5f5f7` (Apple's off-white)
- Accent: `rgba(10, 132, 255, 0.9)` (Apple blue for dark mode)

**Style:**
- Large rounded corners (`border-radius: 12px`)
- Glassmorphism with `backdrop-filter: blur(20px)`
- Soft glow shadows
- Smooth hover transitions
- System font stack (-apple-system, SF Pro Display)
- Subtle light borders for depth
  
## CSS Variables

All themes use CSS custom properties for easy customization:

```css
--bg-main          /* Main background color */
--bg-panel         /* Panel background color */
--bg-input         /* Input field background */
--bg-button        /* Button background */
--bg-button-active /* Active/pressed button */
--bg-header        /* Header background */
--bg-toast         /* Toast notification background */
--text-main        /* Main text color */
--text-header      /* Header/title text color */
--text-subtitle    /* Subtitle text color */
--text-placeholder /* Placeholder text color */
--border-light     /* Light border color (3D effect) */
--border-dark      /* Dark border color (3D effect) */
--border-input     /* Input field border */
--border-radius    /* Corner radius (0 for Win3.1) */
--border-style     /* Border style (solid) */
```

## Theme Selector

Located in the top-right corner of the application:
- Click "Theme" button to open dropdown menu
- Select one
- Theme preference is saved to localStorage

## Target File

Frontend location: `/home/user/clipboard-converter/index.html`

## Adding a New Theme

To add a new theme:

1. Add a new CSS class with theme variables:
```css
.theme-newname {
    --bg-main: #...;
    --bg-panel: #...;
    /* ... other variables */
}
```

2. Add a button in the theme menu:
```html
<button class="theme-option" data-theme="theme-newname">New Theme</button>
```

## Agent Handover Instructions

When modifying themes:

1. **Read the current index.html** to understand the CSS variable structure
2. **Modify theme variables** in the appropriate `.theme-*` class
3. **Test all themes** to ensure consistency
4. **Preserve the theme switching JavaScript** logic
5. **Commit changes** with descriptive message
