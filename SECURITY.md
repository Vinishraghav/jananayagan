# 🔒 Security & Privacy Guide

This guide explains how to use Jananayagan securely and privately, so hackers cannot track you or find your video.

## Table of Contents
1. [Threat Model](#threat-model)
2. [Privacy Features](#privacy-features)
3. [Security Checklist](#security-checklist)
4. [Advanced Protection](#advanced-protection)
5. [Common Threats & Mitigation](#common-threats--mitigation)
6. [Best Practices](#best-practices)

---

## Threat Model

### Who might track you?
1. **Video hosting provider** (Google Drive, Dropbox, etc.)
2. **Your ISP** (Internet Service Provider)
3. **Network administrators** (if on company/school network)
4. **Malicious hackers** (if via phishing or malware)
5. **Nation-state actors** (if highly targeted)

### What data can be exposed?
- Your IP address
- Your location (approximate)
- Your device fingerprint
- Your browsing history
- Your video URL (which might identify content)

### How Jananayagan protects you
- No tracking cookies
- No analytics
- No server-side logging
- No personal data collection
- All processing in your browser
- No URL storage

---

## Privacy Features

### 1. 🔓 → 🔒 Security Mode Toggle

Click the security button to instantly enable:
- Private Mode (no sharing, no tracking)
- Right-click protection (prevent downloads)
- CORS Proxy (hide from video host)
- Security warnings

### 2. Private Mode

When enabled:
- ✅ No social media sharing buttons
- ✅ No URL sharing/copying features
- ✅ Prevents accidental link exposure
- ✅ Blocks all tracking attempts
- ✅ Clears URL on page close

### 3. Password Protection

Add a password to your video:
1. Check "Password Protection"
2. Set a 4+ character password
3. Video will require password to play
4. Share via encrypted channel (Signal, WhatsApp, etc.)

### 4. CORS Proxy

Hides your identity from the video host:
- Your requests appear to come from a proxy server
- Video host sees proxy's IP, not yours
- Additional privacy layer
- ⚠️ May slightly reduce speed

### 5. Right-Click Protection

Prevents casual download attempts:
- Disables right-click context menu on player
- Shows security message instead
- ⚠️ Note: Advanced users can still capture video

---

## Security Checklist

### Minimum Security (for sharing with trusted people)
- [ ] Use HTTPS (GitHub Pages automatically)
- [ ] Share link only via direct message
- [ ] Don't post link on public social media
- [ ] Check video host's privacy settings

### Standard Security (recommended for most users)
- [ ] ✅ Enable Private Mode
- [ ] ✅ Use a password
- [ ] ✅ Enable CORS Proxy
- [ ] ✅ Share via encrypted channel
- [ ] ✅ Disable right-click
- [ ] ✅ Regular link rotation

### Maximum Security (for highly sensitive content)
- [ ] ✅ Use VPN (hide IP address)
- [ ] ✅ Enable all security features
- [ ] ✅ Use incognito/private browsing
- [ ] ✅ Multi-factor authentication on video host
- [ ] ✅ Watermark your video
- [ ] ✅ Share link only once to each person
- [ ] ✅ Monitor access logs
- [ ] ✅ Change password regularly

---

## Advanced Protection

### Option 1: VPN (Virtual Private Network)

A VPN hides your real IP address by routing traffic through a VPN server.

**Setup:**
1. Choose a reputable VPN (ProtonVPN, Mullvad, ExpressVPN)
2. Install on your device
3. Connect to VPN before accessing video
4. Your real IP is now hidden from everyone

**Benefits:**
- ✓ Hides IP from video host
- ✓ Hides IP from ISP
- ✓ Encrypts all traffic
- ✓ Works with all websites

**Cost:** Most have free or paid options

### Option 2: Tor Browser

The Tor Browser routes your traffic through multiple servers, providing maximum anonymity.

**Setup:**
1. Download Tor Browser from torproject.org
2. Open this site in Tor Browser
3. Your traffic is routed anonymously

**Benefits:**
- ✓ Extreme anonymity
- ✓ Hide location
- ✓ Multiple layers of encryption

**Drawbacks:**
- ✗ Slower speeds
- ✗ Some sites block Tor

### Option 3: Incognito/Private Window

Use your browser's private browsing mode.

**Setup:**
- Chrome: Ctrl+Shift+N (Windows) or Cmd+Shift+N (Mac)
- Firefox: Ctrl+Shift+P (Windows) or Cmd+Shift+P (Mac)
- Safari: Cmd+Shift+N (Mac)

**Benefits:**
- ✓ No browser history saved
- ✓ No cookies stored
- ✓ No tracking enabled

**Limitations:**
- ✗ ISP can still see your traffic
- ✗ VPN not included

### Option 4: Privacy-Focused Browser

Use browsers designed for privacy:
- **Brave**: Blocks trackers, ads, fingerprinting
- **Firefox**: Privacy-focused with strong settings
- **DuckDuckGo**: Privacy search alternative

---

## Common Threats & Mitigation

### Threat 1: ISP Tracking

**Risk:** Your ISP can see what websites you visit

**Mitigation:**
- Use VPN (Best)
- Monitor ISP privacy policy
- Consider privacy-friendly ISP
- Contact ISP about opt-out options

**Cost:** VPN $3-12/month or free options

---

### Threat 2: Video Host Tracking

**Risk:** Google Drive, Dropbox can see your IP and access patterns

**Mitigation:**
- Enable CORS Proxy on this player
- Use VPN to hide IP
- Choose privacy-friendly host (not Google/Dropbox)
- Use self-hosted or encrypted services

**Options:**
- Bunny CDN: $0.01/GB (privacy-friendly)
- Wasabi: $6.99/month (no tracking)
- Nextcloud: Self-hosted (maximum control)

---

### Threat 3: Browser Fingerprinting

**Risk:** Advertisers can identify you by your browser configuration

**Mitigation:**
- Use Firefox with privacy settings
- Use Brave browser
- Disable JavaScript (if possible)
- Use extension like uBlock Origin

---

### Threat 4: Phishing

**Risk:** Fake links that look like legitimate video sharing

**Mitigation:**
- Only use the official GitHub Pages URL
- Check URL carefully before entering password
- Don't click links from untrusted sources
- Enable password protection

---

### Threat 5: Video Recording

**Risk:** Someone recording your screen while watching

**Mitigation:**
- Right-click protection (deters casual recording)
- Watermark your video
- Share only with people you trust
- Monitor who has access

---

## Best Practices

### 1. Use Multiple Layers of Protection

Don't rely on one security feature. Combine:
- VPN + this player
- Password + CORS proxy
- Private mode + incognito window
- VPN + password + right-click protection

### 2. Share Carefully

- ✅ Do: Share via Signal, WhatsApp, or encrypted email
- ✅ Do: Share with known, trusted people only
- ✅ Do: Use a password for sensitive content
- ✅ Do: Provide access to one person at a time

- ❌ Don't: Post link on Facebook, Twitter, Reddit
- ❌ Don't: Email in plain text
- ❌ Don't: Use public messaging apps
- ❌ Don't: Share link on public forums

### 3. Monitor Access

If your video host supports it:
- Check access logs regularly
- Look for unusual viewing patterns
- Revoke links if not used in timeframe
- Rotate passwords periodically

### 4. Protect Your Video Content

Before uploading:
- Add watermark with your name/date
- Disable video downloading on host
- Set restricted sharing permissions
- Consider encryption

### 5. Device Security

- Keep OS and browser updated
- Use antivirus/malware protection
- Disable unnecessary extensions
- Clear browser cache regularly
- Use password manager

### 6. Network Security

- Avoid public WiFi for sensitive videos
- Use VPN on public WiFi
- Disable automatic WiFi connection
- Be aware of network administrator access
- Use HTTPS everywhere

---

## Comparison: Security Levels

| Aspect | Minimum | Standard | Maximum |
|--------|---------|----------|---------|
| VPN | No | Optional | ✓ Yes |
| Password | No | ✓ Yes | ✓ Yes |
| Private Mode | No | ✓ Yes | ✓ Yes |
| CORS Proxy | No | ✓ Yes | ✓ Yes |
| Incognito Window | No | Optional | ✓ Yes |
| Encryption Channel | Basic | ✓ Yes | ✓ Yes |
| Tor Browser | No | No | ✓ Yes |
| Watermark | No | Optional | ✓ Yes |
| Link Expiry | No | No | ✓ Yes |
| Access Logs | No | Optional | ✓ Yes |

---

## FAQs

**Q: Can hackers intercept my video URL?**
A: Only if sent over unencrypted channels. Mitigation: Use encrypted messaging (Signal, WhatsApp), not email or SMS.

**Q: Can the GitHub Pages server track me?**
A: No. GitHub doesn't collect visitor data. All video URL processing happens in your browser.

**Q: Is password protection enough?**
A: Not alone. Combine with VPN and private transmission. A strong password is not enough for highly sensitive content.

**Q: Can someone screen record my video?**
A: Yes, but the video will be recorded from their screen, not your player. Right-click protection doesn't prevent this.

**Q: Does CORS Proxy prevent all tracking?**
A: No. Your ISP can still see you're accessing a video. Use VPN for complete privacy.

**Q: Can GitHub see my video URL?**
A: No. Your video URL is stored only in your browser's URL bar. GitHub only sees a request to /jananayagan

**Q: What's the most secure way to share?**
A: VPN + Password + Private Mode + Signal + Tor Browser

**Q: Should I use my real name?**
A: No. Create an anonymous account if uploading video anonymously.

---

## Recommended Security Stack

### For Most Users (Good Privacy)
```
VPN + Your Player (Private Mode) + Password
```
Cost: $0-12/month
Time: 10 minutes to set up
Privacy Level: 9/10

### For Journalists & Activists (Maximum Privacy)
```
Tor Browser + VPN + Your Player (all features) + Self-hosted video + Signal for sharing
```
Cost: Free to $50/month
Time: 1-2 hours to set up
Privacy Level: 10/10

### For Business (Enterprise Security)
```
Corporate VPN + Your Player + Password + Watermark + Access monitoring + Encryption
```
Cost: Varies
Time: Custom setup
Privacy Level: 10/10

---

## Resources

- **VPN Reviews**: https://privacyguides.org/en/vpn/
- **Browser Privacy**: https://privacyguides.org/en/browsers/
- **Tor Project**: https://www.torproject.org
- **OWASP Privacy**: https://cheatsheetseries.owasp.org/
- **EFF Privacy**: https://www.eff.org/deeplinks/topic/privacy

---

## Support

For security questions:
- Review the FAQ above
- Check GitHub issues: https://github.com/Vinishraghav/jananayagan/issues
- Consult privacy resources above

---

## Disclaimer

This guide provides best practices, but no system is 100% secure. For extremely sensitive content, consult a security professional.

**Remember:** Privacy is a right. Use these tools responsibly.

---

**Last Updated:** April 2026
**Author:** Jananayagan Security Team
**Status:** Actively Maintained
