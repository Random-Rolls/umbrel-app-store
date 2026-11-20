# Umbrel App Store

A small Umbrel community app store. Add it in umbrelOS under **App Store → Community App Stores** and paste this repository's URL.

## Apps

| App | ID | Notes |
| --- | --- | --- |
| Ente Photos | `epsilon-ente-photos` | Self-hosted Ente server and web client. |
| openGym | `epsilon-opengym` | openGym 1.4.6, API and web images pinned by digest. |
| Materialious | `epsilon-materialious` | Materialious 1.18.35, pointed at a self-hosted Invidious instance. |
| Redlib | `epsilon-redlib` | Nachtalb fork v0.69.0, private ad-free Reddit front-end. |
| SpiderFoot | `epsilon-spiderfoot` | SpiderFoot 4.0 OSINT scanner, container pinned by digest. |

## How updates work

Umbrel only looks at the `version` field in each app's `umbrel-app.yml`. When that changes, the app shows **Update available** and re-pulls the images on update.

- Ente Photos follows the floating `:latest` tags, so a version bump pulls whatever upstream built most recently.
- openGym is pinned by digest, so a bump is explicit: change the version and the two image digests together.
- Materialious is pinned to a release number.

## Notes

- openGym keeps its data in the app's `data` and `coach-auth` folders.
- Materialious keeps accounts and watch state in its own `data` folder.
