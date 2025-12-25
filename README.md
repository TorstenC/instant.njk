# instant.njk

Nunjucks Playground with Live-Preview for HTML

## About

A minimalist browser-based playground for testing Nunjucks templates with live HTML preview. Enter your Nunjucks template and JSON data, then see the rendered output instantly in a real DOM element.

## Features

- **Live Preview**: Real-time HTML rendering in an iframe
- **Three-Panel Layout**: Template input, JSON data input, and HTML output
- **Error Handling**: Clear error messages for invalid JSON or template syntax
- **Keyboard Shortcuts**: Press Ctrl+Enter (or Cmd+Enter on Mac) to render
- **No Server Required**: Runs entirely in the browser
- **Example Templates**: Includes sample data to get started quickly

## Usage

1. Open `index.html` in your web browser
2. Edit the Nunjucks template in the left panel
3. Modify the JSON data in the middle panel
4. Click "Render" or press Ctrl+Enter to see the output
5. The rendered HTML appears in the right panel

## Example

**Template:**
```nunjucks
<h1>{{ title }}</h1>
<ul>
{% for item in items %}
  <li>{{ item.name }} - {{ item.price }}</li>
{% endfor %}
</ul>
```

**Data:**
```json
{
  "title": "My Shop",
  "items": [
    { "name": "Apple", "price": "$1.00" },
    { "name": "Banana", "price": "$0.50" }
  ]
}
```

**Output:**
```html
<h1>My Shop</h1>
<ul>
  <li>Apple - $1.00</li>
  <li>Banana - $0.50</li>
</ul>
```

## Installation

No installation required! Just clone the repository and open `index.html` in your browser.

```bash
git clone https://github.com/TorstenC/instant.njk.git
cd instant.njk
# Open index.html in your browser
```

## Development

The project uses:
- Nunjucks 3.2.4 (browser version included)
- Pure HTML, CSS, and JavaScript (no build step required)

## License

MIT License - see LICENSE file for details
