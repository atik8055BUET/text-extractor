# Text Extractor – Debian Package

A simple Bash-based text extractor for Kali Linux GNOME (Debian-based). Captures a user-selected area of the screen, runs OCR via Tesseract, and copies the extracted text to the clipboard.

## Installation

1. **Download the `.deb` file**

2. **Install** using `dpkg`:

   ```bash
   sudo dpkg -i text-extractor.deb
   sudo apt-get install -f
   ```
   
To launch the text extractor with **Win+T (windows+T)**, run:

```bash
gsettings set org.gnome.settings-daemon.plugins.media-keys custom-keybindings \
"['/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/']"

gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:"/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/" name "Text Extractor"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:"/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/" command "/opt/text-extractor/text_extractor.sh"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:"/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/" binding "<Super>t"
```

After this, press **Win+T** to run the text extractor. 

> **Note**: If you already have a shortcut bound to `<Super>t` or `windows+t`, remove or change it before running these commands.

## Usage

1. **Select an area**: The screen selection tool appears.
2. Once selected, **OCR** processes the screenshot.
3. The **extracted text** goes directly to your clipboard.
4. A **notification** confirms success.

## Troubleshooting

- **Missing Dependencies**: run this,

```bash
sudo apt update                                        
sudo apt install maim tesseract-ocr xclip libnotify-bin
```
  
- **No GUI Session**:  
  If the keyboard shortcut doesn’t work, ensure you’re running GNOME and that no other shortcuts conflict with `<Super>t`.

---

**Enjoy quick OCR from your screen!**

## Author
MD Atikul Islam
CSE,BUET
atikul.bn@gmail.com
