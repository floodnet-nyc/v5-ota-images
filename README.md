# V5 OTA images: user

Signed OTA images of the **user** release class (the sold build).

Each `fw-bundle_user-<YYYYMMDD>.<n>/` directory holds the four `.s.bin`
images of one firmware bundle and a `manifest.json`; `latest.json` points at
the newest bundle on this branch. Published by
`scripts/release/firmware_bundle.sh --class user` in floodsensor-v5.

    https://raw.githubusercontent.com/floodnet-nyc/v5-ota-images/user/<bundle-tag>/<asset>

Branches: `prod` (default, field), `ltt` (long-term testing), `lab` (provisioning bench), `user` (sold build).
