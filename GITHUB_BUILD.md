# GitHub se .aab banaye (bina PC ke)

Phone se hi ho sakta hai. Steps:

## 1. GitHub account
- Phone pe https://github.com open karo
- Account banao / login karo

## 2. Naya repository
1. **+ → New repository**
2. Name: `SkyMeter`
3. Public select karo
4. **Create repository**

## 3. Files upload (phone se)
### Asaan tareeqa — GitHub website:
1. Repo page pe **uploading an existing file** / **Add file → Upload files**
2. `SkyMeterAndroid` folder ke **saare files** upload karo  
   (ya pehle zip extract karke andar ki cheezein upload)
3. Commit changes

### Better: zip upload via release / ya computer helper
Agar phone se folder upload mushkil ho:
- `SkyMeterAndroid.zip` extract karke andar ke folders upload karo
- `.github/workflows/build-aab.yml` zaroor hona chahiye

## 4. Build start
1. Repo mein **Actions** tab
2. **Build AAB** workflow select karo
3. **Run workflow** → **Run workflow** button
4. 5–10 minute wait (pehle run lamba ho sakta hai)

## 5. Download .aab
1. Green check aane ke baad workflow click karo
2. Neeche **Artifacts**:
   - `SkyMeter-release-aab` → yeh **Play Store** wali file
   - `SkyMeter-keystore` → **BAHUT ZAROORI** — download karke safe jagah save karo

## 6. Play Console
1. https://play.google.com/console
2. App create → **SkyMeter**
3. Production/Testing release → `.aab` upload

---

## Keystore password (auto-generated mode)
Agar GitHub Secrets set nahi kiye:
- Password: `skymeter123`
- Alias: `skymeter`

**Pehli upload ke baad yahi keystore hamesha chahiye updates ke liye.**  
Isliye `SkyMeter-keystore` artifact zaroor backup karo.

## (Optional) Apna strong keystore
Baad mein PC / Termux se naya keystore bana kar GitHub Secrets mein daal sakte ho:
- `KEYSTORE_BASE64`
- `KEYSTORE_PASSWORD`
- `KEY_ALIAS`
- `KEY_PASSWORD`

---

© 2026 SkyMeter
