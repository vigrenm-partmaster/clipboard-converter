# Retro Minimalist Frontend Design Skill

Transform the frontend to a minimalistic Windows 3.1 / old-style notebook aesthetic.

## Design Principles

1. **Color Palette**: Only white, black, and dark gray
   - Background: `#c0c0c0` (classic Windows gray) or `#ffffff` (white)
   - Text: `#000000` (black)
   - Borders: `#808080` (dark gray), `#000000` (black)
   - Button face: `#c0c0c0` or `#dfdfdf`
   - Disabled/secondary: `#808080`

2. **No Shadows**: Remove all `box-shadow` properties completely

3. **No Icons/Emojis**: Remove all emoji characters from text

4. **No Rounded Corners**: Set `border-radius: 0` everywhere

5. **No Gradients**: Replace all `linear-gradient` with flat solid colors

6. **No Animations**: Remove or minimize `transition` effects

7. **Windows 3.1 Button Style**: Use inset/outset borders for 3D effect
   ```css
   /* Raised button (normal state) */
   border: 2px solid;
   border-color: #fff #808080 #808080 #fff;

   /* Pressed button (active state) */
   border-color: #808080 #fff #fff #808080;
   ```

8. **System Fonts**: Use classic system fonts
   ```css
   font-family: 'MS Sans Serif', 'Arial', sans-serif;
   ```
   For code/monospace: `'Fixedsys', 'Courier New', monospace`

9. **Simple Borders**: Use 1-2px solid black or dark gray borders

10. **Flat, Functional Layout**: Focus on usability over aesthetics

## Target File

The frontend is located at: `/home/user/clipboard-converter/index.html`

All CSS is inline within `<style>` tags (lines 7-249).

## Specific Changes Required

### Body & Container
```css
body {
    font-family: 'Arial', 'MS Sans Serif', sans-serif;
    background: #c0c0c0;
    min-height: 100vh;
    padding: 20px;
    color: #000;
}
```

### Panels
```css
.panel {
    background: #fff;
    border: 2px solid;
    border-color: #808080 #fff #fff #808080;
    padding: 20px;
}
```

### Textareas
```css
textarea {
    background: #fff;
    border: 2px solid;
    border-color: #808080 #fff #fff #808080;
    padding: 10px;
    color: #000;
    font-family: 'Courier New', 'Fixedsys', monospace;
}
```

### Buttons (Windows 3.1 style)
```css
.btn {
    background: #c0c0c0;
    border: 2px solid;
    border-color: #fff #808080 #808080 #fff;
    color: #000;
    padding: 8px 16px;
    cursor: pointer;
    font-family: 'Arial', sans-serif;
}

.btn:active {
    border-color: #808080 #fff #fff #808080;
}
```

### Headers
```css
h1, h2, h3 {
    color: #000;
    font-weight: bold;
}
```

### Remove These Properties
- All `box-shadow`
- All `border-radius`
- All `linear-gradient`
- All `transition` (or set to `none`)
- All `transform` effects
- All rgba() transparency (use solid colors)

### Remove From HTML
- All emoji characters (📋, 📥, 📤, 🔄, 🗑️, 📖, ⚠️)
- Replace with plain text labels

## Agent Handover Instructions

When implementing this design:

1. **Read the current index.html** to understand existing structure
2. **Replace the entire `<style>` block** with Windows 3.1 styled CSS
3. **Update HTML content** to remove emojis from:
   - `<h1>` title
   - `<h2>` panel headers
   - Button labels
   - Instructions section
   - Warning message
4. **Test the application** by running `npm start` if needed
5. **Commit changes** with message like "Apply retro minimalist Windows 3.1 design"

## Example Complete CSS

