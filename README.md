# myMDB update channel

Repository pubblico usato dall'updater Android di myMDB.

File di produzione previsti:

- `latest.json` — manifest letto dall'app;
- `myMDB-release.apk` — APK firmata con la stessa chiave dell'installazione da aggiornare.

Il manifest non va pubblicato prima dell'APK corrispondente. La CI di `stefanodiconcetto-ux/myMDB` genera il bundle e verifica package, versionCode, versionName e SHA-256 prima della pubblicazione.

Formato di `latest.json`:

```json
{
  "versionCode": 17,
  "versionName": "0.3.1",
  "apkUrl": "https://raw.githubusercontent.com/stefanodiconcetto-ux/myMDB-updates/main/myMDB-release.apk",
  "sha256": "<64 caratteri esadecimali>"
}
```

Non committare keystore, password, token o altre credenziali in questo repository.
