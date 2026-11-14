# documenso-signall

Documenso v2.21.1 + one patch: after the first signature, all other SIGNATURE fields
of the same signer fill automatically (each via the normal sign call, so audit log is intact).
Licence: AGPL-3.0 (same as Documenso); patch and recipe are public for that reason.

## Rebuild
Edit `DOCUMENSO_VERSION` / `TAG` in `.github/workflows/build.yml`, then Actions > build-signall > Run workflow.
Build stops if the patch no longer fits; adjust `sign-all.patch`.

## Roll back (VPS)
```
cd ~/documenso-deploy && cp compose.yml.bak-20261114 compose.yml && docker compose up -d documenso-app
```
