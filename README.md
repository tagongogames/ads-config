# Tagongo Games — ad-frequency config

Public, static, signed configuration read by Tagongo Games apps to tune how often optional-placement
interstitial ads may appear. It contains **no secrets** and no user data.

- `v1/config.json` — current signed envelope `{fmt, kid, payload(base64 JSON), sig(RSA-2048 PKCS#1 v1.5 SHA-256)}`.
- `v1/historial/NNNNNN.json` — every published version (the git history is the audit log).

Apps verify the signature with embedded public keys, ignore anything invalid, keep the last valid copy,
and always fall back to safe built-in defaults. Hard limits (never during gameplay, never on app open,
no ads after any purchase, minimum spacing) are enforced in the apps and cannot be changed from here.
