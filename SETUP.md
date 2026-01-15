# Setup Instructions

This guide will help you set up and deploy your CV repository.

## Initial Setup

### 1. Install Prerequisites

**Quarto** (required)
- Download from [quarto.org](https://quarto.org/docs/get-started/)
- Or install via command line:
  ```bash
  # macOS
  brew install quarto
  
  # Linux
  curl -LO https://quarto.org/download/latest/quarto-linux-amd64.deb
  sudo dpkg -i quarto-linux-amd64.deb
  ```

**R** (optional, for dynamic content)
- Download from [r-project.org](https://www.r-project.org/)

### 2. Clone and Customize

```bash
# Clone your repository
git clone https://github.com/yourusername/cv.git
cd cv

# Update personal information in:
# - README.md (update links and contact info)
# - _quarto.yml (update GitHub and LinkedIn URLs)
# - cv.qmd (your CV content)
```

### 3. Test Locally

```bash
# Render the CV
quarto render

# Preview in browser
quarto preview
```

This will generate:
- `docs/cv.html` - HTML version
- `docs/cv.pdf` - PDF version  
- `docs/cv.docx` - Word version

### 4. Configure GitHub Pages

1. Push your repository to GitHub
2. Go to **Settings** → **Pages**
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/docs`
4. Click **Save**
5. Wait a few minutes for deployment

Your CV will be available at: `https://yourusername.github.io/cv/`

### 5. Enable GitHub Actions

The repository includes a GitHub Actions workflow that automatically renders your CV when you push changes.

1. Go to **Settings** → **Actions** → **General**
2. Under **Workflow permissions**, select:
   - ✅ Read and write permissions
3. Click **Save**

Now every push to `main` will automatically:
- Render your CV
- Deploy to GitHub Pages

## Customization

### Update Styling

Edit `assets/styles.css` to customize colors, fonts, and layout.

### Add a Photo

1. Add your photo to `assets/` (e.g., `assets/profile.jpg`)
2. Update `cv.qmd` to include it:
   ```markdown
   ![](assets/profile.jpg){width=150px}
   ```

### Create Word Template

```bash
quarto pandoc -o assets/custom-reference.docx --print-default-data-file reference.docx
```

Then edit the styles in Word and save.

### Change Theme

Edit `_quarto.yml` and change `theme: cosmo` to another [Bootswatch theme](https://quarto.org/docs/output-formats/html-themes.html):
- `cosmo`, `flatly`, `journal`, `readable`, `sandstone`, etc.

## Workflow

### Daily Updates

```bash
# Edit your CV
vi cv.qmd

# Render locally to preview
quarto render

# Commit and push (triggers auto-deployment)
git add .
git commit -m "Update CV with new project"
git push
```

### Archive Old Versions

```bash
# Before major changes, save current version
cp docs/cv.pdf archive/cv-2025-01.pdf
git add archive/
git commit -m "Archive January 2025 version"
git push
```

## Troubleshooting

### PDF Not Generating

Install LaTeX:
```bash
# Install TinyTeX (recommended)
quarto install tinytex
```

### GitHub Actions Failing

Check the Actions tab for error logs. Common issues:
- Permissions not set correctly
- Missing dependencies in workflow file

### Changes Not Appearing on GitHub Pages

- Wait 2-5 minutes for deployment
- Check Actions tab to see if workflow completed
- Clear browser cache

## Support

- [Quarto Documentation](https://quarto.org/docs/guide/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
