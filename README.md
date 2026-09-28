# AxionFx

## Usage

Add this repo to your device's `evolution.dependencies`

```json  
{
    "repository"  : "Evolution-X-Devices/packages_apps_AxionFx",
    "remote"      : "github-non-los",
    "branch"      : "cnb",
    "target_path" : "packages/apps/AxionFx"
}
```

<br>

Include in your `device.mk`
```makefile
$(call inherit-product, packages/apps/AxionFx/config.mk)
```

<br>

Add to `audio_effects.xml` (if HIDL audio) otherwise `audio_effects_config.xml` (for AIDL audio)
```xml
<library name="axfx_aidl" path="libaxionfxaidl.so"/>

<effect name="axionfx" library="axfx_aidl" uuid="f35cb927-a887-4f3d-847f-770634486d53" type="5867be72-4060-4c55-a378-c1cdef3e1353"/>
```
