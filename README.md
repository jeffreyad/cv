# Jeffrey A. Dickinson, PhD - Curriculum Vitae

This repository contains my professional CV, built with Quarto.

## View CV

- [HTML Version](https://jeffreyad.github.io/cv/)
- [PDF Version](https://jeffreyad.github.io/cv/cv.pdf)
- [Word Version](https://jeffreyad.github.io/cv/cv.docx)

## About

I'm an Associate Director of Clinical Reporting with 29+ years of experience in pharmaceutical data science, specializing in:

- R package development (pharmaverse ecosystem, admiral, metacore)
- CDISC standards (SDTM, ADaM, ARD)
- Clinical trial data analysis and reporting
- Pharmacokinetics and exposure-response modeling
- SAS programming and biostatistical analysis

## Building Locally

### Prerequisites

- [Quarto](https://quarto.org/docs/get-started/)
- [R](https://www.r-project.org/) (optional, for dynamic content)

### Render the CV

```bash
quarto render cv.qmd
```

This will generate HTML, PDF, and Word versions in the current directory.

## Repository Structure

```
cv/
├── README.md              # This file
├── cv.qmd                 # Main CV source (Quarto)
├── _quarto.yml            # Quarto project configuration
├── assets/                # Supporting files
│   ├── styles.css         # Custom CSS styling
│   └── custom-reference.docx  # Word template (optional)
├── docs/                  # Rendered outputs (GitHub Pages)
├── .github/workflows/     # GitHub Actions for automation
└── archive/               # Previous versions (optional)
```

## GitHub Pages

This CV is automatically published to GitHub Pages using GitHub Actions. Any push to the `main` branch triggers a rebuild.

## Contact

- **GitHub**: [@jeffreyad](https://github.com/jeffreyad)
- **LinkedIn**: [Your Profile](https://linkedin.com/in/jeffreyad)
- **Email**: your.email@example.com

## License

© 2025 Jeffrey A. Dickinson. All rights reserved.
