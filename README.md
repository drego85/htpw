# htpw - Htaccess To Protect WordPress

htpw is a curated `.htaccess` ruleset for Apache that hardens a WordPress site without relying on plugins.
The goal is to raise the baseline security posture with low overhead and minimal changes to WordPress itself.

## What this file does

The `htaccess` ruleset focuses on common hardening measures:

- Protects sensitive system files (e.g., `wp-config.php`, logs, backups).
- Disables directory listing.
- Adds modern security headers.
- Blocks known malicious or scanning user agents.
- Prevents PHP execution inside `wp-content/uploads`.
- Restricts `xmlrpc.php` to trusted services (Jetpack and Akismet).

## Why use htpw

WordPress is a frequent target. Security plugins can be effective, but they may add overhead or conflicts.
htpw provides a lightweight alternative using Apache rules that:

- Reduce the attack surface.
- Require no PHP runtime or plugin.
- Are easy to review, audit, and adjust.

## Installation

1. Download the `htaccess` file from this repository.
2. Append its contents to the bottom of your existing WordPress `.htaccess`.
3. Ensure your web server is Apache with `mod_rewrite` and `mod_headers` enabled.

Note: These rules are not designed for NGINX.

## Security headers

The file ships with a modern header set (HSTS, X-Frame-Options, X-Content-Type-Options, etc.).
There is also a **commented** Content-Security-Policy (CSP) block that you can enable when ready.
CSP can be strict and may require allowlisting external domains used by your theme or plugins.

## Compatibility notes

- If you use a CDN (e.g., Cloudflare), consider enabling `mod_remoteip` so visitor IPs are logged correctly.
- Some plugins that rely on XML-RPC may need adjustments if you tighten that block.
- If you enable the optional CSP, expect a short tuning phase.

## Testing

You can validate that htpw is working by running a scanner such as WPScan.
If the default scan is blocked, the rules are active.

## Contributing and support

- Pull requests are welcome. Please keep changes minimal, well scoped, and documented.
- If you find this project useful, you can support it via Buy Me a Coffee:
  https://buymeacoffee.com/andreadraghetti

## License

GNU General Public License v3.0
