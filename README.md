# pdfino

Convert `.ino` and `.py` files in the current directory into PDFs via Markdown + Pandoc.

## Install (global)

```sh
uv tool install pdfino
```

## Use

```sh
cd /path/to/project
pdfino
```

One PDF is created per input file:

- `listing_demo.ino` -> `listing_demo.ino.pdf`
- `script.py` -> `script.py.pdf`

## Options

```sh
pdfino --help
```

## Examples:

```sh
pdfino -e .ino
pdfino -e py -o out_pdfs
pdfino --keep-md
pdfino --pdf-engine xelatex
```

---

## Step 5: Try it locally (developer loop)

From the project root:

```bash
uv venv
uv pip install -e .
pdfino --help
```

Then, in any folder with .ino or .py files:

```sh
cd /somewhere/with/files
pdfino
```

## Uninstall

If `pdfino` was installed as a global uv tool:

```sh
uv tool uninstall pdfino
```

If you installed it from a local checkout and want to reinstall after changes:

```sh
uv tool uninstall pdfino
uv tool install .
```

This removes the isolated tool environment and the pdfino command from your PATH.