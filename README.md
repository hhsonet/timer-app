# Exam Timer Browser Extension

A lightweight browser extension that provides a clean, minimalist countdown timer perfect for exams, study sessions, and time management. Features a beautiful circular progress indicator and intuitive controls.

![Exam Timer Extension Preview](/screenshots/preview.png)

## Features

- 🎯 Circular progress visualization
- ⚡ Quick preset timers (1h, 2h, 5m, 15m)
- ⌨️ Custom time input (hours, minutes, seconds)
- ⏯️ Pause/Resume functionality
- 🔄 Reset option
- 🎨 Clean, modern interface
- 📱 Responsive design
- 🔔 Time's up notification
- 🌙 Works in background

## Installation

### Chrome Web Store
1. Visit the [Chrome Web Store](https://chrome.google.com/webstore)
2. Search for "Exam Timer"
3. Click "Add to Chrome"

### Manual Installation (Developer Mode)
1. Download or clone this repository
2. Open Chrome and go to `chrome://extensions/`
3. Enable "Developer mode" in the top right
4. Click "Load unpacked" and select the extension directory

## Usage

1. Click the extension icon in your browser toolbar
2. Set your timer using either:
   - Input fields for hours, minutes, and seconds
   - Preset time buttons (1h, 2h, 5m, 15m)
3. Click "Start" to begin countdown
4. Use "Pause" to temporarily stop
5. "Reset" to clear and start over

The timer will continue running even when the popup is closed. You'll receive a notification when time is up.

## Development

### Project Structure
```
exam-timer-extension/
├── manifest.json
├── popup/
│   ├── index.html
│   ├── style.css
│   └── script.js
├── background/
│   └── background.js
├── icons/
│   ├── icon16.png
│   ├── icon48.png
│   ├── icon128.png
│   └── icon192.png
└── screenshots/
    └── preview.png
```

### Building from Source
1. Clone the repository:
```bash
git clone https://github.com/your-username/exam-timer-extension.git
```

2. Make your modifications to the source code

3. Test locally:
   - Open Chrome
   - Go to `chrome://extensions/`
   - Enable Developer mode
   - Click "Load unpacked"
   - Select the extension directory

### manifest.json
```json
{
  "manifest_version": 3,
  "name": "Exam Timer",
  "version": "1.0.0",
  "description": "A clean, minimalist countdown timer perfect for exams and study sessions",
  "permissions": ["notifications", "storage"],
  "action": {
    "default_popup": "popup/index.html",
    "default_icon": {
      "16": "icons/icon16.png",
      "48": "icons/icon48.png",
      "128": "icons/icon128.png"
    }
  },
  "icons": {
    "16": "icons/icon16.png",
    "48": "icons/icon48.png",
    "128": "icons/icon128.png",
    "192": "icons/icon192.png"
  },
  "background": {
    "service_worker": "background/background.js"
  }
}
```

## Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/YourFeature`
3. Commit your changes: `git commit -m 'Add YourFeature'`
4. Push to the branch: `git push origin feature/YourFeature`
5. Submit a Pull Request

### Development Guidelines
- Follow the existing code style
- Test thoroughly in different browsers
- Update documentation as needed
- Add comments for complex logic

## Support

- Report bugs via [GitHub Issues](https://github.com/your-username/exam-timer-extension/issues)
- For feature requests, open an issue with the "enhancement" label
- Check existing issues before creating new ones

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Icons from [Material Design Icons](https://material.io/icons/)
- SVG progress ring inspired by [Jake Archibald's blog post](https://jakearchibald.com/2013/animated-line-drawing-svg/)

## Privacy Policy

This extension does not collect or transmit any user data. All timer data is stored locally in your browser using the Chrome Storage API.
