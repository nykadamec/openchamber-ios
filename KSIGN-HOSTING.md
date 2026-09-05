# KSign hosting – OpenChamber IPA

Zdroj pro KSign/Feather/ESign: `ksign-source.json` (AltStore Classic Source formát).
Aktuální verze: OpenChamber 1.1 (build 4), `com.openchamber.app`, size 17051372 bajtů.

## Postup (3 kroky)

1. **Upload IPA na GitHub release** – vytvoř release `v1.1-build4` a přilož
   `packages/mobile/OpenChamber.ipa` jako `OpenChamber.ipa`.
2. **Uprav `ksign-source.json`** – doplň reálné `USER/REPO` v `downloadURL`
   (`https://github.com/USER/REPO/releases/download/v1.1-build4/OpenChamber.ipa`),
   `iconURL`, `website`; zkontroluj `size` (`stat -f%z packages/mobile/OpenChamber.ipa`).
3. **Přidej zdroj do KSign** – v KSign `Sources → Add Source` vlož https URL
   na tento JSON (např. `https://raw.githubusercontent.com/USER/REPO/main/ksign-source.json`).

## TODO pro uživatele

- Doplnit reálné `USER/REPO` (placeholder v `iconURL`, `website`, `downloadURL`).
- Nahrát `icon.png` na `https://raw.githubusercontent.com/USER/REPO/main/icon.png`.
- Ověřit `curl -I <downloadURL>` (https, funkční HEAD, stabilní URL).
- Import test v KSign provede uživatel manuálně.