```css
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Arial', 'MS Sans Serif', sans-serif;
    background: #c0c0c0;
    min-height: 100vh;
    padding: 20px;
    color: #000;
}

.container {
    max-width: 900px;
    margin: 0 auto;
    background: #c0c0c0;
}

header {
    text-align: center;
    margin-bottom: 20px;
    padding: 10px;
    background: #000080;
    color: #fff;
}

h1 {
    font-size: 1.5rem;
    margin-bottom: 5px;
    color: #fff;
}

.version {
    font-size: 0.8rem;
    color: #c0c0c0;
}

.subtitle {
    color: #c0c0c0;
    font-size: 0.9rem;
}

.main-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
}

@media (max-width: 768px) {
    .main-content {
        grid-template-columns: 1fr;
    }
}

.panel {
    background: #c0c0c0;
    border: 2px solid;
    border-color: #fff #808080 #808080 #fff;
    padding: 15px;
}

.panel h2 {
    font-size: 1rem;
    margin-bottom: 10px;
    color: #000;
    font-weight: bold;
}

textarea {
    width: 100%;
    height: 200px;
    background: #fff;
    border: 2px solid;
    border-color: #808080 #fff #fff #808080;
    padding: 8px;
    color: #000;
    font-family: 'Courier New', monospace;
    font-size: 12px;
    resize: vertical;
}

textarea:focus {
    outline: 1px dotted #000;
}

textarea::placeholder {
    color: #808080;
}

.controls {
    margin-top: 15px;
}

.mode-selector {
    display: flex;
    gap: 5px;
    margin-bottom: 10px;
}

.mode-btn {
    flex: 1;
    padding: 6px 12px;
    background: #c0c0c0;
    border: 2px solid;
    border-color: #fff #808080 #808080 #fff;
    color: #000;
    cursor: pointer;
    font-size: 0.9rem;
    font-weight: normal;
}

.mode-btn:active {
    border-color: #808080 #fff #fff #808080;
}

.mode-btn.active {
    background: #dfdfdf;
    border-color: #808080 #fff #fff #808080;
}

.action-buttons {
    display: flex;
    gap: 5px;
}

.btn {
    flex: 1;
    padding: 8px 16px;
    background: #c0c0c0;
    border: 2px solid;
    border-color: #fff #808080 #808080 #fff;
    color: #000;
    cursor: pointer;
    font-size: 0.9rem;
    font-weight: normal;
}

.btn:active {
    border-color: #808080 #fff #fff #808080;
}

.btn-primary {
    background: #c0c0c0;
}

.btn-secondary {
    background: #c0c0c0;
}

.btn-copy {
    background: #c0c0c0;
}

.stats {
    margin-top: 10px;
    padding: 8px;
    background: #fff;
    border: 1px solid #808080;
    font-size: 0.8rem;
    color: #000;
}

.warning {
    margin-top: 8px;
    padding: 8px;
    background: #fff;
    border: 2px solid #000;
    font-size: 0.8rem;
    color: #000;
    display: none;
}

.warning.show {
    display: block;
}

.toast {
    position: fixed;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%) translateY(100px);
    background: #000080;
    color: #fff;
    padding: 8px 16px;
    border: 2px solid;
    border-color: #fff #808080 #808080 #fff;
    font-weight: normal;
    opacity: 0;
    z-index: 1000;
}

.toast.show {
    transform: translateX(-50%) translateY(0);
    opacity: 1;
}

.instructions {
    margin-top: 20px;
    padding: 15px;
    background: #c0c0c0;
    border: 2px solid;
    border-color: #fff #808080 #808080 #fff;
}

.instructions h3 {
    color: #000;
    margin-bottom: 10px;
    font-size: 1rem;
}

.instructions ol {
    margin-left: 20px;
    color: #000;
    line-height: 1.6;
}

.instructions code {
    background: #fff;
    padding: 1px 4px;
    border: 1px solid #808080;
    color: #000;
    font-family: 'Courier New', monospace;
}
```

## Verification Checklist

After implementing, verify:
- [ ] No emojis visible anywhere
- [ ] No rounded corners
- [ ] No shadows
- [ ] No color gradients
- [ ] Only black, white, and gray colors used
- [ ] Buttons have 3D beveled appearance
- [ ] Text is readable (black on light background)
- [ ] Application still functions correctly
