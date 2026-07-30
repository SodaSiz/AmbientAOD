# Pixel 9 Pro AOD Wallpaper Enabler (KernelSU / Magisk Module)

An elegant, lightweight Runtime Resource Overlay (RRO) module designed for the Pixel 9 Pro to force-enable the hidden **"Show lock screen wallpaper on Always-On Display"** setting. 

Google artificially restricts this feature on certain Pixel models. This module modifies the framework configuration natively without touching system files, allowing you to enjoy a dimmed version of your wallpaper on the AOD screen.

---

## 🚀 Features
* **Native Integration:** Directly unlocks the official option inside `Settings > Display > Lock Screen > Always-on mode`.
* **100% Systemless:** Powered by KernelSU / Magisk. Safe, clean, and easily uninstallable.
* **Battery-Friendly:** Uses Android's built-in RRO (Static Overlay) architecture, meaning zero background battery drain or overhead.

## 🛠️ How It Works
The module injects a static configuration overlay targeting `framework-res.apk`. It forces the boolean value `config_dozeSupportsAodWallpaper` to `true` with maximum priority (`9999`), bypassing Google's default hardware restrictions.

---

## 📦 Installation

### Prerequisites
* A Pixel 9 Pro rooted with **KernelSU**, **KernelSU-Next**, or **Magisk**.
* Always-on Display enabled in your system settings.

### Steps
1. Download the latest `pixel_aod_wallpaper.zip` from the [Releases](https://github.com/YOUR_USERNAME/YOUR_REPO/releases) section.
2. Open your Root Manager app (KernelSU or Magisk).
3. Go to the **Modules** tab, click **Install from storage**, and select the `.zip` file.
4. Reboot your device.
5. Go to **Settings > Display > Lock Screen > Always-on mode** and toggle the new **"Show lock screen wallpaper"** switch!

---

## 🇫🇷 Version Française (Description Rapide)
Ce module KernelSU/Magisk active l'option masquée par Google permettant d'**afficher le fond d'écran sur l'écran de veille permanent (Always-On Display)** sur le Pixel 9 Pro. 

Il utilise un overlay statique système (RRO) ultra-léger pour passer la variable `config_dozeSupportsAodWallpaper` à `true`. 
* **Installation :** Flashez le `.zip` via KernelSU ou Magisk, redémarrez, et activez la nouvelle option apparue dans vos paramètres d'écran de verrouillage !

---

## 🧑‍💻 Developer Notes (Compilation)
If you wish to build the APK yourself from the source:
1. Compile the resources using `aapt2 link --manifest AndroidManifest.xml -I android.jar compiled_res.zip -o EnableAodWallpaper.apk`
2. Ensure `android:isStatic="true"` and `android:priority="9999"` are set in the `AndroidManifest.xml` to avoid `SecurityException: commit failed` on Android 14/15+.
3. Zip the `module.prop` and `system/` directory structure directly (do not zip the parent folder).

## 📄 License
This project is open-source and licensed under the MIT License. Feel free to share and modify!

