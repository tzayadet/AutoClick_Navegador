<p align="center">
  <img src="https://img.shields.io/badge/BROWSER_AUTOMATION-AUTO_LOAD_MORE-101010?style=for-the-badge&labelColor=050805&color=00FF41" alt="Auto Load More"/>
  <img src="https://img.shields.io/badge/JAVASCRIPT-BOOKMARKLET_STYLE-101010?style=for-the-badge&logo=javascript&logoColor=00FF41" alt="JavaScript"/>
</p>

# Auto Load More

Small JavaScript utility that automates a visible **Load more** button on a web page. It checks the page, triggers the button and waits for content to load before continuing.

<p align="center">
  <a href="https://github.com/tzayadet/AutoClick_Navegador"><strong>SOURCE CODE</strong></a>
</p>

## How it works

- Finds visible elements whose text matches the configured button label.
- Checks that the element is visible before interacting.
- Simulates the mouse event sequence: `mousedown`, `mouseup` and `click`.
- Waits between attempts.
- Stops when the target button disappears or the configured stop condition is reached.
- Reports click count and elapsed time.

The repository also contains an improved iteration that checks for page changes, records timestamps and per-load duration, and stops when no new content is detected.

## Use it

1. Open the page you want to inspect.
2. Open the browser developer tools.
3. Select the Console tab.
4. Paste the contents of `auto-load-more.js`.
5. Press Enter and monitor the console output.

Use the script only on pages where automated interaction is permitted.

## Configuration

Adjust the values in the script:

```javascript
const DELAY = 2500;
const BUTTON_TEXT = 'Cargar más';
```

For example, use `BUTTON_TEXT = 'Load more'` for an English interface or increase the delay to give slower pages time to update.

## Project layout

```text
.
├── auto-load-more.js
└── README.md
```

## Limitations

This is a small page-interaction helper, not a universal crawler. It may not work with Shadow DOM, iframes, unusual button structures, infinite scroll, anti-bot controls or pages that require framework-specific events.

## Technology

- JavaScript
- DOM APIs
- Browser mouse events
- Developer Tools Console

## Scope

The script automates repetitive interaction with a page already open in the user's browser. It does not bypass authentication, access controls or anti-bot protections.

## License

See [LICENSE](LICENSE) for the repository's licensing terms.
