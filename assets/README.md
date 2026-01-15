# Custom Word Template

This directory should contain a `custom-reference.docx` file if you want to customize the Word output styling.

## Creating a Custom Template

1. Generate a default reference document:
   ```bash
   quarto pandoc -o custom-reference.docx --print-default-data-file reference.docx
   ```

2. Open `custom-reference.docx` in Microsoft Word

3. Modify the styles (Heading 1, Heading 2, Normal, etc.) to your preferences

4. Save the file as `assets/custom-reference.docx`

5. The `cv.qmd` file is already configured to use this template

## Default Behavior

If `custom-reference.docx` doesn't exist, Quarto will use its default Word styling.
