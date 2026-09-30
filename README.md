# zelavis/marketplace

What the Zelavis marketplace lets an installation install: the signed allow-list,
hosted as a plain file so it can be fetched from GitHub raw as one of several
mirrors.

- `allowlist.json` is the envelope `pnpm allowlist sign` writes in the main
  repository. It is trustworthy only because of its signature (Ed25519, verified
  by every installation against the key built into Zelavis); this repository is a
  place to host it, not a source of trust. Nothing here is edited by hand.
- To publish: in `zelavis`, run `pnpm allowlist update`, then
  `pnpm allowlist sign --out marketplace/allowlist.json`, and commit and push here.
- The signing private key never goes in this repository.
