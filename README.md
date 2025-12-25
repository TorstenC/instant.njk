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

1. Open `docs/index.html` in your web browser (or visit the GitHub Pages URL)
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

No installation required! Just clone the repository and open `docs/index.html` in your browser.

```bash
git clone https://github.com/TorstenC/instant.njk.git
cd instant.njk
# Open docs/index.html in your browser
```

## Development

The project uses:
- Nunjucks 3.2.4 (browser version included)
- Pure HTML, CSS, and JavaScript (no build step required)

### Project Structure

- `/src` - Source files (index.html, nunjucks.min.js)
- `/docs` - Deployment files for GitHub Pages (generated via `npm run deploy`)

### Deployment

To deploy changes to GitHub Pages:

```bash
# 1. Edit files in /src directory
# 2. Run the deploy script to copy files to /docs
npm run deploy
# 3. Commit and push changes
```

The `npm run deploy` script copies `index.html` and `nunjucks.min.js` from `/src` to `/docs` for GitHub Pages hosting.

## License

MIT License - see LICENSE file for details
