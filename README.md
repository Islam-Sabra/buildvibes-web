# buildvibes-web

The public link pages for BuildVibes, served by GitHub Pages at https://buildvibes.aecox.com (review 127, "Link domain for the pilot").

- `/.well-known/assetlinks.json`: Android App Links for `com.buildvibes.buildvibes`. It holds the upload key's SHA-256, used by the builds installed in the pilot. The Play app signing SHA-256 is added when the app is in Play Console.
- `404.html` (and `index.html`, the same page): `/p/<id>` and `/c/<id>` show "Open in BuildVibes" (Android, opens the app when installed) and "Ask your site lead for the BuildVibes app" / «اطلب تطبيق BuildVibes من مسؤول الموقع», in Arabic or English. Nothing is fetched; no profile data is on this site.
- **The day the app goes onto Google Play,** do both together: put the store link back on the page, and add the Play app signing SHA-256 (Play Console → App integrity) to `assetlinks.json` next to the upload key.
- `CNAME`: buildvibes.aecox.com. `.nojekyll`: so `.well-known` is served.

No secrets live here. The app's code is in a separate, private repo.
