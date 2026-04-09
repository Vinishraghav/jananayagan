# 🎬 Jananayagan - Private Video Sharing Platform

**Share your video securely and anonymously** with password protection, privacy controls, and anti-tracking features.

✅ **No tracking • No analytics • No servers logging your data**

---

## 🔒 Privacy First

This platform is designed with **maximum privacy** in mind:
- No cookies, no tracking pixels, no analytics
- All video processing happens in your browser only
- No personal data ever leaves your device
- Open source and transparent code

**[📖 Read our complete Security & Privacy Guide](SECURITY.md)** for detailed protection strategies.

---

## ⚡ Quick Start

1. Upload video to external host (Google Drive, Dropbox, etc.)
2. Copy the public direct URL
3. Open `index.html`, paste URL, click "Load video"
4. Configure privacy settings (Password, Private Mode, CORS Proxy)
5. Push to GitHub and enable GitHub Pages

---

## 📁 Project Files

- `index.html`: Interactive video player with security features
- `styles.css`: Responsive styling with dark theme
- `SECURITY.md`: **Comprehensive privacy & security guide**
- `DEPLOYMENT.md`: Step-by-step deployment instructions
- `HOSTING_GUIDE.md`: Video hosting provider comparison
- `CHECKLIST.md`: Quick verification checklist
- `.gitignore`: Ignores local `jana/` folder so large video file is not committed

---

## 🚀 Features

### 🎮 Video Player
- ✅ HTML5 native player (no plugins needed)
- ✅ Full video controls (play, pause, volume, fullscreen)
- ✅ Video metadata display (duration, progress)
- ✅ Keyboard shortcuts (Space=play/pause, F=fullscreen, M=mute)
- ✅ Responsive design (works on mobile, tablet, desktop)

### 🔐 Security & Privacy
- ✅ **Private Mode**: Disable all sharing and tracking
- ✅ **Password Protection**: Add authentication to your video
- ✅ **CORS Proxy**: Hide your IP from video host
- ✅ **Right-Click Protection**: Prevent downloads
- ✅ **No Tracking**: Zero analytics, zero cookies
- ✅ **HTTP Headers**: Privacy-focused referrer policy

### 📤 Sharing Options
- ✅ URL parameters for pre-loading videos
- ✅ Copy-to-clipboard sharing
- ✅ Encrypted password transmission
- ✅ Share via Signal/WhatsApp (encrypted messaging)

### 🌐 Hosting Flexibility
- ✅ Works with Google Drive, Dropbox, OneDrive
- ✅ Supports AWS S3, Wasabi, Bunny CDN
- ✅ YouTube, Vimeo integration ready
- ✅ Self-hosted video support
- ✅ CORS proxy fallback for blocked hosts

### 📚 Documentation
- ✅ Complete deployment guide
- ✅ Video hosting provider comparison
- ✅ Security & privacy guidelines
- ✅ Quick start checklist
- ✅ Troubleshooting section

## 🔒 Privacy & Security

## Deployment steps

1. Upload your 6.33GB video to a public host such as Google Drive, Dropbox, OneDrive, AWS S3, or another streaming service.
2. Copy the public direct video URL.
3. Open `index.html`, paste the URL into the input field, and click "Load video." 
4. Push this repo to GitHub and enable GitHub Pages on the `main` branch, serving from the root.

## Important note

GitHub cannot host a 6.33GB file directly in a normal repository, so the video must be hosted externally. This website will then play the video from that external source.
