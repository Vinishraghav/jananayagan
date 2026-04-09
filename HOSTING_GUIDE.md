# Video Hosting Guide

This guide explains how to host your 6.33 GB video file on different platforms and get a direct URL for use with Jananayagan.

## Comparison Table

| Platform | Storage | Free/Paid | Speed | Setup | Direct Link |
|----------|---------|----------|-------|-------|-------------|
| Google Drive | 15 GB free | Free | Good | Easy | Yes |
| Dropbox | 2 GB free | Free | Good | Easy | Yes |
| OneDrive | 5 GB free | Free | Good | Easy | Yes |
| AWS S3 | Unlimited | Paid | Excellent | Medium | Yes |
| Bunny CDN | Unlimited | Paid | Excellent | Medium | Yes |
| Wasabi | Unlimited | Paid ($6.99/mo) | Excellent | Medium | Yes |
| Vimeo | Per plan | Paid | Excellent | Easy | Yes (Pro+) |
| YouTube | Unlimited | Free | Excellent | Very Easy | No (with player) |

---

## 1. Google Drive (Recommended for beginners)

### Pros
- Free (15 GB)
- Very easy to use
- No setup required
- Good speed for streaming

### Cons
- Bandwidth throttling for heavy traffic
- Sharing links can stop working
- Rate limiting after excessive downloads

### Steps

