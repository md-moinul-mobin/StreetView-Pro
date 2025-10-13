# StreetView Pro

A lightweight QGIS plugin for opening Google Street View directly from the map canvas with customizable heading and direction.

![QGIS Version](https://img.shields.io/badge/QGIS-3.0+-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0-orange.svg)

## Overview

StreetView Pro allows you to quickly access Google Street View from any location on your QGIS map. Simply click to open Street View, or drag to set a specific viewing direction. The plugin features an intuitive interface with visual feedback and right-click menu integration for enhanced workflow efficiency.

### Visual Guide

![Cover Page](docs/images/Cover%20Page.png)

![Key Features](docs/images/Key%20Features.png)

![Toolbar, Message & Icon](docs/images/Toolbar,%20message%20&%20icon.png)

![Right Click](docs/images/Right%20Click.png)
---

## Installation

### From QGIS Plugin Repository (Recommended)
1. Open QGIS  
2. Go to `Plugins` → `Manage and Install Plugins`  
3. Search for **"StreetView Pro"**  
4. Click **Install Plugin**

### Manual Installation
1. Download the latest release from [GitHub Releases](https://github.com/md-moinul-mobin/StreetView-Pro/releases)  
2. Extract the ZIP file  
3. Copy the `StreetView Pro` folder to your QGIS plugins directory:
   - **Windows:** `C:\Users\YourUsername\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins\`
   - **macOS:** `~/Library/Application Support/QGIS/QGIS3/profiles/default/python/plugins/`
   - **Linux:** `~/.local/share/QGIS/QGIS3/profiles/default/python/plugins/`
4. Restart QGIS  
5. Enable the plugin from `Plugins` → `Manage and Install Plugins`

---

## Usage

### Basic Usage - Click & Drag
1. Click the **StreetView Pro** icon in the toolbar  
2. **Single Click** on the map to open Street View at that location with default heading (North)  
3. **Click and Drag** to set a specific viewing direction — the cyan line shows where you'll be looking  
4. Release to open Google Street View in your browser  

### Context Menu (Right-Click)
Right-click anywhere on the map to access quick actions:
- **Open Street View Here** — Opens Street View at clicked location with default heading  
- **Copy Coordinate** — Copies coordinates in your project's CRS (X, Y format with 1 decimal)  
- **Copy Street View URL** — Copies the full Google Street View URL to clipboard  

### Keyboard Shortcuts
- **ESC** — Cancel the current operation and return to selection mode  

---

## Requirements

- QGIS 3.0 or higher  
- Internet connection (to access Google Street View)  
- Web browser  

---

## Technical Details

- **Plugin Name:** StreetView Pro  
- **Version:** 1.0  
- **QGIS Minimum Version:** 3.0  
- **License:** MIT  
- **Category:** Web  
- **Language:** Python  

### How It Works
1. Captures click/drag events on the QGIS map canvas  
2. Calculates heading angle from drag direction  
3. Transforms coordinates from project CRS to WGS84 (required by Google Maps)  
4. Constructs Google Street View URL with coordinates, heading, pitch, and FOV  
5. Opens URL in default web browser  

---

## Changelog

### Version 1.0 (2025-10-09)
- Initial release  
- Click or drag to open Street View with direction  
- Right-click context menu integration  
- Custom cursor and visual direction indicators  
- CRS support with auto WGS84 transformation  
- ESC key cancellation  
- Auto return to selection mode  

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository  
2. Create a feature branch (`git checkout -b feature/amazing-feature`)  
3. Commit your changes (`git commit -m 'Add amazing feature'`)  
4. Push to the branch (`git push origin feature/amazing-feature`)  
5. Open a Pull Request  

---

## Issues

Found a bug or have a feature request? Please open an issue on [GitHub Issues](https://github.com/md-moinul-mobin/StreetView-Pro/issues).

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## Author

**MD Moinul Mobin**  
- Email: [mdmoinulmobin@gmail.com](mailto:mdmoinulmobin@gmail.com)  
- GitHub: [@md-moinul-mobin](https://github.com/md-moinul-mobin)

---

## Acknowledgments

- Thanks to the QGIS community for their excellent documentation  
- Inspired by the need for quick Street View access during field verification workflows  

---

## Support

If you find this plugin helpful, please:
- ⭐ Star the repository on GitHub  
- 🐛 Report bugs or request features via [Issues](https://github.com/md-moinul-mobin/StreetView-Pro/issues)  
- 📢 Share it with others who might find it useful  

---

**Note:** This plugin uses Google Street View service. Please ensure you comply with Google's Terms of Service when using this plugin.
