# EZRobot Zyra v1 technical report

English first draft of the first-generation Zyra technical report. Open `main.tex` in Overleaf and select pdfLaTeX. Section sources are under `sections/`; references are in `references.bib`.

Local build:

```bash
latexmk -pdf -interaction=nonstopmode -halt-on-error -outdir=build main.tex
```

The draft uses recorded open-agent v9 results from the supplied SPAR snapshot. It separately identifies the earlier pick-and-place agent and its real-robot deployment. Pending measurements are described explicitly rather than filled with estimated results.

See `EDITOR_NOTES.md` for evidence provenance and the remaining author inputs.
