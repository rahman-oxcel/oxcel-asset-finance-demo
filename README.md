# Oxcel Asset Finance — protected preview

A password-protected live preview of the Oxcel Asset Finance loan-writing platform prototype.

- **Live link:** served via GitHub Pages (see the repository's Pages settings).
- **Access:** the page is a single, self-contained build of the prototype, encrypted with a password. Enter the password on the unlock screen to view it.

## How the protection works

The entire application (HTML, CSS, JavaScript and assets) is bundled into one file and encrypted with AES-256-GCM. The key is derived from the password using PBKDF2 (SHA-256, 250,000 iterations). Nothing is readable, and the app cannot run, until the correct password is entered — the decryption happens in the browser. There is no server and no database; the prototype keeps its demo state in the browser's local storage only.

To rotate the password or rebuild, regenerate `index.html` from the source project and push.

_Confidential prototype. Not for public distribution._
