# **Unreal Engine 5 mobiilimängude arendamine Androidile**

## **Eeltingimused**

Enne alustamist veendu, et sul on paigaldatud järgmised tööriistad:

- **Unreal Engine 5** ([Laadi alla Epic Games Launcherist](https://www.unrealengine.com/))
- **Android Studio** ([Laadi alla Android Developerist](https://developer.android.com/studio))
- **Java Development Kit (JDK)** (Tuleb koos Android Studio-ga või laadi alla eraldi [siit](https://adoptium.net/))
- **Android SDK, NDK ja silumisvahendid** (Paigalda Android Studio kaudu)

---

## **Samm 1: Androidi arenduskeskkonna seadistamine**

1. Ava **Android Studio** ja mine **SDK Managerisse**.
2. Paigalda järgmised komponendid:
   - **Android SDK** (soovitatavalt uusim versioon)
   - **Android NDK** (Unreal Engine 5 nõuab NDK versiooni **25.1.8937393 või uuemat**)
   - **Android SDK käsurea tööriistad**
   - **Android Build Tools** (uusim versioon)
3. Seadista keskkonnamuutujad:
   - **`ANDROID_HOME`** -> Tee Android SDK-le (nt `C:\Users\SinuKasutaja\AppData\Local\Android\Sdk`)
   - Lisa SDK tööriistad ja platvormitööriistad `PATH`-i:
     ```
     C:\Users\SinuKasutaja\AppData\Local\Android\Sdk\tools
     C:\Users\SinuKasutaja\AppData\Local\Android\Sdk\platform-tools
     ```

---

## **Samm 2: Unreal Engine seadistamine Androidi jaoks**

1. Ava **Unreal Engine 5**.
2. Mine **Edit** -> **Project Settings** -> **Platforms** -> **Android**.
3. **"Android SDK Configuration"** all:
   - Määra **SDK, NDK ja JDK** kaustad õigesti.
4. **"Android Packaging"** all:
   - Luba **Support for arm64** (vajalik tänapäevaste Android-seadmete jaoks).
   - Määra **Minimum SDK Version** `android-24` või kõrgemaks.
5. Salvesta ja taaskäivita **Unreal Engine**.

---

## **Samm 3: Testi oma mängu Android-seadmes**

1. **Ühenda Android-seade** USB kaudu arvutiga või emuleeri seda.
2. Luba **Developer Mode** ja pane **4x MSAA**.
3. Unreal Engine-is mine **Platforms** ja vali oma **device**.
4. Kui kõik on õigesti seadistatud, peaks mäng käivituma sinu **Android-seadmes**.

---

## **Samm 4: Pakenda ja ehita mäng Androidile**

1. Mine **File** -> **Package Project** -> **Android (ASTC või ETC2)**.
2. Vali **sihtkaust** ja oota, kuni **ehitusprotsess** lõpeb.

---

Nüüd oled valmis alustama mobiilimängude arendamist **Unreal Engine 5** abil! 🚀

