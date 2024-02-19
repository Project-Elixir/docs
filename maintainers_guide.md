<p align="center">
  <img src="https://i.imgur.com/gcOvt3T.png" />
</p>

### Introducing Project Elixir now based on Android 14 シ

<p>"Redefining your android experience with our new update which offers minimal UI enhancement and close to Stock android experience with customization."</p>

### ⊀ Unleash Innovation ⊁

Your experience while using our ROM will be buttery smooth without compromising the quality of the Android experience.

[![Download Project Elixir [Custom ROM]](https://img.shields.io/sourceforge/dm/project-elixir.svg)](https://projectelixiros.com/download) <img src="https://komarev.com/ghpvc/?username=Project-Elixir&style=flat-square" alt="Project-Elixir" />  [![Download Project Elixir [Custom ROM]](https://img.shields.io/sourceforge/dt/project-elixir.svg)](https://projectelixiros.com/download) 

Project Elixir is an AOSP-based custom Android ROM with great performance, security and stability. So do not hesitate anymore, join us now and start enjoying the beauty of stock Android. 

### Project Elixir | Maintainers Guide Begins here 💐

- You don't need source access so don't ask as we provide JENKINS.
- Read it fully for seamless experience
- You can add Miui/Oos/Leica Camera but make sure its stable
- Ship Dolby only if needed
- You can ship Lawnchair/Pixel Launcher according to your choice (By default its Lawnchair)
- After joining us make sure to adapt your trees for Jenkins and elixir 
- Also make sure its properly tested on unofficial source before sending for Jenkins build

### Reference commits:
 
- [Commit 1](https://github.com/ProjectElixir-Devices/device_oneplus_lemonades/commit/f2639e3199645898e676e863cd386744e01a4b9b)
- [Commit 2](https://github.com/ProjectElixir-Devices/device_oneplus_lemonades/commit/af9b7835b22c859f91f61a9167dfca0951a1a38e)
- [Commit 3](https://github.com/ProjectElixir-Devices/device_xiaomi_violet/commits/UNO/remove_packages)

### Mandatory things to test properly before release
- Hotspot
- Camera
- Torch 
- Updater working on your device
- Audio/video/media etc
- Customizations added in Source changelog

### Steps for releasing builds

- Make XDA thread for Release (Only if you haven't made yet) else skip
[XDA Template for A14](https://raw.githubusercontent.com/Project-Elixir/docs/UNO/xda_template.txt)
- Make Pull Req with json from CLI channel, changelog and Guide in Device Org [Important]
- Don't post any other download link in device channel post apart from this link (https://projectelixiros.com/download)
- Tag/Pm @ugly_kid_af to merge Pull req for OTA and release

### How to add things in source or report bug
- If you want anything then test it on unofficial source and ping us to add it after testing
- Report if anything is broken in source ( Don't report while source is in WIP )
- For Proper Reporting use this repo : [TAP HERE](https://github.com/Project-Elixir/issue_tracker/issues/new/choose)

```
    <!-- Whether device has dash charging support -->
    <bool name="config_hasDashCharger">false</bool>
```
```
    <!-- Whether device has warp charging support -->
    <bool name="config_hasWarpCharger">false</bool>
```
```
    <!-- Whether device has VOOC charging support -->
    <bool name="config_hasVoocCharger">false</bool>
```
```
    <!-- Whether device has turbo power charging support -->
    <bool name="config_hasTurboPowerCharger">false</bool>
```
```
    <!-- Path to fast charging status file to detect whether an oem fast charger is active -->
    <string name="config_oemFastChargerStatusPath" translatable="false">/sys/class/power_supply/battery/fastchg_status</string>
```
```
    <!-- Path to fast charging status file to detect whether an oem fast charger is active -->
    <string name="config_oemFastChargerStatusPath2" translatable="false"></string>
```
```
    <!-- Expected value from fast charging status file  -->
    <string name="config_oemFastChargerStatusValue" translatable="false">1</string>
```
```
    <!-- Allow devices override audio panel location to the left side -->
    <bool name="config_audioPanelOnLeftSide">true</bool>
```
```
    <!-- Whether devices suports in-display fingerprint when screen is off -->
    <bool name="config_supportsScreenOffUdfps">false</bool>
```
```
    <!-- Whether device has physical tri state switch -->
    <bool name="config_hasAlertSlider">false</bool>
```
```
    <!-- The location of the devices physical tri state switch
         0: Left side
         1: Right side -->
    <integer name="config_alertSliderLocation">0</integer>
```
```
    <!-- Whether key handler sends intent when changing slider position -->
    <string name="config_alertSliderIntent"></string>
```
```
    <!-- We have switched to strings! add it in OFFICIAL tree  -->
    <string name="elixir_maintainer">Saurav</string>
```
```
    <!-- AOSP Recovery  -->
    TARGET_USES_AOSP_RECOVERY := true
```
```
    <!-- Pixel Launcher -->
    EXCLUDE_LAWNCHAIR := true
```
```
    <!-- GMS product config -->
    TARGET_USES_FULL_GAPPS := true
    TARGET_USES_PICO_GAPPS := true
```
```
    <!-- Faceunlock config -->
    TARGET_FACE_UNLOCK_SUPPORTED := true
```
```
    <!-- APERTURE_CAMERA -->
    TARGET_BUILD_APERTURE_CAMERA := true
```
```
    <!-- In aosp_device.mk  -->
    ELIXIR_BUILD_TYPE := OFFICIAL
    TARGET_BOOT_ANIMATION_RES := 1080
    EXTRA_UDFPS_ANIMATIONS := true
```

### Sepolicy
- We have moved to new sepolicy structure so kindly update ur trees accordingly

- Tracked from Los :
```
path="device/qcom/sepolicy" name="android_device_qcom_sepolicy" 
  
path="device/qcom/sepolicy_vndr/legacy-um" name="android_device_qcom_sepolicy_vndr" revision="lineage-21.0-legacy-um"
  
path="device/qcom/sepolicy_vndr/sm8450" name="android_device_qcom_sepolicy_vndr" revision="lineage-21.0-caf-sm8450"
  
path="device/qcom/sepolicy_vndr/sm8550" name="android_device_qcom_sepolicy_vndr" revision="lineage-21.0-caf-sm8550"
```

- Tracked from Elixir :
```
path="device/custom/sepolicy" name="device_custom_sepolicy"

path="device/qcom/sepolicy-legacy-um" name="device_qcom_sepolicy-legacy-um"

path="hardware/qcom-caf/common" name="hardware_qcom-caf_common"
```

<p align="center">
  <img src="https://i.imgur.com/zY1Znpm.png" />
</p>
