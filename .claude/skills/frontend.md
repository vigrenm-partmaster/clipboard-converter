# Frontend Theme System Skill

This skill documents the theme system and features for the clipboard converter frontend.

## Available Themes

The application supports 3 themes, selectable via the "Theme" button in the top-right corner. **Crystal White is the default theme.**

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

### 2. Crystal White (Modern Apple-inspired Light) - DEFAULT

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

### 3. Crystal Black (Modern Apple-inspired Dark)

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

## Features

### Duplicate Removal

The converter automatically removes duplicate values from the input:
- Duplicates are detected after normalizing to uppercase
- The stats display shows: `Items: X | Characters: Y | Duplicates removed: Z`
- Only unique values appear in the output

### Output Modes

Two separator modes available:
- **Semicolon (;)**: Values joined with semicolons: `VALUE1;VALUE2;VALUE3`
- **Semicolon Equals (;=)**: Values prefixed with equals: `=VALUE1;=VALUE2;=VALUE3`

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
--border-radius    /* Corner radius (0 for Win3.1, 12px for Crystal) */
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

3. For crystal-style themes, add glassmorphism overrides with `backdrop-filter: blur()`.

## Agent Handover Instructions

When modifying themes:

1. **Read the current index.html** to understand the CSS variable structure
2. **Modify theme variables** in the appropriate `.theme-*` class
3. **Test all themes** to ensure consistency
4. **Preserve the theme switching JavaScript** logic
5. **Commit changes** with descriptive message
