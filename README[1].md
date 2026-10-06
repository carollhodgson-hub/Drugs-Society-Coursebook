# Beyond the Substance: Understanding Drugs in Culture & Society

An accessible, interactive coursebook for SOC-245 Drugs and Society.

**Author:** Caroll B. Hodgson  
**Institution:** Rowan-Cabarrus Community College

## GitHub Pages

This folder is ready to publish from the repository root.

1. Upload all files and folders from this package to a GitHub repository.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose the **main** branch and **/(root)** folder, then select **Save**.
5. GitHub will display the public address after deployment finishes.

The root `index.html` opens the visual book landing page. Section 1 is stored at
`topics/what-is-a-drug.html`. The `.nojekyll` file tells GitHub Pages to serve
the static files without Jekyll processing.

## Accessibility and testing

The package includes semantic headings, image alternative text, keyboard-aware
controls, responsive layouts, and equivalent explanatory text for interactive
material. Run the included source audit before future uploads:

```bash
node tools/audit-site.mjs dist
```

The audit checks JavaScript syntax, local files, internal anchors, duplicate
IDs, image alternative text, language metadata, viewport metadata, and page
headings.
