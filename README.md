# Brihat Kirti sign-in return page

`oauth/callback.html` is Brihat Kirti's https bounce page. After you click Allow on a platform's sign-in page (Meta), the platform returns here, and the page forwards the sign-in to Kirti on your own computer (`127.0.0.1`). If that doesn't work, it shows the address to paste into Kirti instead.

- It is a byte-for-byte copy of `packages/publishers/templates/oauth-callback.html` in the Brihat Kirti repo. Don't edit it here; copy it again from there.
- It loads nothing from anywhere else, sends no referrer, and has a strict CSP pinned to its own inline script.
- A sign-in code that passes through here works only once, expires within minutes, and is useless without the app secret held in Kirti's keychain.
