# zelavis/allowlist

The signed marketplace allow-list, hosted as a plain file so it can be fetched
from GitHub raw as one of the mirrors.

- `allowlist.json` is the envelope `pnpm allowlist sign` writes in the main
  repository. It is only trustworthy because of its signature: this repository
  is a place to host it, not a source of trust. Nothing here is edited by hand.
- To publish: in `zelavis`, run `pnpm allowlist update` then
  `pnpm allowlist sign --out allowlist/allowlist.json`, and commit and push here.
- The signing private key never goes in this repository.
