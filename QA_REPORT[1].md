# SOC-245 Coursebook Quality Check

**Audit date:** October 6, 2026  
**Scope:** Complete *Beyond the Substance* static coursebook

## Repairs completed

- **Section 6:** Repaired the recruitment/socialization sequence and Faupel
  lifestyle activity. Literal line breaks inside JavaScript strings had stopped
  both activities from initializing.
- **Section 12:** Repaired the four-case causal-pathway activity. The same
  JavaScript string problem had disabled every case and answer button.
- **Section 12 accessibility:** Added a proper tab panel relationship, selected
  states, roving keyboard focus, arrow-key navigation, Home/End navigation, and
  safe feedback rendering.
- **GitHub landing behavior:** The repository root now opens the visual title
  and chapter landing page. Section 1 remains available as
  `topics/what-is-a-drug.html`.
- **Portable citations:** Coursebook self-citation links now adapt to the host
  address, allowing the same files to work under a GitHub Pages project path.
- **GitHub Pages compatibility:** Added `.nojekyll` and removed dependence on
  ChatGPT Sites routing.

## Automated checks passed

- 27 HTML pages parsed and inspected
- All inline and external JavaScript files pass syntax validation
- All referenced local pages, scripts, stylesheets, and images exist
- All internal fragment links point to existing IDs
- No duplicate IDs detected
- All images include alternative-text attributes
- Every page includes language, viewport, and main-heading metadata
- Git whitespace and patch checks passed

## Live-site comparison

The previously published version was opened page by page in a browser. Runtime
syntax errors appeared only in Section 6 and Section 12, matching the two
failures found by the source audit. Both are repaired in this GitHub-ready
package.

## Recheck after future edits

Run:

```bash
node tools/audit-site.mjs .
```

This audit does not replace human review of wording, external source currency,
or every possible browser and assistive-technology combination. It is designed
to catch the structural failures most likely to make a static coursebook page
or activity stop working.
