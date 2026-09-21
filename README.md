# V5 OTA images: ltt

Signed OTA images of the **ltt** release class (long-term testing units).

Each `fw-bundle_ltt-<YYYYMMDD>.<n>/` directory holds the three `.s.bin`
images of one firmware bundle and a `manifest.json`; `latest.json` points at
the newest bundle on this branch. Published by
`scripts/release/firmware_bundle.sh --class ltt` in floodsensor-v5.

    https://raw.githubusercontent.com/floodnet-nyc/v5-ota-images/ltt/<bundle-tag>/<asset>

Branches: `prod` (default, field), `ltt` (long-term testing), `lab` (provisioning bench).
