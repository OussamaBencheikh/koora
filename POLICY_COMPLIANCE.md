# Chrome Web Store policy checklist

This project is designed around the [Chrome Web Store Program Policies](https://developer.chrome.com/docs/webstore/program-policies). Policy compliance is a release requirement, but Google makes the final review decision.

## Current product scope

- Single purpose: a playable Snake arcade game in the extension popup.
- No browsing-page access, content scripts, background service worker, accounts, ads, analytics, affiliate links, or payments.
- No Chrome permissions are requested.
- All JavaScript and CSS needed by the extension are packaged locally. No remote scripts, remote code, `eval`, or dynamic code execution are used.
- The only stored user value is the local best score. It is not transmitted or shared.

## Release checks

Before every Chrome Web Store submission:

1. Keep the name, description, screenshots, icon, and privacy fields accurate and consistent with the product.
2. Confirm the extension still has one narrow purpose and provides real working functionality.
3. Search the package for remote scripts, remote code, `eval`, new permissions, trackers, ads, and unexplained data collection.
4. Update [privacy-policy.html](privacy-policy.html) and the Chrome Web Store privacy fields if data behavior changes.
5. Build a fresh ZIP containing only the extension runtime files and test it with **Load unpacked**.
6. Review the current [Program Policies](https://developer.chrome.com/docs/webstore/program-policies) and [Manifest V3 requirements](https://developer.chrome.com/docs/webstore/program-policies/mv3-requirements) before publishing.

## Current data disclosure

The extension uses browser `localStorage` only to retain the player's best score on the same device. It does not collect, sell, share, or transmit user data. The public policy is available at [privacy-policy.html](privacy-policy.html).