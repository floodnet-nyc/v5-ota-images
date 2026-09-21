# V5 OTA images: lab

Signed OTA images of the **lab** release class (provisioning bench).

Each `fw-bundle_lab-<YYYYMMDD>.<n>/` directory holds the three `.s.bin`
images of one firmware bundle and a `manifest.json`; `latest.json` points at
the newest bundle on this branch. Published by
`scripts/release/firmware_bundle.sh --class lab` in floodsensor-v5.

    https://raw.githubusercontent.com/floodnet-nyc/v5-ota-images/lab/<bundle-tag>/<asset>

Branches: `prod` (default, field), `ltt` (long-term testing), `lab` (provisioning bench).
