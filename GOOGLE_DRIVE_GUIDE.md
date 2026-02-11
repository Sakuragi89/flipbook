# Google Drive Integration Guide

Add images from Google Drive to your flipbook without uploading them to GitHub!

## 🎯 Quick Start

### Method 1: Using the Admin Panel (Easiest)

1. **Get your Google Drive image link:**
   - Open Google Drive
   - Right-click on an image file
   - Click "Get link" or "Share"
   - Set to "Anyone with the link can view"
   - Copy the link

2. **Add to Admin Panel:**
   - Go to `admin.html`
   - Scroll to "🔗 Google Drive Links" section
   - Paste your link
   - Click "➕ Add Drive Link"

3. **Update index.html:**
   - The admin panel will show you the code in browser console
   - Copy that code and paste it into your `index.html`
   - Upload the updated `index.html` to GitHub

### Method 2: Manual Configuration

1. **Get shareable links** for all your images

2. **Edit index.html** - Find this section:
```javascript
const GDRIVE_CONFIG = {
    enabled: false,
    folderLinks: []
};
```

3. **Update it to:**
```javascript
const GDRIVE_CONFIG = {
    enabled: true,
    folderLinks: [
        "https://drive.google.com/file/d/YOUR_FILE_ID_1/view",
        "https://drive.google.com/file/d/YOUR_FILE_ID_2/view",
        "https://drive.google.com/file/d/YOUR_FILE_ID_3/view"
    ]
};
```

4. **Save and upload** to GitHub

## 📝 Supported Link Formats

The flipbook automatically converts these formats:

✅ **File links:**
```
https://drive.google.com/file/d/1ABC123xyz/view?usp=sharing
```

✅ **Open links:**
```
https://drive.google.com/open?id=1ABC123xyz
```

All are automatically converted to direct image URLs!

## 🎨 How to Get Google Drive Image Links

### For Individual Images:

1. Upload image to Google Drive
2. Right-click the image → "Get link"
3. Change to "Anyone with the link" can view
4. Copy the link
5. Add to admin panel or index.html

### For Multiple Images:

**Option A: Individual Links (Recommended)**
- Get shareable link for each image
- Add all links to the configuration

**Option B: Folder Link (Advanced)**
- Share entire folder with "Anyone with the link"
- Note: Requires Google Drive API for folder listing
- Currently, individual file links work best

## 💡 Tips

- ✅ Make sure images are set to "Anyone with the link can view"
- ✅ Test one image first before adding many
- ✅ Links are stored in your browser's localStorage
- ✅ You can mix GitHub uploads AND Google Drive links
- ✅ Drive images load directly - no storage limits!

## 🔄 Combining GitHub + Google Drive

You can use BOTH methods together:

1. **GitHub**: For images you want to keep in your repository
2. **Google Drive**: For large collections or temporary images

Both will appear in your flipbook!

## 🛠️ Troubleshooting

**Images not loading?**
- Check the sharing permission is "Anyone with the link"
- Make sure GDRIVE_CONFIG.enabled is set to `true`
- Check browser console for errors

**Wrong image format?**
- Google Drive supports: JPG, PNG, GIF
- Make sure files are images, not documents

**Too many images?**
- No limit on number of Drive links!
- Performance depends on Google Drive's response time

## 🔒 Privacy Note

- Images are served directly from Google Drive
- No copies are made to GitHub
- Anyone with your flipbook link can see the images
- Make sure you're comfortable sharing the images publicly!

## 📱 Mobile Access

Google Drive links work perfectly on mobile devices too!

---

**Enjoy unlimited image hosting with Google Drive! 🚀**
