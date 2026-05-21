# ToolHive - Free Online Tools

![ToolHive](https://img.shields.io/badge/ToolHive-v1.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-MVP-brightgreen)

**ToolHive** is a collection of free online tools - no signup required, no limits. All tools run entirely in your browser.

## 🛠️ Available Tools

| Tool | Description |
|------|-------------|
| 📱 **QR Code Generator** | Create QR codes from any text/URL with customizable size and error correction |
| 📋 **JSON Formatter** | Format, validate, beautify, and minify JSON data |
| 🎨 **Color Converter** | Convert colors between HEX, RGB, and HSL formats with live preview |
| 📝 **Text Counter** | Count characters, words, sentences, paragraphs with reading time estimates |
| 🔐 **Base64 Encoder/Decoder** | Encode/decode text and files to/from Base64 format |
| 🔑 **Password Generator** | Generate strong, secure passwords with customizable options |
| 📄 **Lorem Ipsum Generator** | Generate classic Lorem Ipsum placeholder text |
| 📖 **Markdown Preview** | Write and preview Markdown with live side-by-side editing |

## ✨ Features

- ⚡ **Fast** - All tools run locally in your browser
- 🔒 **Private** - Your data never leaves your device
- 💰 **Free** - No signup, no limits, no premium features
- 📱 **Responsive** - Works on desktop, tablet, and mobile
- 🎨 **Modern UI** - Clean, professional design with Tailwind CSS
- 🔍 **SEO Optimized** - Each page has proper meta tags and Open Graph data

## 📁 Project Structure

```
toolhive/
├── index.html              # Homepage with all tool cards
├── css/
│   └── style.css           # Custom styles (Tailwind supplementary)
├── tools/
│   ├── qr-generator.html    # QR Code Generator
│   ├── json-formatter.html # JSON Formatter/Validator
│   ├── color-converter.html# Color Converter (HEX/RGB/HSL)
│   ├── text-counter.html   # Text/Words/Characters Counter
│   ├── base64.html         # Base64 Encoder/Decoder
│   ├── password-generator.html # Password Generator
│   ├── lorem-ipsum.html    # Lorem Ipsum Generator
│   └── markdown-preview.html # Markdown Editor & Preview
├── package.json            # npm package configuration
├── vercel.json             # Vercel deployment configuration
├── DEPLOY.md               # Deployment instructions
└── README.md               # This file
```

## 🚀 Quick Start

### View Locally

Simply open `index.html` in any modern web browser:

```bash
# Option 1: Direct file open
open index.html

# Option 2: Using Python's HTTP server
python3 -m http.server 8000
# Then visit http://localhost:8000

# Option 3: Using Node.js serve
npx serve .
```

### Deploy to Vercel

See [DEPLOY.md](./DEPLOY.md) for detailed deployment instructions.

## 🎨 Design

- **Primary Color**: `#2563EB` (Blue-600)
- **Secondary Color**: `#1E40AF` (Blue-800)
- **Font Stack**: `system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`
- **Style**: Modern minimalist, white background with blue accents
- **Inspiration**: tinywow.com, ilovepdf.com

## 🔧 Technologies Used

- **HTML5** - Semantic markup
- **Tailwind CSS** (CDN) - Utility-first CSS framework
- **Vanilla JavaScript** - No dependencies for tools
- **External Libraries**:
  - [QRCode.js](https://github.com/davidshimjs/qrcodejs) - QR code generation
  - [marked.js](https://marked.js.org/) - Markdown parsing

## 📈 SEO

Each page includes:
- Unique `<title>` and `<meta description>`
- `<meta keywords>` relevant to the tool
- Open Graph tags for social sharing
- Twitter Card meta tags
- Semantic HTML structure

## 🤝 Contributing

This is an MVP version. Future plans include:
- [ ] More tools (image compression, unit converter, etc.)
- [ ] Dark mode toggle
- [ ] Tool favorites/bookmarks
- [ ] Tool history
- [ ] API endpoints for developers

## 📄 License

MIT License - feel free to use this project for personal or commercial purposes.

---

Made with 🐝 by ToolHive
