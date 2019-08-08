sysopch changes for ESP32
=========================

This is a fork of MaJerle's ESP_AT_Lib to support ESP32. The changes w.r.t. the original repo are in sysopch/esp32 branch

The project I am working on is proprietary, but the changes to the library can be shared.

## Description of the changes:

### Custom init sequence

As I had to interface with SDSPI, I could not keep the standard reset sequence. See ESP_CFG_DEVICE_NEEDS_CONFIGURE

### Custom commands/info

All code protected by ESP_CFG_CUSTOM_CMDS is related to application-specific changes
 


### ESP32 support

Code different btw ESP32 and ESP8266 is protected by ESP_CFG_ESP_FLAVOR .

**NOTE** I saw MaJerle has already done some work in this direction. This is not compatible at the moment. I plan to align and merge in the new code.

### Re-enabled direct FreeRTOS suppor in esp_sys