1. Go to [Google Drive](https://drive.google.com)
2. Sign in with your Google account
3. Click **"+ New"** button
4. Select **"Folder upload"** or **"File upload"**
5. Select your `Jananayagan-001.mp4` file
6. Once uploaded, **right-click** the file
7. Select **"Share"**
8. Change permission to **"Viewer"** > **"Anyone with the link"**
9. Copy the sharing link
10. The link will look like:
    ```
    https://drive.google.com/file/d/FILE_ID/view?usp=sharing
    ```

### Get Direct Download Link

Replace `/view` with `/preview` or use this formula:
```
https://drive.google.com/uc?export=download&id=FILE_ID
```

Extract `FILE_ID` from your sharing link and use it above.

### Example
If your share link is:
```
https://drive.google.com/file/d/1a2b3c4d5e6f7g8h9i0j/view?usp=sharing
```

Your direct link is:
```
https://drive.google.com/uc?export=download&id=1a2b3c4d5e6f7g8h9i0j
```

---

## 2. Dropbox

### Pros
- Fast and reliable
- 2 GB free
- Good worldwide presence
- Direct download links

### Cons
- Limited free storage
- Bandwidth limits
- Need Dropbox account

### Steps

1. Go to [Dropbox](https://www.dropbox.com)
2. Sign up or log in
3. Click **"Upload"** button
4. Upload your `Jananayagan-001.mp4` file
5. Once uploaded, **right-click** the file
6. Select **"Share"**
7. Change setting to **"Anyone with this link"**
8. Copy the link
9. Modify the link by changing the ending:
   - Change `?dl=0` to `?dl=1`
   - Or replace with actual direct link format

### Get Direct Link Format
Original:
```
https://www.dropbox.com/s/abc123xyz/Jananayagan-001.mp4?dl=0
```

Direct (add `?dl=1` or change to `?raw=1`):
```
https://www.dropbox.com/s/abc123xyz/Jananayagan-001.mp4?dl=1
```

---

## 3. OneDrive (Microsoft)

### Pros
- 5 GB free
- Part of Microsoft ecosystem
- Fast speeds
- Easy sharing

### Cons
- Limited free storage
- Bandwidth throttling
- Requires Microsoft account

### Steps

1. Go to [OneDrive](https://onedrive.live.com)
2. Sign in with Microsoft account
3. Click **"Upload"** button
4. Upload your `Jananayagan-001.mp4` file
5. **Right-click** the file
6. Select **"Share"**
7. Set to **"Share only the file"** > **"Anyone"** can view
8. Copy the link
9. Modify link to get direct download:
   - Original: `https://1drv.ms/v/s!XXXX`
   - Add `?download=1` at the end

### Get Direct Link

Append `?download=1` to the end:
```
https://1drv.ms/v/s!XXXX?download=1
```

---

## 4. AWS S3 (For High Traffic)

### Pros
- Unlimited storage
- Excellent performance
- Global CDN
- Pay-as-you-go

### Cons
- More technical
- Costs money ($0.09 per GB outbound)
- Setup complexity

### Steps

1. Create [AWS Account](https://aws.amazon.com)
2. Go to **S3** service
3. Click **"Create bucket"**
4. Name your bucket (e.g., `jananayagan-video`)
5. Uncheck **"Block public access"** (if you want public video)
6. Click **"Create"**
7. Upload your video file
8. Right-click file > **"Object actions"** > **"Make public"**
9. Get the **"Object URL"**

### Example S3 URL
```
https://jananayagan-video.s3.amazonaws.com/Jananayagan-001.mp4
```

---

## 5. Bunny CDN (Fast Global Delivery)

### Pros
- Excellent speed globally
- Affordable pricing
- Built for video streaming
- Good uptime

### Cons
- Requires payment ($0.01 per GB)
- More setup required
- Not beginner-friendly

### Steps

1. Create [Bunny CDN Account](https://bunny.net)
2. Go to **Storage** > **Add Storage Zone**
3. Create a storage zone
4. Upload your video via FTP/SFTP
5. Enable CDN for the zone
6. Get the CDN URL:
   ```
   https://your-cdn-url.b-cdn.net/Jananayagan-001.mp4
   ```

---

## 6. Wasabi (Affordable S3-Compatible)

### Pros
- Very affordable ($6.99/month)
- S3-compatible API
- Unlimited storage
- Good performance

### Cons
- Less well-known
- Still requires technical knowledge
- Setup overhead

### Steps

1. Create [Wasabi Account](https://wasabi.com)
2. Create a bucket
3. Upload your video file
4. Set bucket to public
5. Get the direct URL:
   ```
   https://bucket-name.s3.wasabisys.com/Jananayagan-001.mp4
   ```

---

## 7. Vimeo (Professional Video Hosting)

### Pros
- Professional video platform
- Excellent player features
- Good security
- Analytics included

### Cons
- Paid for HD+ ($19-75/month)
- Requires account approval
- May not allow hot-linking

### Steps

1. Create [Vimeo Account](https://vimeo.com)
2. Upload your video
3. Set to **"Public"**
4. Copy video URL from browser
5. For direct link: Extract video ID and use:
   ```
   https://vimeo.com/VIDEO_ID
   ```

**Note:** Vimeo may require their player, limiting direct MP4 access.

---

## 8. YouTube (Unlimited Free)

### Pros
- Unlimited free storage
- Excellent speed
- Massive infrastructure
- Analytics

### Cons
- Requires YouTube account
- Complex private/unlisted sharing
- May require account verification
- Requires YouTube embedded player

### Steps

1. Go to [YouTube](https://youtube.com)
2. Click profile > **"Create a channel"**
3. Click **"Create"** button
4. Upload your video
5. Set to **"Unlisted"** (only people with link can watch)
6. Share the unlisted URL

**Note:** YouTube doesn't support direct MP4 downloads. You must use their embedded player or third-party extraction tools.

---

## Choosing the Best Option

### For Beginners
→ **Google Drive** or **OneDrive**
- No cost
- Easy to set up
- Works out of the box

### For Moderate Use (< 1TB/month)
→ **Dropbox** or **AWS S3**
- Reasonable pricing
- Good speed
- Reliable

### For High Traffic
→ **Bunny CDN** or **Wasabi** + **CloudFront**
- Excellent performance
- Global distribution
- Fast worldwide delivery

### For Professional Video
→ **Vimeo** or **YouTube**
- Built for video hosting
- Professional player
- Analytics and metrics

---

## Troubleshooting

### Link doesn't play
- Test the URL in a new browser tab first
- Ensure it downloads the video, not showing a preview
- Check if link has `?dl=1` or similar parameter
- Try different URL formats

### Slow playback
- Check your hosting bandwidth limits
- Consider upgrading or switching providers
- Use a CDN for better speed
- Test from different locations

### Link stopped working
- Some services disable links after inactivity
- Check sharing permissions
- Refresh or regenerate the link
- Verify file still exists in storage

### CORS errors
- Some servers block browser requests
- Use a CORS proxy: `https://cors-anywhere.herokuapp.com/YOUR_URL`
- Switch to a more friendly hosting service

---

## Cost Comparison

**Free Options:**
- Google Drive: 15 GB free
- OneDrive: 5 GB free
- Dropbox: 2 GB free
- YouTube: Unlimited free

**Paid Options (estimated for 6.33 GB):**
- AWS S3: ~$0.57/month
- Wasabi: $6.99/month (unlimited)
- Bunny CDN: ~$0.06/month (minimal usage)
- Vimeo Pro: $19/month

---

## Next Steps

1. Choose a hosting provider
2. Upload your 6.33 GB video
3. Get the direct URL
4. Paste into Jananayagan and test
5. Share the link!

Questions? Check `DEPLOYMENT.md` for complete setup guide.

Happy streaming! 🎬
