# jananayagan

This repository contains a mini website to showcase your video.

## How it works

- `index.html`: the landing page with an interactive video player.
- `styles.css`: styling for the page.
- `.gitignore`: ignores the local `jana/` folder so the large video file is not committed.

## Deployment steps

1. Upload your 6.33GB video to a public host such as Google Drive, Dropbox, OneDrive, AWS S3, or another streaming service.
2. Copy the public direct video URL.
3. Open `index.html`, paste the URL into the input field, and click "Load video." 
4. Push this repo to GitHub and enable GitHub Pages on the `main` branch, serving from the root.

## Important note

GitHub cannot host a 6.33GB file directly in a normal repository, so the video must be hosted externally. This website will then play the video from that external source.
