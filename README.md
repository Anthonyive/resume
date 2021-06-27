# Résumé

My résumé is created here!

## Download PDF

The résumé will be published in a form of GitHub releases.

- To download PDF: [Click Here](https://github.com/Anthonyive/resume/releases/latest/download/resume.pdf)
- To go to the latest release page: [Click Here](https://github.com/Anthonyive/resume/releases/latest)

## GitHub Actions CI/CD

GitHub Actions are set up for compiling tex file, generating pdf, and pushing to GitHub Releases with calendar versioning. So I will only need to push the `resume.tex` to GitHub, and the build system will compile the pdf for me.

### Release Logic

`.tex` file will be compiled for every push. However, if there's multiple pushs in a day, the last release will replace the others.

### Build Engine & Font

I love the `EB Garamond` font on my resume, so it is the default font. In addition, there are fontawesome icons (also some sort of font) on the resume. Because of these reasons, the build engine for `resume.tex` has to be `LuaLaTeX`.

### Little Caveat About Calendar Versioning

<img src="https://img.shields.io/badge/calver-vYYYY.0M.0D-22bfda.svg" />

It seems like the CI uses UTC time, so the timezone could be a little bit off. Since the default timezone is most likely going to be UTC for Linux systems, I wouldn't bother to change it to my current timezone.
