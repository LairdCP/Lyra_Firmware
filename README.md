[![Ezurio](/images/ezurio_logo.jpg)](https://www.ezurio.com/)

# Lyra Firmware

[![Lyra-P & Lyra-S](/images/lyra_p_and_lyra_s_render.jpg)](https://www.ezurio.com/wireless-modules/bluetooth-modules/bluetooth-5-modules/lyra-series-bluetooth-53-modules)
[![Silabs](/images/silabs_logo.jpg)](https://www.silabs.com)
[![Gecko SDK](/images/gecko_sdk_logo.jpg)](https://www.silabs.com/developers/gecko-software-development-kit)
[![Simplicity Studio](/images/simplicity_studio_logo.jpg)](https://www.silabs.com/developers/simplicity-studio)

This is the firmware release page for the Ezurio [Lyra][Lyra product brief] product family.

The product is available in [P (PCB module)][Lyra P module datasheet] & [S (System In Package)][Lyra S module datasheet] variants.

---
**_Note:_** The latest available firmware releases are available on the [Lyra Releases Page].

Details for flashing the different image types can be found in the [Firmware options and upgrade guide] application note.

---

---
**_Note:_** Lyra DVKs with revision 2.3 or below use alternate labelling for SW1.

The 'BGx' position should be used when programming the Lyra Bootloader, AT Interface and Bluetooth Xpress.

The 'AT / SWO' position should be used when performing native C development.

---

# Content

All firmware is offered in P and S versions, depending upon the Lyra variant in use.

## AT Interface

The [Lyra AT Interface][Lyra AT Interface guide] application builds upon many years of AT Interface experience gained with Ezurio's BL65x range of Bluetooth modules. It offers a VSP service for cable replacement applications and GATT client and server functionality. Please find [here][Lyra AT Interface release notes] the latest release notes.

Binaries are available for transfer using SWD and OTA and UART bootloader.

## Bluetooth Xpress

For legacy [Bluetooth Xpress][Bluetooth Xpress] users, Bluetooth Xpress firmware is available for usage with the Lyra P & S modules. Note this is a frozen release and further updates will not be supported.

Further details are available in the [Bluetooth Xpress migration guide][Bluetooth Xpress migration guide].

Binaries are available for transfer using SWD and UART bootloader.

## Bootloader

The Bootloader is required for operation of all other applications, and is also needed when performing [native C development][Native C development guide]. This should be the first application programmed to the target device.

Further details of usage of the bootloader can be found in the [Firmware options and upgrade guide][Firmware options and upgrade guide].

Bootloaders are also included for use with legacy Bluetooth Xpress hardware designs. Note these differ in the location of the BOOT pin defined by the Bootloader as follows.

|   Bootloader Type  | Lyra P BOOT Pin | Lyra S BOOT Pin |
|--------------------|-----------------|-----------------|
| Ezurio             |      PC07       |      PA06       |
| Bluetooth Xpress   |      PD02       |      PD02       |

Binaries are available for transfer using SWD only. Please note that by default all Lyra modules ship with the Ezurio bootloader type preprogrammed.

## DTM

Two DTM applications are available for testing the Lyra BLE radio performance in conjunction with the [Lyra P DVK][Lyra P DVK user guide]
and [Lyra S DVK][Lyra S DVK user guide]. These are described as follows.

Binaries are available for transfer using SWD and OTA and UART bootloader.

### BGAPI

This is used in conjunction with [tools supplied by Silabs][Silabs BGAPI DTM documentation]. Communication is performed using the [BGAPI][Silabs BGAPI description] protocol. Refer also to our [Lyra P BGAPI DTM][Lyra P BGAPI DTM Application Note] and [Lyra S BGAPI DTM][Lyra S BGAPI DTM Application Note] application notes for more details.

### BTSIG

This is used in conjunction with BT-SIG approved DTM test equipment. Communication is performed using the native DTM protocol as defined in the BLE specification. You can find more information in the Bluetooth SIG Bluetooth Core Specification Version 5.3 | Vol 6 (Low Energy Controller) | Part F (Direct Test Mode) which is available under [https://www.bluetooth.com/specifications/bluetooth-core-specification][Bluetooth SIG Core Specification].

[Lyra product brief]: <https://www.ezurio.com/documentation/product-brief-lyra-series>
[Lyra P module datasheet]: <https://www.ezurio.com/documentation/datasheet-lyra-p>
[Lyra S module datasheet]: <https://www.ezurio.com/documentation/datasheet-lyra-s>
[Lyra AT Interface guide]: <https://www.ezurio.com/documentation/user-guide-at-interface-application-lyra-22-24-series >
[Lyra AT Interface release notes]: <https://www.ezurio.com/documentation/release-notes-lyra-24-p-s-v3-3-x>
[Bluetooth Xpress]: <https://docs.silabs.com/gecko-os/1/bgx/latest/getting-started>
[Lyra P DVK user guide]: <https://www.ezurio.com/documentation/user-guide-lyra-p-development-kit>
[Lyra S DVK user guide]: <https://www.ezurio.com/documentation/user-guide-lyra-s-development-kit>
[Native C development guide]: <https://www.ezurio.com/documentation/user-guide-lyra-series-c-code-development>
[Firmware options and upgrade guide]: <https://www.ezurio.com/documentation/user-guide-firmware-options-and-upgrading-lyra-series>
[Lyra P BGAPI DTM Application Note]: <https://www.ezurio.com/documentation/application-note-using-bgapi-direct-test-mode-lyra-p>
[Lyra S BGAPI DTM Application Note]: <https://www.ezurio.com/documentation/application-note-using-bgapi-direct-test-mode-lyra-s>
[Bluetooth SIG Core Specification]: <https://www.bluetooth.com/specifications/bluetooth-core-specification>
[Bluetooth Xpress migration guide]: <https://www.ezurio.com/documentation/user-guide-bluetooth-xpress-bgx-migration-lyra-modules>
[Silabs BGAPI DTM documentation]: <https://www.silabs.com/documents/public/application-notes/an1267-bt-rf-phy-evaluation-using-dtm-sdk-v3x.pdf>
[Silabs BGAPI description]: <https://docs.silabs.com/bluetooth/3.1/bgapi>
[Lyra Releases Page]: <https://github.com/LairdCP/Lyra_Firmware/releases/tag/GA3.1>
