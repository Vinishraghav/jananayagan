# Complete Deployment Guide

This guide will walk you through deploying the Jananayagan video showcase to GitHub Pages and hosting your video.

## Prerequisites

- A GitHub account
- A video file (6.33 GB or any size)
- Access to a file hosting service

## Step 1: Host Your Video

You need to host your large video file externally since GitHub cannot store files larger than 100 MB in most cases.

### Recommended Hosting Options

1. **Google Drive**
   - Free tier: 15 GB
   - Unlimited with Google Workspace
   - Easy sharing and link generation
   - See `HOSTING_GUIDE.md` for detailed instructions

2. **Dropbox**
   - Free tier: 2 GB
   - Plus plan: 2 TB
   - Excellent uptime and speed
   - Direct download links available

3. **OneDrive**
   - Free tier: 5 GB
   - Microsoft 365: 1 TB+
   - Fast and reliable
   - Good for Microsoft ecosystem users

4. **AWS S3**
   - Pay-as-you-go pricing
   - Unlimited storage
   - Best for high traffic
   - More technical setup required

5. **Bunny CDN**
   - Fast global CDN
   - Affordable pricing
   - Optimized for video delivery
   - Excellent uptime

6. **Wasabi**
   - Unlimited storage
   - Low cost ($6.99/month)
   - S3-compatible API
   - Fast delivery

For detailed instructions on each platform, see `HOSTING_GUIDE.md`.

## Step 2: Get Your Video URL

Once uploaded, you need to obtain the **direct public URL** to your video file.

### Important
- The URL must be publicly accessible (no authentication required)
- The URL must point directly to the MP4 file, not a web page
- Test the URL in a new browser tab to confirm it works

If you get a preview page instead of downloading the video, the URL is incorrect. Look for options like:
- "Share link"
- "Get link"
- "Copy sharing link"
- "Public link"

## Step 3: Enable GitHub Pages

1. Go to your GitHub repository: `https://github.com/Vinishraghav/jananayagan`
2. Click **Settings** (gear icon)
3. Scroll down to **Pages** section
4. Under "Source", select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**

Wait 1-2 minutes for GitHub to build your site.

## Step 4: Access Your Video Showcase

Your site will be available at:
```
https://vinishraghav.github.io/jananayagan
```

Replace `vinishraghav` with your GitHub username.

## Step 5: Share Your Video

1. Open the deployed website
2. Paste your video URL into the input field
3. Click "Load video"
4. Use the "Copy Link" button to share the page with your audience

### Sharing with Pre-loaded Video

You can create a direct link with the video already loaded by adding the URL as a query parameter:

```
https://vinishraghav.github.io/jananayagan?v=YOUR_VIDEO_URL_HERE
```

Replace `YOUR_VIDEO_URL_HERE` with your actual video URL.

**Example with URL encoding:**
```
https://vinishraghav.github.io/jananayagan?v=https://example.com/video.mp4
```

## Features

### Built-in Player Features
- ✅ Play/Pause controls
- ✅ Full screen support
- ✅ Volume control
- ✅ Timeline seeking
- ✅ Video duration display
- ✅ Playback progress tracking

### Keyboard Shortcuts
- **Space** - Play/Pause
- **F** - Fullscreen
- **M** - Mute/Unmute

### Sharing
- Copy shareable link to clipboard
- Tweet about the video (with pre-filled message)
- Direct link sharing with pre-loaded video URL

## Troubleshooting

### Video won't load
- Confirm the URL points directly to an MP4 file
- Check that the URL is publicly accessible
- Test opening the URL in a new browser tab
- Check browser console for CORS errors
- Some hosts require special link formats for direct playback

### CORS errors
- Some servers block cross-origin requests
- Use a CORS proxy if needed: `https://cors-anywhere.herokuapp.com/`
- Consider switching to a more CDN-friendly host

### Slow playback
- Your hosting provider may have bandwidth limits
- Consider upgrading your hosting plan
- Use a CDN for faster delivery (Bunny, Cloudflare, AWS CloudFront)

### File too large
- GitHub Pages has no storage limit for the HTML/CSS/JS
- Only the video URL matters (hosted externally)
- Your video can be any size on external hosting

## Custom Domain (Optional)

To use your own domain instead of GitHub Pages URL:

1. Go to repository **Settings** > **Pages**
2. Under "Custom domain", enter your domain
3. Add DNS records to your domain provider pointing to GitHub's servers
4. GitHub will provide the exact DNS records needed

See GitHub's documentation for detailed custom domain setup.

## Maintenance

### Updating Video
1. Upload new video to your hosting service
2. Get the new URL
3. Paste the new URL into the player

### Updating Website
Make changes to `index.html` or `styles.css` in the repository:

```bash
git add index.html styles.css README.md
git commit -m "Update website"
git push origin main
```

GitHub Pages will automatically redeploy within 1-2 minutes.

## Security Notes

- Your video URL is stored in the browser's address bar
- It is NOT sent to any server or tracked
- For sensitive videos, ensure your hosting service has proper access controls
- Use HTTPS-only hosting services
- Consider adding password protection to your hosting service if available

## Performance Tips

1. **Reduce video file size** using compression tools
2. **Use H.264 codec** for best compatibility
3. **Enable CDN** on your hosting service
4. **Monitor bandwidth** for unexpected costs
5. **Test from different locations** to ensure speed

## Support

For issues or questions:
- Check `HOSTING_GUIDE.md` for host-specific help
- Review GitHub Pages documentation: https://docs.github.com/en/pages
- Check browser console for error messages (F12 key)
- Verify your video URL one more time

## Next Steps

1. ✅ Host your video (see `HOSTING_GUIDE.md`)
2. ✅ Enable GitHub Pages (see Step 3 above)
3. ✅ Load and test your video
4. ✅ Share the link with your audience

Happy streaming! 🎬
