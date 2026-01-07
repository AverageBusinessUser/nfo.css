# NFO.css

A CSS library that emulates the aesthetic of NFO file ASCII art from the demoscene era. Bring the retro terminal/warez look to your web projects.

```
 ███╗   ██╗███████╗ ██████╗    ██████╗███████╗███████╗
 ████╗  ██║██╔════╝██╔═══██╗  ██╔════╝██╔════╝██╔════╝
 ██╔██╗ ██║█████╗  ██║   ██║  ██║     ███████╗███████╗
 ██║╚██╗██║██╔══╝  ██║   ██║  ██║     ╚════██║╚════██║
 ██║ ╚████║██║     ╚██████╔╝  ╚██████╗███████║███████║
 ╚═╝  ╚═══╝╚═╝      ╚═════╝    ╚═════╝╚══════╝╚══════╝
```

## Features

- **Full component library**: Boxes, buttons, cards, navigation, tables, forms, lists
- **ASCII & Unicode borders**: Both pure ASCII (`+--+`) and Unicode box-drawing (`┌─┐`) styles
- **Effects**: Glows, gradients, scanlines, CRT flicker, cursor blink, typing animation
- **Responsive**: Works on all screen sizes
- **No dependencies**: Pure CSS, no JavaScript required
- **Accessibility**: Respects `prefers-reduced-motion`

## Installation

### Direct Download

Download the files and include in your HTML:

```html
<link rel="stylesheet" href="path/to/src/nfo.css">
```

## Quick Start

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="nfo.css">
</head>
<body class="nfo-page nfo-scanlines">
  <div class="nfo-container">
    <h1 class="nfo-cyan nfo-glow-cyan">Welcome</h1>
    <div class="nfo-box nfo-box-single nfo-box-cyan">
      <p>Your content here</p>
    </div>
    <button class="nfo-btn nfo-btn-bracket nfo-cyan">[ Click Me ]</button>
  </div>
</body>
</html>
```

## Color Palette

| Color | Variable | Hex |
|-------|----------|-----|
| Cyan | `--nfo-cyan` | `#00ffff` |
| Green | `--nfo-green` | `#00ff00` |
| Magenta | `--nfo-magenta` | `#ff00ff` |
| Yellow | `--nfo-yellow` | `#ffff00` |
| Orange | `--nfo-orange` | `#ff6600` |
| Red | `--nfo-red` | `#ff0000` |
| Blue | `--nfo-blue` | `#0066ff` |
| White | `--nfo-white` | `#ffffff` |

## Components

### Boxes

```html
<!-- Single border -->
<div class="nfo-box nfo-box-single">Content</div>

<!-- Double border -->
<div class="nfo-box nfo-box-double">Content</div>

<!-- ASCII dashed border -->
<div class="nfo-box nfo-box-ascii">Content</div>

<!-- Block border (thick) -->
<div class="nfo-box nfo-box-block-full">Content</div>

<!-- Colored border -->
<div class="nfo-box nfo-box-single nfo-box-cyan">Content</div>
<div class="nfo-box nfo-box-single nfo-box-green">Content</div>
<div class="nfo-box nfo-box-single nfo-box-magenta">Content</div>

<!-- Unicode box with corners -->
<div class="nfo-box-unicode-full">
  <div class="nfo-box-unicode-top">
    <span class="nfo-box-unicode-line"></span>
  </div>
  <div class="nfo-box-unicode-content">Content</div>
  <div class="nfo-box-unicode-bottom">
    <span class="nfo-box-unicode-line"></span>
  </div>
</div>

<!-- Box with header -->
<div class="nfo-box-header nfo-box-single">
  <div class="nfo-box-header-title">Title</div>
  <div class="nfo-box-header-content">Content</div>
</div>
```

### Banners

```html
<!-- ASCII art banner -->
<pre class="nfo-banner nfo-banner-cyan nfo-banner-glow">
 █████╗ ██████╗ ████████╗
██╔══██╗██╔══██╗╚══██╔══╝
███████║██████╔╝   ██║
██╔══██║██╔══██╗   ██║
██║  ██║██║  ██║   ██║
╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝
</pre>

<!-- Sizes: nfo-banner-sm, nfo-banner-md, nfo-banner-lg, nfo-banner-xl -->
<!-- Colors: nfo-banner-cyan, nfo-banner-green, nfo-banner-magenta, nfo-banner-yellow -->
<!-- Effects: nfo-banner-glow, nfo-banner-glow-intense -->
<!-- Frames: nfo-banner-framed, nfo-banner-double-framed -->
<!-- Gradient: nfo-banner-gradient -->
```

