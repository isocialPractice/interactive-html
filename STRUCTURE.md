# Template Structure Visualization

## File Architecture

```
interactive-html/
│
├── style.css                          # Global stylesheet (NEW)
├── favicon.svg                        # Site icon (NEW)
├── index.html                         # Landing page ✅
│
├── Templates/
│   └── page.html                      # Master template ✅
│
├── 555-astable-calculator.html        # ✅ Template applied
├── 555-timer-simulator.html           # ✅ Template applied
├── 555-monostable-simulator.html      # ✅ Template applied
├── 555-logic-simulator.html           # ✅ Template applied
│
├── electronics-ohms-law-calculator.html              # ✅ Template applied
├── electronics-led-current-calculator.html           # ✅ Template applied
├── electronics-voltage-divider-calculator.html       # ✅ Template applied
├── electronics-resistor-calculator.html              # ✅ Template applied
├── electronics-parallel-resistor-calculator.html     # ✅ Template applied
├── electronics-fusible-resistor-calculator.html      # ✅ Template applied
├── electronics-potentiometer-simulator.html          # ✅ Template applied
├── electronics-potentiometer-decoder.html            # ✅ Template applied
├── electronics-varistor-simulator.html               # ✅ Template applied
└── electronics-electronics-surface-mount-decoder.html # ✅ Template applied
```

## HTML Page Structure

```html
┌─────────────────────────────────────────────────────────────┐
│ <!DOCTYPE html>                                             │
│ <!-- InstanceBegin template="/Templates/page.html" -->      │
│ <html>                                                      │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│ <head>                                                      │
│   <meta charset="UTF-8">                                    │
│   <meta name="viewport"...>                                 │
│   <link rel="stylesheet" href="style.css">    ◄── GLOBAL    │
│   <link rel="icon" href="favicon.svg">        ◄── GLOBAL    │
│                                                             │
│   <!-- InstanceBeginEditable name="head" -->                │
│   ┌───────────────────────────────────────────────────┐     │
│   │ <title>Page-Specific Title</title>                │     │
│   │ <style>                                           │     │
│   │   /* Page-specific styles override global */      │     │
│   │ </style>                                          │     │
│   └───────────────────────────────────────────────────┘     │
│   <!-- InstanceEndEditable -->                              │
│ </head>                                                     │
└─────────────────────────────────────────────────────────────┘
                            │
                            ▼
┌─────────────────────────────────────────────────────────────┐
│ <body>                                                      │
│   ┌─────────────────────────────────────────────────────┐   │
│   │ FIXED NAVIGATION BAR (Same on all pages)            │   │
│   │ ┌───────────────────────────────────────────────┐   │   │
│   │ │ Logo │ 555 Timer ▼ │ Resistors ▼ │ LED ▼ │... │   │   │
│   │ └───────────────────────────────────────────────┘   │   │
│   └─────────────────────────────────────────────────────┘   │
│                                                             │
│   <!-- InstanceBeginEditable name="page" -->                │
│   ┌───────────────────────────────────────────────────┐     │
│   │                                                   │     │
│   │  <div class="container">                          │     │
│   │    <h1>Tool Title</h1>                            │     │
│   │    <p class="subtitle">Description</p>            │     │
│   │                                                   │     │
│   │    <div class="controls">                         │     │
│   │      <!-- Input elements -->                      │     │
│   │    </div>                                         │     │
│   │                                                   │     │
│   │    <div class="results">                          │     │
│   │      <!-- Output display -->                      │     │
│   │    </div>                                         │     │
│   │                                                   │     │
│   │    <script>                                       │     │
│   │      // Tool-specific JavaScript                  │     │
│   │    </script>                                      │     │
│   │  </div>                                           │     │
│   │                                                   │     │
│   └───────────────────────────────────────────────────┘     │
│   <!-- InstanceEndEditable -->                              │
│                                                             │
│ </body>                                                     │
│ <!-- InstanceEnd -->                                        │
│ </html>                                                     │
└─────────────────────────────────────────────────────────────┘
```

## Navigation Menu Structure

