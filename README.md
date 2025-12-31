# Interactive HTML

A collection of interactive electronics calculators, simulators, and educational tools built with HTML, CSS, and JavaScript. All tools run directly in the browser with no dependencies or installation required.

## 🚀 Quick Start

**[Launch Interactive Electronics Tools](https://isocialpractice.github.io/interactive-html/index.html)** - Browse all tools from our modern landing page with search and categorized navigation.

Or visit any tool directly from the list below.

## Features

- **No Installation Required**: All tools are standalone HTML files that run directly in any modern web browser
- **Interactive Visualizations**: Real-time visual feedback with SVG circuit diagrams and animated components
- **Modern Design**: Professional light theme inspired by leading electronics education platforms
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Educational**: Perfect for electronics students, hobbyists, and engineers
- **GitHub Pages Ready**: Optimized for hosting on GitHub Pages with SEO-friendly structure

## Available Tools

### 555 Timer Tools

- **[555 Timer Simulator](555-timer-simulator.html)** - Interactive 555 timer circuit simulator with tabs for Astable, Monostable, and Bistable modes
- **[555 Astable Calculator](555-astable-calculator.html)** - Calculate frequency and duty cycle for 555 timer astable mode with resistor and capacitor values
- **[555 Monostable Simulator](555-monostable-simulator.html)** - Simulate 555 timer monostable (one-shot) operation
- **[555 Logic Simulator](555-logic-simulator.html)** - Explore 555 timer logic configurations

### Resistor Tools

- **[Resistor Color Code Calculator](electronics-resistor-calculator.html)** - Interactive resistor color band decoder with visual representation
- **[Parallel Resistor Calculator](electronics-parallel-resistor-calculator.html)** - Calculate equivalent resistance for parallel resistor networks
- **[Fusible Resistor Calculator](electronics-fusible-resistor-calculator.html)** - Calculate specifications for fusible resistors

### LED & Power Tools

- **[LED Current Calculator](electronics-led-current-calculator.html)** - Calculate current-limiting resistor values for LEDs with visual circuit diagram
- **[Voltage Divider Calculator](electronics-voltage-divider-calculator.html)** - Design voltage divider circuits with interactive SVG diagrams
- **[Ohm's Law Calculator](electronics-ohms-law-calculator.html)** - Calculate voltage, current, resistance, and power using Ohm's Law (V = I × R)

### Component Tools

- **[Potentiometer Simulator](electronics-potentiometer-simulator.html)** - Interactive potentiometer simulator with adjustable wiper position
- **[Potentiometer Decoder](electronics-potentiometer-decoder.html)** - Decode potentiometer markings and specifications
- **[Surface Mount Decoder](electronics-electronics-surface-mount-decoder.html)** - Decode surface mount component markings
- **[Varistor Simulator](electronics-varistor-simulator.html)** - Simulate varistor voltage-current characteristics

## Usage

### Quick Start

1. Download any HTML file from this repository
2. Open the file in your web browser (Chrome, Firefox, Safari, Edge, etc.)
3. Start using the calculator or simulator immediately

### No Server Required

All tools are self-contained single-file applications. No web server, npm packages, or build process needed.

### Example Usage

**For LED projects:**
```
1. Open electronics-led-current-calculator.html
2. Enter your supply voltage (e.g., 5V)
3. Enter LED forward voltage (e.g., 2.0V for red LED)
4. Enter desired LED current (e.g., 20mA)
5. See the required resistor value and power rating
```

**For 555 timer circuits:**
```
1. Open 555-astable-calculator.html
2. Enter R1, R2, and C values
3. See calculated frequency and duty cycle
4. Adjust values to meet your timing requirements
```

**For resistor color codes:**
```
1. Open electronics-resistor-calculator.html
2. Select color bands from the dropdowns
3. See the decoded resistance value and tolerance
4. Visual resistor updates in real-time
```

## Technical Details

- **Built with**: Pure HTML5, CSS3, and vanilla JavaScript
- **Graphics**: SVG for scalable circuit diagrams and component visualizations
- **Compatibility**: Works in all modern browsers (Chrome, Firefox, Safari, Edge)
- **No Dependencies**: No frameworks, libraries, or external resources required
- **Offline Ready**: Download and use without internet connection

## Project Structure

```
interactive-html/
├── Templates/
│   └── page.html                         # Master template file
├── style.css                             # Global stylesheet
├── favicon.svg                           # Site icon
├── index.html                            # Landing page with tool browser
├── 555-timer-simulator.html              # Main 555 timer simulator
├── 555-astable-calculator.html           # 555 astable mode calculator
├── 555-monostable-simulator.html         # 555 monostable simulator
├── 555-logic-simulator.html              # 555 logic configurations
├── electronics-resistor-calculator.html  # Resistor color code decoder
├── electronics-parallel-resistor-calculator.html
├── electronics-fusible-resistor-calculator.html
├── electronics-led-current-calculator.html
├── electronics-ohms-law-calculator.html
├── electronics-voltage-divider-calculator.html
├── electronics-potentiometer-simulator.html
├── electronics-potentiometer-decoder.html
├── electronics-electronics-surface-mount-decoder.html
├── electronics-varistor-simulator.html
└── README.md
```

## Template System

This project uses a Dreamweaver-style template system for consistent navigation and styling across all pages. All HTML files inherit from `Templates/page.html`.

### For Users

No special setup needed - just open any HTML file in your browser. The template system works automatically.

### For Developers

#### Managing Templates with html-dwt-cmd

To update all pages when you modify the template, use the [html-dwt-cmd-template](https://github.com/isocialPractice/html-dwt-cmd-template/tree/main) CLI tool:

**Installation:**
```bash
git clone https://github.com/isocialPractice/html-dwt-cmd-template.git
cd html-dwt-cmd-template
npm install
npm run compile
npm link  # Optional: makes html-dwt-cmd available globally
```

**Usage Example:**
```bash
# Update all HTML files after modifying Templates/page.html
html-dwt-cmd update-all Templates/page.html --auto-apply
```

**What it does:**
- Scans all HTML files using the template
- Creates automatic backups in `.html-dwt-cmd-template-backups/`
- Updates non-editable template content (navigation, header, footer)
- Preserves editable regions (page title, styles, content)
- Ensures consistency across all 15+ pages

**Common Commands:**
```bash
# Update all pages (with automatic application)
html-dwt-cmd update-all Templates/page.html --auto-apply

# Find all pages using the template
html-dwt-cmd find-instances Templates/page.html

# View editable regions in a file
html-dwt-cmd show-regions 555-timer-simulator.html
```

#### Manual Template Structure

Each HTML file follows this pattern:
```html
<!-- InstanceBegin template="/Templates/page.html" -->
<head>
  <link rel="stylesheet" href="style.css">
  <link rel="icon" href="favicon.svg">
  
  <!-- InstanceBeginEditable name="head" -->
  <title>Page Title</title>
  <style>/* Page-specific styles */</style>
  <!-- InstanceEndEditable -->
</head>
<body>
  <nav class="site-nav"><!-- Global navigation --></nav>
  
  <!-- InstanceBeginEditable name="page" -->
  <!-- Page content here -->
  <!-- InstanceEndEditable -->
</body>
```

See [QUICK_START.md](QUICK_START.md) and [STRUCTURE.md](STRUCTURE.md) for detailed documentation.

## Use Cases

### For Students
- Learn electronics concepts through interactive visualization
- Verify homework calculations
- Understand component behavior and circuit operation

### For Hobbyists
- Design LED projects with proper current limiting
- Calculate 555 timer values for projects
- Decode resistor color codes quickly
- Plan voltage divider circuits

### For Engineers
- Quick reference calculations
- Prototype circuit design
- Component selection assistance
- Educational demonstrations

## Browser Compatibility

| Browser | Minimum Version |
|---------|----------------|
| Chrome  | 60+            |
| Firefox | 55+            |
| Safari  | 11+            |
| Edge    | 79+            |

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**What this means:**
- ✅ Free to use for personal and commercial projects
- ✅ Free to modify and distribute
- ✅ No warranty or liability
- ✅ Attribution appreciated but not required

## Contributing

Contributions are welcome! Feel free to:
- Report bugs or issues
- Suggest new features or tools
- Submit pull requests
- Improve documentation

## Contact

For questions, suggestions, or issues, please open an issue in this repository.

