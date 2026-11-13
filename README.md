# AKLİSANS PRO public license catalog repository template

This repository publishes the current AKLİSANS PRO signed license catalog. It is public-read so customer computers can download the catalog anonymously. Only the AKLİSANS PRO management computer publishes updates, through the GitHub CLI session for the `MeansOfMany` owner.

## Files to publish from the AKLİSANS PRO management computer

- `licenses.json` — the latest RSA-PSS signed catalog prepared by the management app.
- `licenses.json.public.pem` — the matching public verification key, distributed to customer builds and optionally mirrored here.

The customer client downloads only `licenses.json` over normal certificate-validated HTTPS. It does not need a GitHub account, token, or write access. The matching PEM is for controlled distribution and pinning in client trust configuration; clients must never trust an arbitrary key fetched from the same location as the catalog.

Keep repository write credentials on the AKLİSANS PRO management computer in GitHub CLI's credential store. The management publisher verifies the owner and public visibility, rejects every root entry outside its explicit allowlist, creates a signed monotonically increasing catalog, writes only the four allowlisted files, and reads back the catalog to verify signature and revision. Never add activation codes, customer names/contact details, Access databases/backups, TLS private keys, or any RSA private key. The `.gitignore` is additional protection and is not the publication allowlist.

Catalog entries contain only full activation-code hashes, product codes, dates, status, terminal limits, revision, UTC publication time, and RSA-PSS signature. An unsuccessful publication remains pending locally with a bounded retry delay and visible management-app status; a successful central database operation is never presented as a successful GitHub publication unless the read-back check passes.
