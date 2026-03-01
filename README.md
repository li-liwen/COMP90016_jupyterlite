# COMP90016 JupyterLite

Browser-based Jupyter environment for COMP90016, deployed as a static website with GitHub Pages.

## Scope

- Includes public course data from the companion public repository.
- Includes starter notebooks under `notebooks/` for in-browser workflows.
- Uses the Pyodide-backed Python kernel for stability.

Important: native command-line bioinformatics tools from the old conda/Binder environment (for example `bwa`, `samtools`, `blast`, `prokka`) are not runnable inside JupyterLite.

See [`COMPATIBILITY.md`](COMPATIBILITY.md) for the package/tool support matrix and fallback workflow.

## Local Build

```bash
python3 -m pip install -r requirements.txt
jupyter lite build --contents content/comp90016 --output-dir dist
```

Preview locally:

```bash
python3 -m http.server -d dist 8000
```

Then open: `http://localhost:8000/lab`

## Deployment

Push to `main` to trigger the GitHub Actions workflow in `.github/workflows/deploy.yml`.
The workflow builds the site and deploys it to GitHub Pages.

## Browser Support

- Firefox 90+
- Chromium 89+
