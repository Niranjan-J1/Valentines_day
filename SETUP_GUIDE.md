# 🎵 Valentine's Website Setup Guide

## 📁 Step 1: Set Up Your Folder Structure

Create this exact folder structure:

```
valentine_final.html
assets/
├── images/
│   ├── cover.jpg          (Your album cover photo)
│   ├── track1.jpg         (First memory photo)
│   ├── track2.jpg         (Second memory photo)
│   ├── track3.jpg         (Third memory photo)
│   ├── track4.jpg         (Fourth memory photo)
│   ├── track5.jpg         (Fifth memory photo)
│   └── track6.jpg         (Valentine's screen photo)
└── music/
    ├── track1.mp3         (First memory song)
    ├── track2.mp3         (Second memory song)
    ├── track3.mp3         (Third memory song)
    ├── track4.mp3         (Fourth memory song)
    ├── track5.mp3         (Fifth memory song)
    └── track6.mp3         (Valentine's proposal song)
```

## 🖼️ Step 2: Add Your Photos

1. **Prepare your images:**
   - Use photos from your relationship
   - Recommended size: 1000x1000 pixels or larger
   - Supported formats: .jpg, .png, .webp

2. **Name them correctly:**
   - cover.jpg - Album cover (a photo of you two together)
   - track1.jpg - First coffee/meeting
   - track2.jpg - Dancing in the rain memory
   - track3.jpg - Sunrise/late night memory
   - track4.jpg - Car/driving memory
   - track5.jpg - Night adventure memory
   - track6.jpg - Recent photo for Valentine's proposal

3. **Place them in:** `assets/images/` folder

## 🎵 Step 3: Add Your Music

1. **Choose your songs:**
   - Pick meaningful songs for each memory
   - The last track (track6.mp3) will play during the Valentine's proposal!

2. **Supported formats:**
   - .mp3 (recommended)
   - .wav
   - .m4a

3. **Place them in:** `assets/music/` folder

## ✏️ Step 4: Personalize the Text

Open `valentine_final.html` in any text editor (VS Code, Notepad++, etc.)

Find the section with the memories (around line 540) and edit:

```javascript
const memories = [
    {
        title: "nikes",  // Keep or change the track name
        subtitle: "First Coffee Together",  // ← EDIT THIS
        date: "where it all started",  // ← EDIT THIS
        description: "Your personal story here...",  // ← EDIT THIS
        image: "assets/images/track1.jpg",  // ← ADD YOUR IMAGE PATH
        audio: "assets/music/track1.mp3"   // ← ADD YOUR AUDIO PATH
    },
    // ... repeat for all 6 tracks
]
```

**Also update the album cover image (around line 570):**
```javascript
const coverImage = "assets/images/cover.jpg";
```

## 🚀 Step 5: Test Locally

### Option A: Simple Double-Click
- Just double-click `valentine_final.html`
- It will open in your default browser
- ⚠️ Audio might not autoplay due to browser restrictions

### Option B: VS Code Live Server (Recommended)
1. Install VS Code (free)
2. Install "Live Server" extension
3. Right-click `valentine_final.html`
4. Select "Open with Live Server"
5. Website opens at `http://localhost:5500`

### Option C: Python Server
```bash
# In your terminal, navigate to the folder with the HTML file
cd /path/to/your/folder

# Run a simple server
python -m http.server 8000

# Open browser to: http://localhost:8000
```

## 🌐 Step 6: Deploy Online (Share with Your Girlfriend!)

### Option 1: Netlify (Easiest - FREE)

1. Go to [netlify.com](https://netlify.com)
2. Sign up (free)
3. Click "Add new site" → "Deploy manually"
4. Drag your entire folder (with HTML + assets folder)
5. Get instant URL: `yoursite.netlify.app`
6. Send her the link! 💕

**Custom Domain (Optional):**
- In Netlify, go to Domain Settings
- Add your own domain like `loveyou.com`

### Option 2: GitHub Pages (FREE)

1. Create account at [github.com](https://github.com)
2. Create new repository (e.g., "valentine")
3. Upload all files (HTML + assets folder)
4. Go to Settings → Pages
5. Select "main" branch → Save
6. URL: `yourusername.github.io/valentine`

### Option 3: Vercel (FREE)

1. Go to [vercel.com](https://vercel.com)
2. Sign up with GitHub
3. Import your repository
4. Auto-deploys!
5. Get URL: `yoursite.vercel.app`

## 🎨 Quick Customization Tips

### Change Colors
Find the `gradient` values in each memory and update:
```javascript
gradient: "linear-gradient(135deg, #c0a080 0%, #d4b896 100%)"
```
Use [cssgradient.io](https://cssgradient.io/) to create custom gradients!

### Remove Music
If you don't want background music, just leave the `audio: ""` fields empty.

### Add More or Fewer Tracks
- To add more: Copy one memory object and add it to the array
- To remove: Delete one memory object
- The last track always leads to the Valentine's proposal

## ❓ Troubleshooting

**Images not showing?**
- Check file paths match exactly (case-sensitive!)
- Make sure images are in the right folder
- Try using relative paths: `assets/images/track1.jpg`

**Music not playing?**
- Browsers block autoplay - this is normal
- Music should play after user clicks on a track
- Check file format (.mp3 works best)

**Website looks broken?**
- Make sure the HTML file and assets folder are in the same location
- Don't separate them!

## 💡 Pro Tips

1. **Test on mobile:** Open the site on your phone before sending
2. **Compress images:** Use [tinypng.com](https://tinypng.com) to make images load faster
3. **Preview first:** Always check the site yourself before sharing
4. **Keep it secret:** Use incognito mode when testing so it stays a surprise!

## 🎁 Final Checklist

- [ ] All photos added to `assets/images/`
- [ ] All music added to `assets/music/`
- [ ] Text personalized for each memory
- [ ] Album cover image set
- [ ] Tested locally (everything works!)
- [ ] Deployed online
- [ ] Tested the live link
- [ ] Ready to send to your girlfriend! 💕

---

**Need help?** The code has detailed comments throughout. Just search for "PERSONALIZATION GUIDE" in the HTML file!

Good luck! She's going to love this! 🌹
