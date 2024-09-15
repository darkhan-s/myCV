# myCV
[![Build LaTeX and Deploy PDF to pdf-output](https://github.com/darkhan-s/myCV/actions/workflows/latex-pdf.yml/badge.svg?branch=main)](https://github.com/darkhan-s/myCV/actions/workflows/latex-pdf.yml)

# CV LaTeX Build & Deployment

This repository contains my CVs written in LaTeX, which are automatically built and deployed to a separate branch using GitHub Actions.
# DO NOT PUSH TO THIS BRANCH. It will not do any harm, but also will produce nothing useful.
## Workflow

The GitHub Actions workflow is triggered every time changes are pushed to any branch except `pdf-output`. The workflow performs the following steps:

1. **Install LaTeX**: Uses a Docker container with LaTeX pre-installed to compile the `.tex` file specific to the branch.
2. **Compile LaTeX**: Dynamically selects the `.tex` file based on the branch name and compiles it into a PDF using `xelatex`.
3. **Deploy to `pdf-output` Branch**: After the build, the compiled PDF is automatically pushed to the `pdf-output` branch, ensuring all branches contribute their PDF without triggering another workflow.

## Output

The final PDF is located in the root of the `pdf-output` branch. You can access the latest version of the CVs by checking the `pdf-output` branch.

## How It Works

1. Push changes to any branch (other than `pdf-output`).
2. GitHub Actions will automatically build the PDF corresponding to the LaTeX file in that branch.
3. The compiled PDF will be pushed to the `pdf-output` branch with a file name corresponding to the branch name.
4. The latest PDF for any branch can be accessed from the `pdf-output` branch.

## Branches

- **`main`**: Contains the primary LaTeX source files for the CV.
- **Other branches**: Each branch can have its own LaTeX file, and the corresponding PDF will be generated and pushed to the `pdf-output` branch.
- **`pdf-output`**: Contains the compiled PDF files from all branches.

## Access the Latest PDFs

To view or download the latest version of any compiled CV, go to the `pdf-output` branch or use the following link:
- [Darkhan Saidnassimov's CV (main branch)](https://darkhan-s.github.io/myCV/main.pdf)
- Replace `main` in the URL to access PDFs from other branches, e.g., `https://darkhan-s.github.io/myCV/<branch-name>.pdf`

## Notes

- In Visual Studio Code or Overleaf, use the build recipe: `latexmk` with `xelatex`.
- Each branch should have a corresponding `.tex` file named after the branch.
