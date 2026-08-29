# CHIMERA — public pages

The public pages for CHIMERA, a local-first video editing and measurement
tool. Served by GitHub Pages.

| Page | Purpose |
|---|---|
| `index.html` | What CHIMERA is, what it measures, which TikTok permissions it requests |
| `privacy.html` | Privacy policy |
| `terms.html` | Terms of service |
| `connected.html` | OAuth redirect target — shows the returned URL so it can be copied |

This repository is public for one reason: TikTok requires proof of ownership
for any domain registered with an app, and that proof is either a DNS record
or a file served from the domain. Neither is possible on a third-party host.

CHIMERA itself is not here.

## Domain verification

TikTok's signature file goes in the repository root and is served at
`https://<user>.github.io/<repo>/<filename>`. Add it, commit, push, wait for
the Pages build, then verify in the developer portal.

`.nojekyll` is present so Pages serves every file verbatim — without it,
files beginning with an underscore are silently dropped, which is exactly
the kind of file a verification scheme likes to hand you.
