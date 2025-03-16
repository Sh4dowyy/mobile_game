Unreal Engine 5 mobiilimängude arendamine Androidile

Eeltingimused

Enne alustamist veendu, et sul on paigaldatud järgmised tööriistad:

Unreal Engine 5 (Laadi alla Epic Games Launcherist)

Android Studio (Laadi alla Android Developerist)

Java Development Kit (JDK) (Tuleb koos Android Studio-ga või laadi alla eraldi siit)

Android SDK, NDK ja silumisvahendid (Paigalda Android Studio kaudu)

Samm 1: Androidi arenduskeskkonna seadistamine

Ava Android Studio ja mine SDK Managerisse.

Paigalda järgmised komponendid:

Android SDK (soovitatavalt uusim versioon)

Android NDK (Unreal Engine 5 nõuab NDK versiooni 25.1.8937393 või uuemat)

Android SDK käsurea tööriistad

Android Build Tools (uusim versioon)

Seadista keskkonnamuutujad:

ANDROID_HOME -> Tee Android SDK-le (nt C:\Users\SinuKasutaja\AppData\Local\Android\Sdk)

Lisa SDK tööriistad ja platvormitööriistad PATH-i:

C:\Users\SinuKasutaja\AppData\Local\Android\Sdk\tools
C:\Users\SinuKasutaja\AppData\Local\Android\Sdk\platform-tools

Samm 2: Unreal Engine seadistamine Androidi jaoks

Ava Unreal Engine 5.

Mine Edit -> Project Settings -> Platforms -> Android.

"Android SDK Configuration" all:

Määra SDK, NDK ja JDK kaustad õigesti.

"Android Packaging" all:

Luba Support for arm64 (vajalik tänapäevaste Android-seadmete jaoks).

Määra Minimum SDK Version android-24 või kõrgemaks.

Salvesta ja taaskäivita Unreal Engine.

Samm 3: Testi oma mängu Android-seadmes

Ühenda Android-seade USB kaudu arvutiga või emuleeri seda

Luba developer mode ja pane 4x MSAA.

Unreal Engine-is mine Platforms ja vali oma device.

Kui kõik on õigesti seadistatud, peaks mäng käivituma sinu Android-seadmes.

Samm 5: Pakenda ja ehita mäng Androidile

Mine File -> Package Project -> Android (ASTC või ETC2).

Vali sihtkaust ja oota, kuni ehitusprotsess lõpeb.

Loodud .apk või .aab faili saab installida seadmesse või üles laadida Google Play poodi.
