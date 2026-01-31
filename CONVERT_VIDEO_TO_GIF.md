# How to Convert Your Logo Video to GIF for Email Signature

Email signatures require GIF format for animations. Here are three ways to convert your `copy_409A1D28-C47E-480A-B327-241ED236AAFB.mov` file:

## Method 1: Using FFmpeg (Recommended - Best Quality)

If you have FFmpeg installed or can install it:

```bash
# Install FFmpeg (if not already installed)
# On macOS with Homebrew:
brew install ffmpeg

# Convert to high-quality GIF
ffmpeg -i copy_409A1D28-C47E-480A-B327-241ED236AAFB.mov \
  -vf "fps=15,scale=160:-1:flags=lanczos" \
  -c:v gif \
  logo-animation.gif
```

For even better quality with palette optimization:

```bash
ffmpeg -i copy_409A1D28-C47E-480A-B327-241ED236AAFB.mov \
  -vf "fps=15,scale=160:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" \
  logo-animation.gif
```

## Method 2: Online Converters (Easiest)

Visit any of these free online converters:
- https://ezgif.com/video-to-gif
- https://convertio.co/video-gif/
- https://cloudconvert.com/mov-to-gif

Steps:
1. Upload your `copy_409A1D28-C47E-480A-B327-241ED236AAFB.mov` file
2. Adjust settings (recommended: 15-20 fps, width 80-160px)
3. Download the resulting GIF as `logo-animation.gif`

## Method 3: Using macOS Built-in Tools

1. Open the video in QuickTime Player
2. Trim if needed (Edit > Trim)
3. File > Export As > choose a format
4. Then use an online converter to finalize to GIF

---

# How to Add the Signature to Your Email Client

## Gmail
1. Open Gmail Settings
2. Scroll to "Signature" section
3. Click "Create new"
4. Copy the HTML code from `signature-inline.html`
5. Paste into the signature box
6. Upload your `logo-animation.gif` and replace the placeholder

## Apple Mail
1. Mail > Settings > Signatures
2. Click the + button to create a new signature
3. Uncheck "Always match my default message font"
4. Open `signature-inline.html` in a browser
5. Select All, Copy, and Paste into the signature field

## Outlook
1. File > Options > Mail > Signatures
2. Click "New" to create a signature
3. Open `signature-inline.html` in a browser
4. Select, Copy, and Paste the signature

## Important Notes

- GIF file size should be under 50KB for email compatibility
- Recommended dimensions: 80-160 pixels wide
- Frame rate: 10-15 fps is sufficient for logos
- Loop the animation infinitely
- Test your signature by sending emails to yourself first