### Dividers

```html
<div class="nfo-divider nfo-divider-single nfo-cyan"></div>
<div class="nfo-divider nfo-divider-double nfo-green"></div>
<div class="nfo-divider nfo-divider-ascii"></div>
<div class="nfo-divider nfo-divider-dots nfo-magenta"></div>
<div class="nfo-divider nfo-divider-stars nfo-yellow"></div>
<div class="nfo-divider nfo-divider-blocks nfo-orange"></div>

<!-- Title divider -->
<div class="nfo-title-divider nfo-cyan">
  <span class="nfo-title-divider-text">Section Title</span>
</div>
```

### Buttons

```html
<!-- Standard -->
<button class="nfo-btn">Default</button>
<button class="nfo-btn nfo-btn-cyan">Cyan</button>
<button class="nfo-btn nfo-btn-green">Green</button>
<button class="nfo-btn nfo-btn-magenta">Magenta</button>
<button class="nfo-btn nfo-btn-yellow">Yellow</button>
<button class="nfo-btn nfo-btn-orange">Orange</button>
<button class="nfo-btn nfo-btn-red">Red</button>

<!-- Solid style -->
<button class="nfo-btn nfo-btn-solid">Solid</button>
<button class="nfo-btn nfo-btn-solid nfo-btn-cyan">Solid Cyan</button>

<!-- Bracket style [ Button ] -->
<button class="nfo-btn nfo-btn-bracket">Download</button>

<!-- Arrow style < Button > -->
<button class="nfo-btn nfo-btn-arrow">Navigate</button>

<!-- Block style -->
<button class="nfo-btn nfo-btn-block">Block</button>

<!-- Sizes -->
<button class="nfo-btn nfo-btn-sm">Small</button>
<button class="nfo-btn nfo-btn-lg">Large</button>

<!-- Button group -->
<div class="nfo-btn-group">
  <button class="nfo-btn nfo-btn-cyan">First</button>
  <button class="nfo-btn nfo-btn-cyan">Second</button>
  <button class="nfo-btn nfo-btn-cyan">Third</button>
</div>

<!-- With glow -->
<button class="nfo-btn nfo-btn-cyan nfo-btn-glow-cyan">Glow</button>
<button class="nfo-btn nfo-btn-green nfo-btn-glow-green">Glow</button>
<button class="nfo-btn nfo-btn-magenta nfo-btn-glow-magenta">Glow</button>
```

### Cards

```html
<!-- Standard card -->
<div class="nfo-card nfo-card-cyan">
  <div class="nfo-card-header">
    <h3 class="nfo-card-title">Title</h3>
  </div>
  <div class="nfo-card-body">Content here</div>
  <div class="nfo-card-footer">Footer</div>
</div>

<!-- Color variants: nfo-card-cyan, nfo-card-green, nfo-card-magenta, nfo-card-yellow -->

<!-- Glow variants -->
<div class="nfo-card nfo-card-glow-cyan">...</div>
<div class="nfo-card nfo-card-glow-green">...</div>
<div class="nfo-card nfo-card-glow-magenta">...</div>

<!-- Horizontal layout -->
<div class="nfo-card nfo-card-horizontal nfo-card-cyan">
  <div class="nfo-card-header"><h3 class="nfo-card-title">Title</h3></div>
  <div class="nfo-card-body">Content side by side</div>
</div>

<!-- Compact variant -->
<div class="nfo-card nfo-card-compact">...</div>

<!-- ASCII header style -->
<div class="nfo-card-ascii-header">
  <div class="nfo-card-header"><h3 class="nfo-card-title">:: Title ::</h3></div>
  <div class="nfo-card-body">Content</div>
  <div class="nfo-card-footer">Footer</div>
</div>

<!-- Card meta info -->
<div class="nfo-card-meta">
  <div class="nfo-card-meta-row">
    <span class="nfo-card-meta-label">Title</span>
    <span class="nfo-card-meta-value">Value</span>
  </div>
</div>
```

