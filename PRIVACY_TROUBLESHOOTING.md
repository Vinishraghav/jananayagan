# 🛠️ Privacy Troubleshooting Guide

**Diagnose and fix common privacy and security issues.**

---

## Problem: Password Not Working

### Symptom
- Enter password, click unlock, nothing happens
- Video doesn't load

### Solutions

**Solution 1: Clear Browser Cache**
- Chrome: Ctrl+Shift+Delete → Click "All time" → Check "Cookies" → Clear
- Firefox: Ctrl+Shift+Delete → "Everything" → Clear
- Then refresh page and try again

**Solution 2: Check JavaScript Console**
- Press F12 to open Developer Tools
- Click "Console" tab
- Look for red error messages
- Report error to GitHub Issues

**Solution 3: Try Private/Incognito Window**
- Open new private window
- Paste full URL with video parameter
- Set password again

---

## Problem: CORS Proxy Not Hiding IP

### Symptom
- Checked "Hide IP" but still see real IP when accessing video
- CORS proxy errors in console

### Solutions

**Solution 1: Verify Proxy is Enabled**
- Check that "CORS Proxy" checkbox is checked (blue ✓)
- Check "Hide IP" checkbox as well
- Reload page

**Solution 2: Use VPN Instead**
- CORS proxy sometimes blocked by video host
- Download VPN app (ProtonVPN, Mullvad, ExpressVPN)
- Connect to VPN before accessing video
- This hides IP from ISP too

**Solution 3: Alternative Hosting**
- CORS issues often with Google Drive
- Try Bunny CDN, Wasabi, or AWS S3 instead
- These providers are more privacy-friendly

---

## Problem: Video Won't Load

### Symptom
- Click "Load video" but video doesn't appear
- Video player shows as blank/black

### Solutions

**Check 1: Invalid Video URL**
- Make sure URL is a **direct video link**, not a folder link
- Should end in `.mp4`, not containing `/view?` or `/open?`
- For Google Drive: Use the share link converter to get direct link
- For Dropbox: Add `?dl=1` to end of share link

**Check 2: Video Host Blocked by CORS**
- Enable "CORS Proxy" checkbox
- Try adding `?v=` parameter to end of URL to bust cache

**Check 3: Mixed Content Error**
- If accessing via HTTPS but video URL is HTTP
- Enable CORS Proxy
- Or ask video host to use HTTPS link

**Check 4: Video File Issues**
- Make sure video file actually exists at URL
- Try opening URL in new browser tab
- Should see video player or download prompt
- If blank, URL is invalid

**Check 5: Browser Compatibility**
- Chrome, Firefox, Safari, Edge all supported
- Try different browser to confirm
- Check browser console for errors (F12)

---

## Problem: Right-Click Protection Not Working

### Symptom
- Right-click still shows context menu
- Can still download video

### Solutions

**Important Note:** Right-click protection is **not foolproof**
- Advanced users can bypass this with browser tools
- It only prevents casual downloads
- Nothing stops screen recording or network capture

**To Improve Protection:**

1. **Use Password Protection**
   - Password prevents unauthorized access
   - Set in "Private Mode" section

2. **Use Watermark**
   - Edit your video file before uploading
   - Add timestamp/name watermark
   - Identifies leakers if recorded

3. **Monitor Access**
   - If using self-hosted videos
   - Check server logs for suspicious requests
   - Limiting access per day

---

## Problem: Privacy Mode Disables Video Sharing

### Symptom
- Enabled "Private Mode"
- Share button disappeared
- Can't share video URL anymore

### Status
**This is by design!** Private Mode disables all sharing to maximize privacy.

### Solutions

**Option 1: Share via Copy-Paste**
- Disable "Private Mode"
- Use "Copy Link" button to get URL
- Send via encrypted channel (Signal, WhatsApp)
- Re-enable Private Mode after sharing

**Option 2: Use Password Instead of Private Mode**
- Uncheck "Private Mode"
- Check "Password Protection"
- Video still shareable but requires password
- Only person with password can access

**Option 3: Brief Sharing Window**
- Enable Private Mode for maximum privacy
- Disable Private Mode only when sharing
- Enable again after sharing
- Rotate video URL regularly

---

## Problem: HTTPS Certificate Warning

### Symptom
- Browser shows security warning
- "Not secure" message in URL bar
- Red lock icon

### Causes & Solutions

**Cause 1: You're on github.io domain**
- GitHub Pages uses HTTPS by default
- You should be getting green lock
- Clear cache and refresh

**Cause 2: Video URL is HTTP**
- Hosting provider doesn't support HTTPS
- Use "CORS Proxy" checkbox to bypass

**Cause 3: Browser extension issue**
- Disable browser extensions temporarily
- Try in incognito window
- Try different browser

---

## Problem: Someone Shared My Video Without Permission

### Solutions

**Immediate Actions:**
1. **Change video hosting URL**
   - Delete old video from host
   - Upload new copy with different URL
   - Share new URL only with authorized people

2. **Password protect**
   - Even if URL leaks, requires password
   - Change password frequently
   - Only share with close friends

3. **Report & Document**
   - Screenshot who shared it
   - Document where you found it
   - In extreme cases, send DMCA takedown

