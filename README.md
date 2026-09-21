# V5 OTA images

Public home of the signed v5 OTA images (nRF9151, STM32U575, ESP32-C3), which
devices download over plain HTTPS for over-the-air updates.

One branch per firmware release class:

| branch | release class | for |
|---|---|---|
| `prod` (default) | `fw-bundle_prod-<YYYYMMDD>.<n>` | the field |
| `ltt` | `fw-bundle_ltt-<YYYYMMDD>.<n>` | long-term testing units |
| `lab` | `fw-bundle_lab-<YYYYMMDD>.<n>` | the provisioning bench |

On each branch, a `<bundle-tag>/` directory holds the three `.s.bin` images of
one firmware bundle and a `manifest.json`, and `latest.json` points at the
newest bundle of that branch:

    https://raw.githubusercontent.com/floodnet-nyc/v5-ota-images/<branch>/<bundle-tag>/<asset>

This branch was called `main` before release classes existed; the unclassed
`fw-bundle-<YYYYMMDD>.<n>/` directories here are production bundles from then.

Published by `scripts/release/firmware_bundle.sh` in floodsensor-v5.