### Navigation

```html
<!-- Bracket style [item] -->
<nav class="nfo-nav nfo-nav-bracket">
  <a href="#" class="nfo-nav-item">Home</a>
  <a href="#" class="nfo-nav-item active">About</a>
  <a href="#" class="nfo-nav-item">Contact</a>
</nav>

<!-- With separators -->
<nav class="nfo-nav nfo-nav-separated">...</nav>
<nav class="nfo-nav nfo-nav-separated-dot">...</nav>
<nav class="nfo-nav nfo-nav-separated-arrow">...</nav>

<!-- Vertical -->
<nav class="nfo-nav nfo-nav-vertical">
  <a href="#" class="nfo-nav-item">Item 1</a>
  <a href="#" class="nfo-nav-item">Item 2</a>
</nav>

<!-- Pointer style > item -->
<nav class="nfo-nav nfo-nav-pointer nfo-nav-vertical">...</nav>

<!-- Boxed -->
<nav class="nfo-nav nfo-nav-boxed">...</nav>

<!-- Color variants: nfo-nav-green, nfo-nav-magenta, nfo-nav-yellow -->

<!-- Tabs -->
<div class="nfo-tabs">
  <a href="#" class="nfo-tab active">Tab 1</a>
  <a href="#" class="nfo-tab">Tab 2</a>
</div>

<!-- Breadcrumb -->
<nav class="nfo-breadcrumb">
  <a href="#" class="nfo-breadcrumb-item">Home</a>
  <span class="nfo-breadcrumb-separator"></span>
  <a href="#" class="nfo-breadcrumb-item">Section</a>
</nav>
```

### Tables

```html
<table class="nfo-table nfo-table-striped nfo-table-hover">
  <thead>
    <tr>
      <th>Name</th>
      <th>Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Item</td>
      <td>Data</td>
    </tr>
  </tbody>
</table>

<!-- NFO-style info table -->
<table class="nfo-info-table">
  <tr><th>Label</th><td>Value</td></tr>
</table>
```

### Forms

```html
<!-- Basic input -->
<div class="nfo-form-group">
  <label class="nfo-label">Username</label>
  <input type="text" class="nfo-input nfo-input-glow">
</div>

<!-- Required field -->
<label class="nfo-label nfo-label-required">Password</label>

<!-- Input sizes -->
<input class="nfo-input nfo-input-sm">
<input class="nfo-input nfo-input-lg">

<!-- Color variants (on focus) -->
<input class="nfo-input nfo-input-cyan">
<input class="nfo-input nfo-input-green">
<input class="nfo-input nfo-input-magenta">

<!-- Input group with prefix/suffix -->
<div class="nfo-input-group">
  <span class="nfo-input-prefix">$</span>
  <input type="text" class="nfo-input">
  <span class="nfo-input-suffix">.00</span>
</div>

<!-- Textarea -->
<textarea class="nfo-textarea"></textarea>

<!-- Select -->
<select class="nfo-select">
  <option>Option 1</option>
</select>

<!-- Checkbox [x] style -->
<label class="nfo-checkbox">
  <input type="checkbox">
  <span class="nfo-checkbox-indicator"></span>
  Option
</label>

<!-- Checkbox block [█] style -->
<label class="nfo-checkbox nfo-checkbox-block">
  <input type="checkbox">
  <span class="nfo-checkbox-indicator"></span>
  Option
</label>

<!-- Radio (•) style -->
<label class="nfo-radio">
  <input type="radio" name="group">
  <span class="nfo-radio-indicator"></span>
  Option
</label>

<!-- Validation states -->
<input class="nfo-input nfo-input-error">
<span class="nfo-error-message">Error message</span>

<input class="nfo-input nfo-input-success">
<span class="nfo-help">Help text</span>

<!-- Fieldset -->
<fieldset class="nfo-fieldset">
  <legend class="nfo-legend">:: Settings ::</legend>
  <!-- form fields -->
</fieldset>
```

### Lists