**Prevention:**
- Don't share URL widely
- Use password protection
- Share with one person at a time
- Watermark your video
- Rotate URL monthly

---

## Problem: I Forgot My Password

### Symptom
- Set password but forgot what it was
- Can't unlock video anymore
- Locked out of own content

### Solutions

**Solution 1: No Recovery (By Design)**
- Passwords are encrypted, can't be recovered
- There is no "forgot password" for security reasons
- This is intentional for maximum privacy

**Solution 2: Clear Data & Reset**
- In Developer Tools (F12), go to "Application"
- Find "Local Storage" → Click your domain
- Find "videPassword" entry → Delete it
- Refresh page - password is now cleared

**Solution 3: Use Incognito Window**
- Open new incognito/private window
- No LocalStorage = no password stored
- Set new password

**Solution 4: Re-upload Video**
- Change video URL to new hosting location
- Clear old URL from your memory
- Set new password
- Share new URL

---

## Problem: Slow Video Playback

### Symptom
- Video stutters, buffers, or lags
- Playback speed is slow
- Audio/video out of sync

### Causes & Solutions

**Cause 1: Slow Internet**
- Check internet speed: speedtest.net
- Should have at least 5 Mbps for HD video
- Move closer to WiFi router
- Restart modem/router

**Cause 2: Video File Too Large**
- Compress video before uploading
- Use FFmpeg to create smaller file
- Command: `ffmpeg -i input.mp4 -b:v 2000k output.mp4`

**Cause 3: CORS Proxy Overhead**
- CORS Proxy adds latency
- Disable if not needed
- Use faster video host (Bunny CDN fastest)

**Cause 4: Hosted Video Issues**
- Google Drive is slow for videos
- Try Bunny CDN (fastest, $0.01/GB)
- Or AWS S3 with CloudFront

**Cause 5: Browser Tabs**
- Close other browser tabs
- They consume bandwidth and CPU
- Restart browser completely

---

## Problem: "Mixed Content" Error

### Symptom
- Browser shows warning
- Video won't load
- Console shows "Mixed Content" error

### Cause
- Website uses HTTPS but video URL uses HTTP
- Browsers block this for security

### Solutions

**Solution 1: Use HTTPS Video URL**
- Ask video host for HTTPS link
- Most providers support HTTPS now
- Replace `http://` with `https://`

**Solution 2: Enable CORS Proxy**
- Check "CORS Proxy" checkbox
- This routes through secure proxy
- Works around the issue

**Solution 3: Self-Host Video**
- Upload to Bunny CDN, AWS S3, or Wasabi
- All support HTTPS
- More private than Google Drive anyway

---

## Problem: VPN Causes Video Not to Load

### Symptom
- When VPN is ON, video won't load
- When VPN is OFF, video loads fine

### Causes & Solutions

**Cause 1: Video Host Blocks VPN IPs**
- Some hosts block VPN/proxy IPs
- Try different VPN server location
- Switch to different VPN provider

**Cause 2: VPN Configured Wrong**
- Some VPNs split tunnel (leak real IP)
- Check VPN settings
- Enable "Kill Switch" to prevent leaks

**Cause 3: ISP Blocks Specific VPN**
- Some ISPs block known VPN services
- Try Tor Browser or different VPN
- Use stealth/obfuscation mode if available

**Solution:**
- Use Bunny CDN - works with any VPN
- Or use Tor Browser for maximum privacy
- Or use different VPN service

---

## Problem: Browser Crashes or Freezes

### Symptom
- Tab freezes when loading large video
- Browser becomes unresponsive
- Had to force close browser

### Causes & Solutions

**Cause 1: Video File Too Large**
- Large 4K videos can freeze browser
- Compress video to smaller size
- Max recommended: 500MB file

**Cause 2: Out of Memory**
- Too many tabs open
- Browser not enough RAM
- Close other programs
- Restart browser

**Cause 3: Browser Bug**
- Update browser to latest version
- Try different browser
- Disable extensions temporarily

---

& Success: Video loads, plays smoothly, password works

## Quick Troubleshooting Flowchart

```
Issue: Problem with video sharing?

1. Video won't load?
   → Copy-paste URL in new tab
   → Is it a direct .mp4 link?
   → If no: Get direct link, try again
   → If yes: Enable CORS Proxy checkbox

2. Password not working?
   → Clear browser cache
   → Try incognito window
   → Check developer console for errors

3. Slow playback?
   → Check internet: speedtest.net
   → Disable CORS Proxy
   → Switch to faster host (Bunny CDN)

4. IP not hidden?
   → Enable both: CORS Proxy + VPN
   → VPN alone is more reliable
   → Use Tor Browser for maximum hiding

5. Someone stole my video?
   → Change video URL immediately
   → Password protect next time
   → Use watermark to identify leakers
```

---

## Getting Help

If your issue isn't listed above:

1. **Check the FAQ** in [SECURITY.md](SECURITY.md)
2. **Review [DEPLOYMENT.md](DEPLOYMENT.md)** for setup issues
3. **Open issue on GitHub**: https://github.com/Vinishraghav/jananayagan/issues
4. **Browser Console (F12)**: Copy error message to issue

---

**Remember:** If you think it's a privacy issue, assume worst-case and use VPN + Tor + all security features.
