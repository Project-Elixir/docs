<p align="center">
  <img src="https://github.com/Project-Elixir/docs/blob/bkl/res/elixir-a16banner.png" />
</p

<br>   

### Project Elixir | Maintainers Guide Begins here シ

"Redefine Simplicity with your android experience on our minimalistic custom rom — where sleek design meets robust security, performance, and stability." Elevate your user interface with minimalist design and with the striking of perfect balanced customization options, customize with ease. Project Elixir is an AOSP-based custom Android ROM with great performance, security and stability. So do not hesitate anymore, join us now and start enjoying the beauty of stock Android.

[![Download Project Elixir [Custom ROM]](https://img.shields.io/sourceforge/dm/project-elixir.svg)](https://projectelixiros.com/download) <img src="https://komarev.com/ghpvc/?username=Project-Elixir&style=flat-square" alt="Project-Elixir" />  [![Download Project Elixir [Custom ROM]](https://img.shields.io/sourceforge/dt/project-elixir.svg)](https://projectelixiros.com/download) 

> [!Warning]
> - You don't need source access so don't ask as we provide JENKINS.
> - Read this guide step by step to avoid issues in anything
> - You can add Miui/Oos/Leica Camera & Dolby/Viper but make sure its stable
> - You can ship Lawnchair/Pixel Launcher according to your choice. (By default its Pixel Launcher)
> - After joining us make sure to adapt your trees for Jenkins and elixir 
> - Also make sure its properly tested on unofficial source before sending for Jenkins build

<br>

> [!Important]
> **Reference commits:**
> - [Elixir Bringup & OFFICIAL Flags](https://github.com/ProjectElixir-Devices/device_xiaomi_violet/commit/e3a09107048bd36ab1bb4c96e2e4440bc249e206) 
> - [Adding vendorsetup & Remove txt](https://github.com/ProjectElixir-Devices/device_oneplus_lemonades/commit/af9b7835b22c859f91f61a9167dfca0951a1a38e) 
> - [Adding Remove Pkg to debloat](https://github.com/ProjectElixir-Devices/device_xiaomi_violet/commit/364a662fdcf239a165d035512901f4f5dbe9eaac)


<br>

> [!Note] 
> **Mandatory things to test properly before release**
> - Hotspot is working or not
> - Camera is working or not
> - Torch is working or not
> - Updater working on your device or needs some changes for flashing
> - Audio/video/media etc is working or not
> - Customizations added in Source changelog is working or not

### How to add things in source or report bug
- If you want anything then test it on unofficial source and ping us to add it after testing
- Report if anything is broken in source ( Don't report while source is in WIP )
- For Proper Reporting use this repo : [TAP HERE](https://github.com/Project-Elixir/issue_tracker/issues/new/choose)

<br>

### Adapt your tree according to elixir 
~ *check below strings/flags and add or adapt if needed for your device*

<br>

**Whether device has dash charging support**
```
<bool name="config_hasDashCharger">false</bool>
```

**Whether device has warp charging support**
```
<bool name="config_hasWarpCharger">false</bool>
```

**Whether device has VOOC charging support**
```
<bool name="config_hasVoocCharger">false</bool>
```

**Whether device has turbo power charging support**
```
<bool name="config_hasTurboPowerCharger">false</bool>
```

**Path to fast charging status file to detect whether an oem fast charger is active**
```
<string name="config_oemFastChargerStatusPath" translatable="false">/sys/class/power_supply/battery/fastchg_status</string>
```

**Path to fast charging status file to detect whether an oem fast charger is active**
```
<string name="config_oemFastChargerStatusPath2" translatable="false"></string>
```

**Expected value from fast charging status file**
```
<string name="config_oemFastChargerStatusValue" translatable="false">1</string>
```

**Allow devices override audio panel location to the left side**
```
<bool name="config_audioPanelOnLeftSide">true</bool>
```

**Whether devices suports in-display fingerprint when screen is off**
```
<bool name="config_supportsScreenOffUdfps">false</bool>
```

**Whether device has physical tri state switch**
```
<bool name="config_hasAlertSlider">false</bool>
```

**The location of the devices physical tri state switch**
         0: Left side
         1: Right side 
```         
<integer name="config_alertSliderLocation">0</integer>
```

**Whether key handler sends intent when changing slider position**
```
<string name="config_alertSliderIntent"></string>
```

**Elixir Recovery**
```
TARGET_USES_AOSP_RECOVERY := true
```

**Lawnchair Launcher**
```
FORCE_LAWNCHAIR := true
```

**GMS product config**
```
WITH_GMS := true
```

**Faceunlock gets build by default if u want to disable it, then**
```
TARGET_FACE_UNLOCK_SUPPORTED := false
```

**For APERTURE CAMERA**
```
TARGET_BUILD_APERTURE_CAMERA := true
```

**In lineage_device.mk**
~ Now Elixir is based on lineage from Android 16
```
ELIXIR_BUILD_TYPE := OFFICIAL
BUILD_USERNAME := Elixir
BUILD_HOSTNAME := Elixir
```

**For Extra UDFPS Animation**
```
EXTRA_UDFPS_ANIMATIONS := true
```

**We have switched to strings! add it in OFFICIAL tree**
```
<string name="elixir_maintainer">Saurav</string>
```

<br>

> [!Warning]
> **All the maintainers must follow templates for wiki,changelog,and OTA strictly**
> - Template for Installation Guide : [Tap Here](https://github.com/ProjectElixir-Devices/Wiki/blob/bkl/template_for_wiki.md)
> - Template for Changelog : [Tap Here](https://github.com/ProjectElixir-Devices/Changelogs/blob/bkl/template_for_changelog.md)
> - Template for OTA Repo : [Tap Here](https://github.com/ProjectElixir-Devices/official_devices/commit/ff2850392a0ba2f1392dd9b4be686a57bc83d624)

<br>

> [!Important]
> **Steps for releasing builds**
> - Make Proper Wiki/Flashing Gudide for your Device with Warning,Important,Reqired Files and Notes
>   * **[Template for Installation Guide](https://github.com/ProjectElixir-Devices/Wiki/blob/bkl/violet.md)**
>
> - Make Pull Request to `official_devices` repo with json from CLI(jenkins) channel build post and changelog with proper path in Device Org
>   * **[Template for OTA Repo](https://github.com/ProjectElixir-Devices/official_devices/commit/ff2850392a0ba2f1392dd9b4be686a57bc83d624)**
>
> - Don't post any other **download link** in device channel post apart from this link below
>   * **[OFFICIAL WEBSITE DOWNLOAD PAGE](https://projectelixiros.com/download)**
>    
> - Tag/Pm **[Saurav](https://telegram.me/ugly_kid_af)** with the build link that you want to release and to merge Pull req for OTA!

<p align="center">
  <img src="https://github.com/Project-Elixir/docs/blob/bkl/res/elixir-copyright.png" />
</p
