# myCV
[![Build LaTeX and Deploy PDF to pdf-output](https://github.com/darkhan-s/myCV/actions/workflows/latex-pdf.yml/badge.svg?branch=main)](https://github.com/darkhan-s/myCV/actions/workflows/latex-pdf.yml)

# CV LaTeX Build & Deployment

This repository contains my CV written in LaTeX, which is automatically built and deployed to a separate branch using GitHub Actions.

## Workflow

The GitHub Actions workflow is triggered every time changes are pushed to the `main` branch. The workflow performs the following steps:

1. **Install LaTeX**: Installs the required LaTeX packages to compile the `.tex` file.
2. **Compile LaTeX**: Compiles the LaTeX file (`.tex`) into a PDF using `xelatex`.
3. **Copy to `pdf-output` Branch**: After the build, all files from the `main` branch, including the compiled PDF, are copied to the `pdf-output` branch.

## Output

The final PDF, `SaidnassimovDarkhanCV.pdf`, is located in the root of the `pdf-output` branch. You can access the latest version of the CV by checking the `pdf-output` branch.

## How It Works

1. Push changes to the `main` branch.
2. GitHub Actions will automatically build the PDF from the LaTeX source.
3. All files, including the PDF, will be copied to the `pdf-output` branch.
4. The latest PDF can be accessed from the `pdf-output` branch.

## Branches

- **`main`**: Contains the LaTeX source files and any other relevant files for the CV.
- **`pdf-output`**: Contains all the files from `main` and the compiled PDF (`SaidnassimovDarkhanCV.pdf`).

## Access the Latest PDF

To view or download the latest version of the compiled CV, go to the `pdf-output` branch or use the following link:
https://darkhan-s.github.io/myCV/SaidnassimovDarkhanCV.pdf


## Notes

In Visual Studio code and in Overleaf, build using Recipe:latexmk (xelatex).

