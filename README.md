# SimpleKit Starter Template

This repository is the clean starter template for future SimpleKit tool repos.

It preserves the proven static SimpleKit architecture from the original working tool repo:

- shared core shell loaded from `https://core.simplekit.app`
- existing Google Analytics head snippet kept in place
- no build step required for the default starter

The previous tool-specific logic, copy, charts, test harness, and styling have been removed so a future tool can start from a clean base instead of a single-purpose implementation.

## Starter File Structure

```text
/
  index.html
  assets/
    css/
      styles.css
    js/
      app.js
  README.md
```

## Edit These Files First

For a new tool, start here:

1. `index.html`
2. `assets/js/app.js`
3. `assets/css/styles.css`

### `index.html`

Update:

- page title
- meta description
- canonical URL
- Open Graph tags
- Twitter tags
- JSON-LD
- hero copy
- section headings

Do not remove:

- the Google Analytics snippet in the `<head>`
- the `preconnect` and shared core stylesheet/script references
- shared shell mount points such as `data-simplekit-header`, `data-simplekit-support`, and `data-simplekit-footer`

### `assets/js/app.js`

This file contains the placeholder starter behavior:

- starter form defaults
- URL state syncing
- sample/reset actions
- simple preview/result rendering
- share-link helper

Replace the placeholder sections labeled through the UI and code with your tool-specific logic.

### `assets/css/styles.css`

This file contains the local visual layer for the starter template only.

Keep platform-level shell styling in the shared core deployment. Use this file for:

- tool-specific layout
- section styling
- local form/result presentation

## Shared Core Connection

This starter continues the same working pattern used by the original repo:

- `index.html` sets `window.SimpleKitPage` before loading the core script
- the page loads `https://core.simplekit.app/core.css`
- the page loads `https://core.simplekit.app/core.js`
- the shared core mounts the standard SimpleKit shell into the page

At a high level, this means the copied repo owns the tool content while the shared core owns the common platform shell.

## Google Analytics

The Google Analytics head code lives in:

- `index.html`

Keep it exactly as-is unless the overall SimpleKit tracking setup changes centrally.

## Deployment Notes

This is a static repo. A copied tool repo can be deployed directly as a static site, including GitHub Pages.

Basic flow:

1. Copy this starter into a new repo.
2. Replace all placeholder metadata and content.
3. Add the new tool-specific logic and any required assets.
4. Deploy the copied repo as a static site.
5. Verify the deployed page can still reach:
   - `https://core.simplekit.app/core.css`
   - `https://core.simplekit.app/core.js`
6. Verify the shared header, footer, and support section render correctly.

## New Tool Checklist

- Replace `SimpleKit Tool Title` everywhere it appears.
- Replace `Tool description goes here` everywhere it appears.
- Update canonical and social URLs before deploy.
- Replace the starter JSON-LD with tool-specific schema.
- Replace placeholder form fields and starter output cards.
- Remove or adapt the starter share action if the finished tool does not need it.
- Confirm no placeholder copy remains in UI, metadata, comments, or README.
- Confirm the shared core shell still loads after deployment.
- Confirm the Google Analytics snippet is still present in the page head.