```
┌──────────────────────────────────────────────────────────────────┐
│  [ Logo ] Electronics Tools                               [=]    │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌────────────┐  ┌───────────┐  ┌──────────┐  ┌───────────┐      │
│  │     555    │  │    Resist │  │   LED &  │  │     Compo │      │
│  │   Timer ▼  │  │   -ors ▼  │  │   Power ▼│  │   -nents ▼│      │
│  └────────────┘  └───────────┘  └──────────┘  └───────────┘      │
│      │               │               │               │           │
│      │               │               │               │           │
│      ▼               ▼               ▼               ▼           │
│  ┌──────────┐    ┌──────────┐    ┌─────────┐    ┌─────────┐      │
│  │Simulator │    │Color Code│    │Ohm's Law│    │ Potentio│      │
│  │Astable   │    │Parallel  │    │LED Calc │    │  -meter │      │
│  │Monostable│    │Fusible   │    │Voltage  │    │ Decoder │      │
│  │Logic     │    └──────────┘    │Varistor │    │   SMD   │      │
│  └──────────┘                    └─────────┘    └─────────┘      │
└──────────────────────────────────────────────────────────────────┘
```

## CSS Variable System

```css
:root {
    /* Color System */
    --color-primary: #0066CC        ◄── Buttons, links, accents
    --color-primary-dark: #004080   ◄── Headings, hover states
    --color-primary-light: #E6F2FF  ◄── Backgrounds, highlights
    --color-secondary: #00A86B      ◄── Success indicators
    --color-accent: #FF6B35         ◄── Warning, special attention
    
    /* Typography */
    --font-family: Inter, Segoe UI, system
    --font-size-base: 16px
    --font-weight-bold: 700
    
    /* Spacing */
    --spacing-md: 16px
    --spacing-lg: 24px
    
    /* Effects */
    --radius-md: 8px
    --shadow-lg: 0 8px 24px rgba(0,0,0,0.12)
}
```

## Style Cascade Flow

```
1. GLOBAL STYLES (style.css)
   │
   ├─→ CSS Variables (colors, fonts, spacing)
   ├─→ Reset styles (* selector)
   ├─→ Navigation menu styles
   ├─→ Common component styles
   └─→ Responsive breakpoints
   
2. PAGE-SPECIFIC STYLES (in <head>)
   │
   ├─→ Override global styles as needed
   ├─→ Tool-specific layouts
   ├─→ Custom visualizations
   └─→ Unique interactive elements

3. INLINE STYLES (rarely used)
   │
   └─→ Dynamic JavaScript-generated styles
```

## Component Reuse Patterns

```html
<!-- Standard Input Group -->
<div class="control-group">
    <label>Input Label</label>
    <input type="range" id="slider" min="0" max="100" value="50">
    <div class="value-display" id="value">50</div>
</div>

<!-- Results Display -->
<div class="results">
    <div class="result-row">
        <span class="result-label">Label:</span>
        <span class="result-value" id="result">0</span>
    </div>
</div>

<!-- Information Box -->
<div class="info-box">
    <div class="info-title">ℹ️ Title</div>
    <div class="info-text">Explanation text...</div>
</div>

<!-- Button -->
<button class="btn" onclick="calculate()">Calculate</button>
```

## Template Editing Workflow

```
┌─────────────────────────────────────────────┐
│ 1. Developer edits Templates/page.html      │
│    (Master template with navigation)        │
└─────────────────┬───────────────────────────┘
                  │
                  ▼
┌─────────────────────────────────────────────┐
│ 2. Changes propagate to all pages via       │
│    Instance comments (conceptually)         │
└─────────────────┬───────────────────────────┘
                  │
                  ▼
┌─────────────────────────────────────────────┐
│ 3. Each page maintains two editable regions:│
│    • <head> for title and page styles       │
│    • <body> for page content                │
└─────────────────────────────────────────────┘
```

## Dreamweaver-Style Template Tags

```html
<!-- InstanceBegin -->       ← Marks start of page instance
<!-- InstanceBeginEditable → Marks editable region start
<!-- InstanceEndEditable →   Marks editable region end
<!-- InstanceEnd -->          ← Marks end of page instance

<!-- TemplateBegin →         Master template start (in Templates/)
<!-- TemplateBeginEditable →  Master editable region start
<!-- TemplateEndEditable →    Master editable region end
```

## Data Flow Diagram

```
User Action (Click Tool Link)
        │
        ▼
    Browser loads HTML file
        │
        ├─→ Loads style.css (cached after first load)
        ├─→ Loads favicon.svg (cached after first load)
        └─→ Renders page HTML
               │
               ├─→ Fixed Navigation (from template)
               ├─→ Page Content (unique to tool)
               └─→ JavaScript initialization
                      │
                      ▼
                  Interactive Tool Ready
```

---

This structure provides:
- **Consistency**: All pages follow same pattern
- **Maintainability**: Global changes in one place
- **Scalability**: Easy to add new tools
- **Performance**: Shared assets cached
- **Flexibility**: Per-page customization where needed
