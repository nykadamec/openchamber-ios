# OpenChamber iOS

Veřejný zdroj pro sideload OpenChamber na iOS (unsigned IPA + KSign AltStore source).

- Aplikace: OpenChamber 1.1 (build 4), bundle `com.openchamber.app`, velikost 17051372 bajtů
- IPA (unsigned, vyžaduje re-sign v KSign/Feather vlastním certifikátem): https://github.com/nykadamec/openchamber-ios/releases/download/v1.1-build4/OpenChamber.ipa
- KSign source: https://raw.githubusercontent.com/nykadamec/openchamber-ios/main/repo.json

## Přidání do KSign

V KSign `Sources → Add Source` vlož:

```
https://raw.githubusercontent.com/nykadamec/openchamber-ios/main/repo.json
```

## Soubory

- `repo.json` – finální AltStore Classic Source (tento soubor přidat do KSign)
- `ksign-source.json` – pracovní šablona zdroje (placeholder `USER/REPO`)
- `KSIGN-HOSTING.md` – postup hostingu a TODO

## Poznámka

IPA je **unsigned** – před instalací vyžaduje re-sign na zařízení (KSign/Feather + vlastní certifikát).
