# LaTeX Resume Setup with Altacv

This README provides instructions to set up LaTeX with the `altacv` class and the necessary packages to compile a resume on Windows, macOS, and Linux (Fedora and Ubuntu).

## Prerequisites

Ensure you have the following installed on your system:

- A working TeX distribution:
  - **Windows**: MiKTeX
  - **macOS**: MacTeX
  - **Linux**: TeX Live

### Step 1: Install LaTeX Distribution

#### Windows

1. Download and install MiKTeX from [MiKTeX Download](https://miktex.org/download).
2. Follow the installation instructions and ensure that the "Install missing packages on-the-fly" option is enabled.
3. Install the required packages:
   - Open MiKTeX Console, go to "Packages", and install:
     - `fontspec`
     - `geometry`
     - `graphicx`
     - `hyperref`
     - `xcolor`
     - `titlesec`
     - `fontawesome5`
     - `xifthen`
     - `pgf`
     - `paracol`
     - `ragged2e`
     - `enumitem`
     - `tcolorbox`
     - `academicons`

#### macOS

1. Download and install MacTeX from [MacTeX Download](https://tug.org/mactex/).
2. Follow the installation instructions.
3. Open Terminal and install the required packages with:
   ```bash
   sudo tlmgr install fontspec geometry graphicx hyperref xcolor titlesec fontawesome5 xifthen pgf paracol ragged2e enumitem tcolorbox academicons
   ```

#### Ubuntu

```bash
sudo apt update
sudo apt install texlive-latex-extra texlive-fonts-recommended texlive-fonts-extra lualatex \
texlive-fontspec texlive-geometry texlive-graphicx texlive-hyperref texlive-xcolor \
texlive-titlesec texlive-fontawesome5 texlive-xifthen texlive-pgf texlive-paracol \
texlive-ragged2e texlive-enumitem texlive-tcolorbox texlive-academicons
```

#### Fedora

```bash
sudo dnf install texlive-scheme-full texlive-latex-extra texlive-fonts-recommended texlive-fonts-extra \
texlive-fontspec texlive-geometry texlive-graphicx texlive-hyperref texlive-xcolor \
texlive-titlesec texlive-fontawesome5 texlive-xifthen texlive-pgf texlive-paracol \
texlive-ragged2e texlive-enumitem texlive-tcolorbox texlive-academicons
```

### Step 2: Compile Your Resume

1. **Navigate to your LaTeX directory** where your `resume.tex` file is located:
   ```bash
   cd <your-latex-directory>
   ```

2. **Compile the resume** using `lualatex`:
   ```bash
   lualatex resume.tex
   ```

3. You may need to run the compile command multiple times to resolve cross-references.

### Troubleshooting

- If you encounter missing package errors during compilation, ensure that the required packages are installed.
- Refer to the documentation of your LaTeX distribution for help on package installations and troubleshooting.

## Conclusion

You should now be able to set up LaTeX with the `altacv` class and compile your resume. For further customization and options, refer to the [altacv documentation](./altacv.cls.md).
    