```html
<!-- Bullet styles -->
<ul class="nfo-list nfo-list-arrow">...</ul>      <!-- > item -->
<ul class="nfo-list nfo-list-dash">...</ul>       <!-- - item -->
<ul class="nfo-list nfo-list-asterisk">...</ul>   <!-- * item -->
<ul class="nfo-list nfo-list-dot">...</ul>        <!-- • item -->
<ul class="nfo-list nfo-list-block">...</ul>      <!-- █ item -->
<ul class="nfo-list nfo-list-double-arrow">...</ul> <!-- >> item -->
<ul class="nfo-list nfo-list-bracket">...</ul>    <!-- [+] item -->
<ul class="nfo-list nfo-list-numbered">...</ul>   <!-- [01] item -->

<!-- Color variants -->
<ul class="nfo-list nfo-list-arrow nfo-list-cyan">...</ul>
<ul class="nfo-list nfo-list-arrow nfo-list-green">...</ul>
<ul class="nfo-list nfo-list-arrow nfo-list-magenta">...</ul>

<!-- Horizontal list -->
<ul class="nfo-list nfo-list-horizontal">...</ul>
<ul class="nfo-list nfo-list-horizontal nfo-list-horizontal-separated">...</ul>

<!-- Description list -->
<dl class="nfo-dl">
  <dt>Term</dt>
  <dd>Description</dd>
</dl>

<!-- Inline description list -->
<dl class="nfo-dl nfo-dl-inline">...</dl>

<!-- Static checklist -->
<ul class="nfo-list nfo-checklist">
  <li class="checked">Done</li>
  <li>Pending</li>
</ul>

<!-- Interactive checklist -->
<ul class="nfo-list nfo-checklist-interactive">
  <li>
    <label>
      <input type="checkbox">
      <span class="nfo-check-indicator"></span>
      <span class="nfo-check-text">Task</span>
    </label>
  </li>
</ul>

<!-- Checklist variants -->
<ul class="nfo-list nfo-checklist-interactive nfo-checklist-block">...</ul>  <!-- [█] -->
<ul class="nfo-list nfo-checklist-interactive nfo-checklist-star">...</ul>   <!-- [*] -->

<!-- File tree -->
<ul class="nfo-list nfo-tree">
  <li class="nfo-tree-folder"><span class="nfo-tree-name">src</span>
    <ul class="nfo-tree">
      <li class="nfo-tree-file"><span class="nfo-tree-name">index.js</span></li>
    </ul>
  </li>
</ul>

<!-- Bracket-style file tree -->
<ul class="nfo-list nfo-tree nfo-tree-bracket">...</ul>
```

## Effects

### Glows

```html
<!-- Text glows -->
<span class="nfo-cyan nfo-glow-cyan">Cyan glow</span>
<span class="nfo-green nfo-glow-green">Green glow</span>
<span class="nfo-magenta nfo-glow-magenta">Magenta glow</span>
<span class="nfo-yellow nfo-glow-yellow">Yellow glow</span>
<span class="nfo-orange nfo-glow-orange">Orange glow</span>
<span class="nfo-red nfo-glow-red">Red glow</span>

<!-- Intensity variants -->
<span class="nfo-glow-subtle">Subtle</span>
<span class="nfo-glow">Normal</span>
<span class="nfo-glow-strong">Strong</span>
<span class="nfo-glow-cyan-strong">Strong cyan</span>

<!-- Box glows -->
<div class="nfo-box nfo-box-glow">...</div>
<div class="nfo-box nfo-box-glow-cyan">...</div>
<div class="nfo-box nfo-box-glow-green">...</div>
<div class="nfo-box nfo-box-glow-magenta">...</div>

<!-- Border glows -->
<div class="nfo-box nfo-border-glow-cyan">...</div>
<div class="nfo-box nfo-border-glow-green">...</div>
<div class="nfo-box nfo-border-glow-magenta">...</div>

<!-- Pulsing glow -->
<span class="nfo-glow-pulse">Pulsing</span>
```

### Animations

