# GitHub Pages Hosting Setup

## Step 1: Create Repository Structure

Create a new repository with these files:

```
notion-datetime-widget/
├── index.html          (your widget file)
└── README.md          (documentation)
```

## Step 2: index.html

Save your widget as `index.html` in the repository root.

## Step 3: README.md

```markdown
# Notion Date Time Widget

A beautiful, customizable date and time widget for embedding in Notion pages.

## Features

- 🎨 Clean light gray design
- ⏰ Live time display with seconds
- 📅 Dynamic greeting based on time of day
- 📊 Semester/term progress tracking
- 💬 Motivational status messages
- 📱 Fully responsive design

## Usage

### Embed in Notion

1. Copy your GitHub Pages URL: `https://YOUR-USERNAME.github.io/notion-datetime-widget/`
2. In Notion, type `/embed`
3. Paste the URL
4. Adjust the embed size as needed

### Configuration

Edit the `CONFIG` object in `index.html`:

```javascript
const CONFIG = {
    semesterStart: new Date('2024-08-26'),  // Start date
    semesterEnd: new Date('2024-12-20'),    // End date
    semesterName: 'Fall 2024',              // Display name
    periodName: 'Semester'                   // 'Semester', 'Quarter', 'Term', etc.
};
```

## Customization Examples

### For Academic Quarter
```javascript
periodName: 'Quarter'
semesterName: 'Winter Quarter 2025'
```

### For Work Sprint
```javascript
periodName: 'Sprint'
semesterName: 'Q4 Sprint'
```

### For Year-Long Tracking
```javascript
periodName: 'Year'
semesterName: '2025'
```

## Status Messages

The widget shows different messages based on progress:
- 🚀 Week 1: "Fresh start! Let's make it count."
- 📊 Mid-period: Shows percentage completion
- ⚡ Last 3 weeks: "X weeks remaining. Push through!"
- 🏁 Final week: "Final week! You're almost there!"
- 🎉 After end date: "Semester complete! Time to relax."

## Local Development

1. Clone the repository
2. Open `index.html` in your browser
3. Make changes and refresh to see updates

## License

MIT License - Feel free to use and modify!
```

## Step 4: Enable GitHub Pages

1. Push your files to GitHub:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/notion-datetime-widget.git
git push -u origin main
```

2. Go to repository Settings → Pages
3. Under "Source", select "Deploy from a branch"
4. Select branch: `main` and folder: `/ (root)`
5. Click Save

## Step 5: Get Your URL

Your widget will be live at:
```
https://YOUR-USERNAME.github.io/notion-datetime-widget/
```

Wait 1-2 minutes for deployment, then use this URL in Notion!

## Quick Git Commands

### First Time Setup
```bash
# Navigate to your folder
cd notion-datetime-widget

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit"

# Add remote (replace YOUR-USERNAME and REPO-NAME)
git remote add origin https://github.com/YOUR-USERNAME/REPO-NAME.git

# Push
git branch -M main
git push -u origin main
```

### Making Updates
```bash
# After editing files
git add .
git commit -m "Updated configuration"
git push
```

## Notion Embed Tips

- **Recommended embed height**: 250-300px
- The widget is responsive and works in full-width or column layouts
- Use `/embed` command in Notion, not `/link preview`
- Refresh the Notion page if the widget doesn't update immediately

## Troubleshooting

**Widget not showing in Notion?**
- Wait 2-3 minutes after pushing changes for GitHub Pages to update
- Make sure the repository is public
- Check that GitHub Pages is enabled in Settings
- Try opening the URL directly in your browser first

**Times are wrong?**
- The widget uses the browser's local time zone
- Check your computer's time settings

**Week numbers seem off?**
- Verify the `semesterStart` date in CONFIG
- Week 1 starts on the semesterStart date
