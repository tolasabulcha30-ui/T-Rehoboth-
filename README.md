# REHOBOTH — App Android fi Website

Appii jalqabaa REHOBOTH, Afaan Oromoo. Teknooloojii: React + Vite + TypeScript + Firebase + Capacitor.

## Wanti amma keessa jiru
- Fuula galmee fi seensa Firebase Authentication.
- Profile miseensaa Firestore keessatti uumuu.
- Fuula Mana, Barumsa, Miseensota, Channels fi Chat.
- Barumsa fakkeenyaa Afaan Oromoo.
- Yaada maxxansuu fi Firestore keessatti kuusuu.
- Like barumsaaf (demo/local; lakkoofsi Firestore yoo barumsi database keessa jiraate qofa haaromfama).
- Qajeelfama Firestore fi Storage security rules.
- Qindaa'ina Capacitor Android.

**Hubachiisa:** Kun source code jalqabaa hojii ijaarsaaf qophaa'e dha; appii online irratti maxxanfame ykn APK xumurame miti. Firebase credentials galchuun, rules maxxansuun, test gochuun barbaachisa. Chat live UI fi collection irratti jalqaba qophaa'e; message list, channel permissions, moderation fi push notifications hojii itti aanu keessatti guutamuu qabu.

## 1. Firebase qopheessi
1. Firebase Console bani: https://console.firebase.google.com/
2. Project kee filadhu: `rehoboth-6e5f5`.
3. Web App config keessaa values fudhadhu.
4. Authentication > Sign-in method keessatti Email/Password enable godhi.
5. Firestore Database uumii.
6. Storage enable godhi.
7. Firestore Rules keessaa `firestore.rules` maxxansi; Storage Rules keessaa `storage.rules` maxxansi.

## 2. Config galchi
`.env.local` faayila qindaa’e ZIP kana keessatti jira; gatiiwwan Firebase project `rehoboth-6e5f5` kee itti galfamaniiru. Faayila kana GitHub irratti hin maxxansin, nama biraattis hin qoodin. `apiKey` fi `appId` Firebase console keessaa fudhadhu. `.env.local` GitHub irratti hin maxxansin.

## 3. Website jalqabi
Node.js LTS install godhi. Terminal keessatti:
```bash
npm install
npm run dev
```
Vite URL local irratti agarsiisu bana.

Website production build:
```bash
npm run build
```
Bu'aan `dist/` keessa uumama. Hosting irratti deploy gochuuf Firebase Hosting ykn hosting biraa qindeessi.

## 4. Android APK qopheessi
Android Studio fi Android SDK install godhi. Ergasii:
```bash
npm install
npx cap add android
npm run android:sync
npm run android:open
```
Android Studio keessatti Build > Generate Signed Bundle / APK filadhu. APK sirrii maxxansuuf application ID, icon, signing key fi test dabalataa barbaachisu.

## 5. Admin jalqabaa
Account admin amanamaa tokko erga uumtee booda, Firebase Console > Firestore > `users` > document UID isaa bani; field `role` gatii `admin` godhi. Nama amanamaa qofa admin godhi. App keessatti role ofumaan admin gochuun hin hayyamamu.

## 6. Waan hojii itti aanu keessatti xumuramuu qabu
- Admin dashboard fi role management UI.
- Teacher-only lesson publishing.
- Realtime chat message stream fi DM.
- Channels database, subscriptions fi moderation.
- Password reset, email verification, profile edit.
- Push notifications, reporting/blocking, pagination.
- Afaan Oromoo proofreading, privacy policy fi terms.
- Full security review, tests, hosting deployment fi signed APK.

## Nageenya
- Password appichi hin kuusu; Firebase Authentication to'ata.
- Firebase config public web config dha; garuu Firestore/Storage Rules nageenya murteessu.
- Admin role console irraa qindeessi; role admin user irraa hin fudhatin.
- Dubbii amantii irratti namoota ykn gareewwan amantii hin arrabsin; madda, yaada fi hiika adda baasi.
