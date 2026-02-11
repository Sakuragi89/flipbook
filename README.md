# Screenshot Flipbook - GitHub Pages

A completely free flipbook viewer for screenshots, hosted on GitHub Pages with admin upload functionality.

## 🌟 Features

- ✅ **100% Free** - No paid services required
- 📸 **Screenshot Flipbook** - Beautiful viewer with navigation
- 🔐 **Admin Panel** - Secure upload interface
- 🌍 **Global Access** - Anyone can view your flipbook
- 📱 **Responsive Design** - Works on all devices
- ⌨️ **Keyboard Navigation** - Arrow keys to browse

## 🚀 Quick Setup Guide

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon → "New repository"
3. Name it anything (e.g., `my-flipbook`)
4. Make it **Public**
5. Click "Create repository"

### Step 2: Upload Files

1. Upload these files to your repository:
   - `index.html` (the flipbook viewer)
   - `admin.html` (the admin panel)

2. Create a folder called `screenshots` in your repository
   - This is where uploaded images will be stored
   - You can create it by uploading a dummy file or through GitHub's interface

### Step 3: Enable GitHub Pages

1. Go to your repository Settings
2. Scroll to "Pages" section (left sidebar)
3. Under "Source", select "main" branch
4. Click "Save"
5. Your site will be live at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

### Step 4: Create GitHub Personal Access Token

1. Go to GitHub Settings → Developer Settings → Personal Access Tokens → Tokens (classic)
2. Click "Generate new token (classic)"
3. Give it a name (e.g., "Flipbook Upload")
4. Check the **`repo`** permission (full control of private repositories)
5. Click "Generate token"
6. **Copy the token** (you won't see it again!)

### Step 5: Configure the Viewer

Edit `index.html` and update these lines (around line 131):

```javascript
const GITHUB_CONFIG = {
    owner: 'YOUR_GITHUB_USERNAME',        // Replace with your GitHub username
    repo: 'YOUR_REPO_NAME',               // Replace with your repository name
    branch: 'main',
    path: 'screenshots'
};
```

Commit the changes to your repository.

### Step 6: Upload Screenshots

1. Visit `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/admin.html`
2. Enter your GitHub configuration:
   - GitHub Username
   - Repository Name
   - Branch (usually "main")
   - Personal Access Token (from Step 4)
3. Click "Save Configuration"
4. Upload your screenshots using drag-and-drop or file selection
5. Click "Upload All Screenshots"

### Step 7: View Your Flipbook

Visit `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/` to see your flipbook!

## 📖 How to Use

### For Viewers:
- Click "Next" and "Previous" buttons to navigate
- Use arrow keys (← →) for keyboard navigation
- Click thumbnails to jump to specific pages

### For Admins:
- Access the admin panel at `/admin.html`
- Configure GitHub settings (saved in browser)
- Drag and drop images or click to select
- Upload multiple screenshots at once

## 🔒 Security Notes

- Your GitHub token is stored in your browser's localStorage
- Never share your personal access token
- Only you (the admin) can upload screenshots
- Everyone can view the flipbook (it's public)

## 🛠️ Troubleshooting

**"No screenshots found"**
- Make sure the `screenshots` folder exists in your repository
- Check that your GitHub configuration is correct
- Verify your token has `repo` permissions

**Upload fails**
- Check your token is valid and has correct permissions
- Ensure repository name and username are correct
- Check browser console for error messages

**Images not loading**
- Wait a few minutes for GitHub to process the upload
- Try refreshing the page
- Check that images are in the `screenshots` folder

## 📝 Tips

- Recommended image format: PNG or JPG
- Keep images under 5MB for best performance
- Use descriptive filenames (they're timestamped on upload)
- Images are displayed in alphabetical order

## 🎨 Customization

Feel free to modify the CSS in both HTML files to match your style!

New Features:

🖼️ Click any image to open it in full-screen gallery mode
🔍 Zoom in/out with +/- buttons (up to 500% zoom!)
🖱️ Drag to pan when zoomed in
⌨️ Keyboard shortcuts:

Arrow keys: Navigate between images
+/- keys: Zoom in/out
0 key: Reset zoom
Escape: Close gallery
Enter/Space: Open gallery


🎯 Mouse wheel to zoom
⟲ Reset button to return to 100%

Gallery Controls:

‹ › buttons to navigate while in gallery
× button to close
Zoom controls at the bottom
Dark overlay for better image focus

## 📄 License

Free to use and modify for your own projects!

---

**Enjoy your free screenshot flipbook! 📸✨**
