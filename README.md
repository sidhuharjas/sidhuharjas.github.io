# sidhuharjas.github.io

## Direct Linking on GitHub Pages

To enable direct linking to paths like `/combat/overview` on GitHub Pages without `404` errors, this site uses a custom `404.html` redirect script.

- `404.html` captures unknown routes and redirects to the root `index.html` with the original path preserved in a query parameter.
- `index.html` then restores the requested route and rewrites the URL back to a clean path.

This approach keeps clean URLs (without `#`) while still working with static GitHub Pages hosting.

Alternative: hash routing (for example `/#/combat/overview`) is simpler to set up, but it exposes the hash symbol in URLs.

For more details, see GitHub Pages documentation and community SPA routing guides.
