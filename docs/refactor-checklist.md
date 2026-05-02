# Refactor checklist

Branch: portfolio-mambo-ui

## Current safe state

- Main branch is untouched.
- Audit notes exist in docs/audit.md.
- Current CSS has been copied into assets/css/portfolio.css.
- index.html has not yet been changed, so the public-facing page logic is not affected by this branch.

## Next safe refactor steps

1. Open index.html locally or in GitHub editor.
2. Copy the full inline style block into assets/css/portfolio.css if it changed after this checklist.
3. Replace the inline style block with:

```html
<link rel="stylesheet" href="assets/css/portfolio.css">
```

4. Verify that the visual layout is unchanged.
5. Only after that, extract the full inline script into:

```text
assets/js/portfolio-status.js
```

6. Replace the inline script block with:

```html
<script src="assets/js/portfolio-status.js" defer></script>
```

7. Verify section toggles, status badges, progress bars, and the Bevezetes subtask rendering.

## Checks before MAMBO visual adaptation

- All section toggles open and close correctly.
- No console errors.
- No broken Google Docs or Google Sheets links except intentional placeholders.
- Placeholder href="#" links are either replaced or visually marked as pending.
- Narrow mobile view does not overflow because of long Hungarian titles.
- External GIF dependency is either accepted or replaced by a local asset.

## Stop condition

Do not start the visual MAMBO adaptation if the extracted CSS or JS causes any functional difference.