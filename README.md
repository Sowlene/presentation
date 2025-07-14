# 📄 Automatic LaTeX PDF Build with GitHub Actions - Presentation

This repository automatically compiles a LaTeX document (`bulletpoints.tex`) on every push  
and makes the generated PDF available as a downloadable artifact.

---

## 🧾 Repo Contents

- `bulletpoints.tex`: A minimal LaTeX file with simple bullet points.
- `.github/workflows/latex.yml`: The GitHub Actions workflow that compiles the LaTeX file using Docker and uploads the resulting PDF.

---

## ⚙️ How does it works

On every push to the `main` branch, GitHub Actions:

1. Starts a Docker container with a full TeX Live environment (`blang/latex:ctanfull`).
2. Compiles the `bulletpoints.tex` file using `pdflatex`.
3. Uploads the resulting `bulletpoints.pdf` as a downloadable artifact.

---

## 📥 How to Download the Generated PDF

1. Go to the **Actions** tab in your GitHub repository.
2. Click on the latest workflow run (usually titled “Build LaTeX document”).
3. In the right-hand sidebar, look for the **Artifacts** section.
4. Click on **`bulletpoints-pdf`** to download a `.zip` file containing `bulletpoints.pdf`.

---

## 📌 Notes

- This setup uses Docker to avoid slow installations of TeX Live during every run.
- The PDF is built in a clean and reproducible environment.
- You can edit `bulletpoints.tex`, include packages, or change the compiler (e.g., `xelatex`, `lualatex`).