```html
<!-- Blinking -->
<span class="nfo-blink">Blinking text</span>

<!-- Cursor styles -->
<span class="nfo-cursor">Text with block cursor</span>
<span class="nfo-cursor-underscore">Text with underscore</span>
<span class="nfo-cursor-pipe">Text with pipe</span>

<!-- Scanlines (apply to body or container) -->
<body class="nfo-scanlines">...</body>
<body class="nfo-scanlines-heavy">...</body>

<!-- Moving scanline -->
<div class="nfo-scanline-moving">Content</div>

<!-- CRT flicker -->
<div class="nfo-flicker">Flickering</div>
<div class="nfo-flicker-subtle">Subtle flicker</div>

<!-- Glitch on hover -->
<span class="nfo-glitch">Hover me</span>

<!-- RGB shift on hover -->
<span class="nfo-rgb-shift">Hover me</span>

<!-- Fade in -->
<div class="nfo-fade-in">Fades in</div>
<div class="nfo-fade-in-up">Fades in from below</div>

<!-- CRT power on (page load effect) -->
<body class="nfo-crt-on">...</body>

<!-- Typing effect -->
<p class="nfo-typing">This text types out...</p>
```

### Gradients

```html
<!-- Text gradients -->
<span class="nfo-gradient-text nfo-gradient-cyan-magenta">Gradient</span>
<span class="nfo-gradient-text nfo-gradient-green-cyan">Gradient</span>
<span class="nfo-gradient-text nfo-gradient-magenta-yellow">Gradient</span>
<span class="nfo-gradient-text nfo-gradient-orange-red">Gradient</span>
<span class="nfo-gradient-text nfo-gradient-rainbow">Rainbow</span>

<!-- Animated gradient -->
<span class="nfo-gradient-text nfo-gradient-cyan-magenta nfo-gradient-animated">Animated</span>

<!-- Background gradients -->
<div class="nfo-bg-gradient-dark">...</div>
<div class="nfo-bg-gradient-blue">...</div>
<div class="nfo-bg-gradient-radial">...</div>
<div class="nfo-bg-gradient-cyan-tint">...</div>
<div class="nfo-bg-gradient-green-tint">...</div>
<div class="nfo-bg-gradient-magenta-tint">...</div>

<!-- Vignette effect -->
<div class="nfo-vignette">Content with vignette</div>
```

## Layout

### Page Setup

```html
<body class="nfo-page nfo-scanlines">
  <div class="nfo-container">
    <!-- content -->
  </div>
</body>
```

### Containers

```html
<div class="nfo-container"><!-- max-width: 1024px --></div>
<div class="nfo-container nfo-container-sm"><!-- max-width: 640px --></div>
<div class="nfo-container nfo-container-lg"><!-- max-width: 1280px --></div>
<div class="nfo-container nfo-container-full"><!-- full width --></div>
```

### Grid

```html
<div class="nfo-grid nfo-grid-cols-2 nfo-gap-4">
  <div>Column 1</div>
  <div>Column 2</div>
</div>

<!-- Responsive -->
<div class="nfo-grid nfo-grid-cols-1 nfo-md-grid-cols-2 nfo-lg-grid-cols-3 nfo-gap-4">
  ...
</div>
```

### Flexbox

```html
<div class="nfo-flex nfo-gap-4">...</div>
<div class="nfo-flex nfo-flex-col">...</div>
<div class="nfo-flex nfo-justify-center">...</div>
<div class="nfo-flex nfo-items-center">...</div>
<div class="nfo-flex nfo-flex-wrap">...</div>
```

### Spacing

```html
<!-- Padding -->
<div class="nfo-p-4">All sides</div>
<div class="nfo-px-4">Horizontal</div>
<div class="nfo-py-4">Vertical</div>
<div class="nfo-pt-4 nfo-pb-2">Top and bottom</div>

<!-- Margin -->
<div class="nfo-m-4">All sides</div>
<div class="nfo-mx-4">Horizontal</div>
<div class="nfo-my-4">Vertical</div>
<div class="nfo-mt-4 nfo-mb-2">Top and bottom</div>

<!-- Gap (for flex/grid) -->
<div class="nfo-flex nfo-gap-2">...</div>
<div class="nfo-grid nfo-gap-4">...</div>
```

## Customization

Override CSS variables to customize colors:

```css
:root {
  --nfo-cyan: #00cccc;
  --nfo-green: #33ff33;
  --nfo-bg-black: #000000;
  --nfo-font-family: "Your Font", monospace;
  --nfo-blink-speed: 1s;
}
```

## Demo

Open `examples/index.html` in a browser to see all components in action.

## License

MIT License

## Credits

Inspired by the NFO files and ANSI/ASCII art of the demoscene and warez scene of the 90s and 2000s.
