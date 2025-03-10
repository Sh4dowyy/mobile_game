Unreal Engine mängu paigaldamine BlueStacks emulaatorisse

See juhend aitab sul oma Unreal Engine'is loodud Android-mängu käivitada BlueStacks emulaatoris.

---

## Eeltingimused
- **Unreal Engine** (koos Android SDK, NDK ja JDK seadistustega)
- **BlueStacks** (uusim versioon, saadaval aadressil [bluestacks.com](https://www.bluestacks.com/))
- **ADB (Android Debug Bridge)**, mis on saadaval Android Studio või eraldi tööriistana

---

## 1. BlueStacks emulaatori ettevalmistamine
1. **Ava BlueStacks ja aktiveeri ADB**
   - Ava **Seaded** → **Täpsem**
   - Luba **Android Debug Bridge (ADB)**
   - Taaskäivita BlueStacks, et muudatused rakenduksid

2. **Loo ADB ühendus**
   - Ava terminal või käsumootor ja käivita:
     ```sh
     adb connect 127.0.0.1:5555
     ```
   - Kontrolli, kas ühendus õnnestus:
     ```sh
     adb devices
     ```
   - Kui näed nimekirjas "127.0.0.1:5555", on ühendus aktiivne.

---

## 2. Mängu pakendamine Unreal Engine'is
1. **Seadista Android SDK**
   - Ava `Muuda` → `Projekti seaded` → `Platvormid` → `Android`
   - Veendu, et Android SDK, NDK ja JDK rajad on õigesti määratud.
   - Kui vaja, kasuta **Unreal Setup Android Tool**-i.

2. **Loo APK-fail**
   - Ava `Fail` → `Pakenda projekt` → `Android` → Vali sobiv tekstuurikompressioon (nt **ETC2**).
   - Oota, kuni Unreal Engine loob APK-faili (`Saved/StagedBuilds/` kaustas).

---

## 3. Mängu paigaldamine BlueStacks-i
### **Meetod 1: Lohistamine**
- Lohista **APK-fail** otse BlueStacks aknasse.
- Installimine algab automaatselt.

### **Meetod 2: ADB kaudu**
- Ava terminal/käsumootor ja sisesta:
  ```sh
  adb install tee-sinu-apk-failini.apk
  ```
- Kui installimine on edukas, ilmub mäng BlueStacks-i rakenduste nimekirja.

---

## 4. Mängu käivitamine ja optimeerimine
- Ava BlueStacks ja käivita mäng.
- Kui esineb viivitusi, mine `Seaded` → `Jõudlus` ja suurenda **CPU tuumade** ja **RAM-i** eraldust.

---
