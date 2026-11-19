# Lumen

A simple, fast, local-first API client for Windows, by **Inficia**.

No account, no login, no telemetry, no cloud. Collections are plain YAML files in an ordinary folder, so you can keep them in git.

## What you can do

- **Send requests** with any method, query and path parameters, headers and the bodies you expect: JSON, text, XML, form fields, multipart (with files), binary files and GraphQL. See the status, time, size, headers, cookies, a formatted body and a timing breakdown.
- **Keep work in folders.** A collection is a folder of small YAML files, one per request, that you can read, review and merge like code. Changes made outside the app (a `git pull`, an editor) show up in the app.
- **Use variables.** `{{name}}` works in the address, headers, bodies and authentication, with layers: request, folder, environment, collection, global and the values scripts store. Unresolved names are highlighted, and a hover shows where a value comes from.
- **Keep secrets out of files.** A variable marked secret has no value in the YAML file. Its value is stored encrypted for your own account (Electron `safeStorage`: Windows DPAPI, or on Linux a keyring such as GNOME Keyring or KWallet, and never a built-in key) and is never written to a collection, an export, the history, a log or the screen.
- **Sign in:** Basic, Bearer, API key, Digest and OAuth 2.0 (authorization code with PKCE in your browser, client credentials, refresh token), with tokens kept encrypted and refreshed for you.
- **Script and test** with JavaScript before and after a request, plus no-code assertions. Scripts run in an isolated sandbox with a time and memory limit and see only the documented API ([scripting reference](docs/scripting-api.md)).
- **Run a folder or a whole collection**, in order, with an environment, several iterations, a CSV or JSON data file, "stop on the first failure" and a delay. Watch the results arrive and export a JSON, JUnit, HTML or text report. The same runner is a command line program, `lumen` (below).
- **Import** a Lumen collection file (see Export), a cURL command (paste it into the address field, or press Ctrl+Shift+I), a Postman collection (v2.0 and v2.1) and environment, or an OpenAPI 3 or Swagger 2 file. You see what will be created, and what could not be converted, before anything is written.
- **Export** a collection, a folder or one request as a **Lumen collection** file (the first choice: it moves a collection to Lumen on another computer with nothing lost, and leaves secret values behind to be entered again), as Postman (v2.1 or v2.0), OpenAPI 3.0 (JSON or YAML) or a script of cURL commands for Bash, Windows cmd or PowerShell. Nothing secret goes out, and each export says what its format could not hold.
- **Copy as code:** cURL, JavaScript (fetch), Python (requests), Go, C# (HttpClient) and PowerShell (Invoke-RestMethod). Secrets stay as placeholders unless you confirm in a dialog.
- **History** of what you sent, kept on your machine with secrets removed and no response bodies by default. Search it, re-open an entry, clear it, or switch it off.
- **Network settings:** system, manual or no proxy (with authentication and a no-proxy list), your own certificate authorities, client certificates (PFX and PEM), a cookie jar you can inspect and clear, size limits, and TLS verification (on by default; switching it off shows a warning and a badge).
- Light and dark themes (system by default), a text size setting, keyboard shortcuts and a cheat sheet (Ctrl+/).