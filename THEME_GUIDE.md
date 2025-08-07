# Webpark Themes Development Guide

This guide explains the structure and development of the Webpark Themes extension.

## Theme Structure

Each theme is defined in a JSON file with the following structure:

```json
{
  "$schema": "vscode://schemas/color-theme",
  "name": "Theme Name",
  "colors": {
    // UI Colors
  },
  "tokenColors": [
    // Syntax Highlighting Colors
  ]
}
```

## Available Themes

### 1. Webpark Primary (webpark-primary-color-theme.json)
- **UI Theme**: vs-dark
- **Purpose**: Original vibrant theme with deep backgrounds
- **Best For**: Modern development environments

### 2. Webpark Dark (webpark-dark-color-theme.json)
- **UI Theme**: vs-dark
- **Purpose**: Classic dark theme with balanced contrast
- **Best For**: Everyday development work

### 3. Webpark Light (webpark-light-color-theme.json)
- **UI Theme**: vs
- **Purpose**: Clean light theme
- **Best For**: Bright environments and daytime coding

### 4. Webpark Dimmed (webpark-dimmed-color-theme.json)
- **UI Theme**: vs-dark
- **Purpose**: Soft dark theme with reduced contrast
- **Best For**: Low-light environments

### 5. Webpark High Contrast (webpark-high-contrast-color-theme.json)
- **UI Theme**: hc-black
- **Purpose**: High contrast for accessibility
- **Best For**: Accessibility and challenging lighting

## Color Categories

### UI Colors
- **Editor Colors**: Background, foreground, whitespace
- **Activity Bar**: Background, foreground, badges
- **Side Bar**: Background, titles, headers
- **Tabs**: Active/inactive backgrounds, borders
- **Status Bar**: Background, foreground
- **Panels**: Background for various panels
- **Widgets**: Hover, suggest, peek view widgets

### Token Colors
- **Comments**: Code comments
- **Variables**: Variable names and placeholders
- **Keywords**: Language keywords, storage types
- **Strings**: String literals
- **Numbers**: Numeric constants
- **Functions**: Function names and calls
- **Classes**: Class and type names
- **Constants**: Language constants
- **Operators**: Mathematical and logical operators
- **Punctuation**: Separators and terminators

## Adding New Themes

1. Create a new JSON file in the `themes/` directory
2. Follow the existing theme structure
3. Add the theme to `package.json` in the `contributes.themes` array
4. Update the README.md with theme description
5. Update CHANGELOG.md with version information

## Testing Themes

1. Open the extension in VS Code
2. Press F5 to start debugging
3. In the new VS Code window, open Command Palette (Ctrl+Shift+P)
4. Type "Preferences: Color Theme"
5. Select your theme to test

## Best Practices

- Maintain consistent color schemes across themes
- Ensure good contrast ratios for accessibility
- Test themes in different lighting conditions
- Use semantic color names in comments
- Keep token colors consistent with language standards

## Color Palette Guidelines

### Dark Themes
- Use dark backgrounds (#000000 to #2d2d30)
- Bright foregrounds for good contrast
- Accent colors for highlights and errors

### Light Themes
- Use light backgrounds (#ffffff to #f3f3f3)
- Dark foregrounds for readability
- Muted accent colors

### High Contrast
- Maximum contrast (black/white)
- Bright accent colors
- Clear distinction between elements
