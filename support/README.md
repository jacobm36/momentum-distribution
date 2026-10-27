# Launcher compatibility support data

This folder publishes signed compatibility support records that allow newer
package evidence to be recognized by compatible launcher versions without
rebuilding game installer ZIPs.

- `compatibility-v1.json` — compatibility records payload.
- `compatibility-v1.json.sig` — OpenSSL SHA-256 signature over the JSON bytes.

The launcher ships the matching public key and verifies signatures before use.
If refresh fails, it reuses the last verified cached payload.
