# V2raySwift — releases

Public distribution point for **V2raySwift**. The source lives in a private repository; this
artifacts-only repo exists because [Sparkle](https://sparkle-project.org) fetches its update
feed unauthenticated, and a private repo answers those fetches with 404.

Each release tagged `v<version>` carries:

- `V2raySwift-<version>.zip` — the app, Developer ID signed and notarized;
- `appcast.xml` — the Sparkle feed, EdDSA-signed over the zip.

The feed URL the app has baked in is
`https://github.com/bukede/v2raySwift-releases/releases/latest/download/appcast.xml`.

## Verifying a download

Download the newest zip from [releases](../../releases), unzip it, and — if you want to know
what Gatekeeper will say before opening — check:

```console
$ spctl -a -vv --type execute V2raySwift.app
V2raySwift.app: accepted
source=Notarized Developer ID
```
