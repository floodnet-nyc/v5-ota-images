# Campaign v2: bench images (virtual-eFuse ESP32)

**Bench only. Never start this campaign on a field unit.**

Same campaign as branch `migration`, folder `migration-v2/`, except that
the ESP32 bootloader burns nothing:

| File | Differs from `migration` | Why |
| --- | --- | --- |
| `v5_esp32c3_sbl.bin` | yes | ESP32 v0.2.0-rc.7 prod, `-DFN_EFUSE_VIRTUAL=ON`: eFuses kept in flash at 0x3B0000 (8 KB) |
| `v5_esp32c3_v0.2.0-rc.7.s.bin` | yes | same build; the app confirms itself under the virtual-eFuse bootloader |
| `v5_stm32u575_v0.1.99-migration-v2.bin` | yes | same source (d90b561f), this branch's `manifest.txt` baked in |
| `v5_nrf9151_v0.1.99-transition.bin` | yes | nRF d2e2833 + `app/overlay-migration-testing.conf` (URL and sha256 of the image above) |
| everything else | no | identical to `migration` |

Start the campaign with:

```
CMD_CELL_APP_OTA:https://raw.githubusercontent.com/floodnet-nyc/v5-ota-images/migration-testing/migration-v2/v5_nrf9151_v0.1.99-transition.bin
```

Before the run, erase the virtual-eFuse area on the ESP32
(`esptool erase-region 0x3B0000 0x2000`): the bootloader loads anything
there that is not all 0xFF as its eFuses.
