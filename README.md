# Text Extractor for Kali Linux GNOME

A lightweight utility that lets you select a screen area, perform OCR using **Tesseract**, and automatically copy the extracted text to your clipboard. This repository also demonstrates how to package the script as a `.deb` for easy distribution, add a desktop icon/launcher, and set a GNOME keyboard shortcut (e.g., **Super+T**).

---

## Features

- **Area Selection**: Select any portion of the screen to capture.
- **OCR Extraction**: Automatically runs [Tesseract OCR](https://github.com/tesseract-ocr/tesseract).
- **Clipboard Copy**: Places the recognized text into your clipboard for easy pasting.
- **Desktop Notification**: Informs you once extraction is complete.
- **Installable**: Provides a guide to package as a `.deb` and integrate into your system menu with an icon.
- **Optional Keyboard Shortcut**: Can be configured (via GNOME’s keyboard settings or a dconf override) to launch with **Win+T** or any other key combo.

---

## Requirements

- **Kali Linux GNOME** (or any Debian-based GNOME environment)
- `maim` (screenshot tool)
- `tesseract-ocr` (OCR engine)
- `xclip` (clipboard utility)
- `libnotify-bin` (desktop notifications)

Install them with:

```bash
sudo apt update
sudo apt install maim tesseract-ocr xclip libnotify-bin
