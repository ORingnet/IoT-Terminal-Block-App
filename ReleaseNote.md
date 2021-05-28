# Release Notes

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adhere to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
App download [Install](https://play.google.com/apps/internaltest/4699210505717851596)

## 2.5.7A6 Iot Terminal Block App 2021-05-26
### Added
- Remote Control Page
- Remote Control Page -> Button(Remote/BLE) when switching between remote mode and BLE mode.

- Slide Menu
- Build I/O Page for remote mode
- Build Dashboard Page for remote mode
- Build Gateway Page for remote mode

## 2.5.7A5 Iot Terminal Block App 2021-05-26
### Added 
- Remote Control Page
- Remote Control Page -> Button(Remote) for Remote mode.

### Changed
- Api Server
- api domain name -> https://api.iot-terminal-block.wmc.idc.oringnet.cloud
- AccessToken check-rules changed.

- Initial Page
- Check AccessToken in Remote mode.
- Save AccessToken when OAuth response is success.  


## 2.5.7A4 Iot Terminal Block App 2021-05-25
### Added 
- Network Status Page
- Network Status -> Info list -> RSSI (BLE)
- Network Status -> Info list -> MCC (BLE)
- Network Status -> Info list -> ORDER NUMBER (BLE)
- Network Status -> Info list -> BAND CatM1 (BLE)
- Network Status -> Info list -> BAND NB1 (BLE)

### Changed
- Dashboard Page copy from I/O Page
- Slide menu default page -> Dashboard Page

## 2.5.7A3 Iot Terminal Block App 2021-05-10
### Added
- Gateway page for menu 
- Gateway page -> 32 Channel switch button (BLE mode)
- Gateway page -> RTU Setting (BLE mode)
- Gateway page -> Item Detail (BLE mode)

- Cloud Setting Page
- Cloud Setting -> Info list -> CLOUD_CONFIG (BLE mode)
- Cloud Setting -> Info list -> MQTT Broker (BLE mode)
- Cloud Setting -> Info list -> Broker port (BLE mode)
- Cloud Setting -> Info list -> Client ID (BLE mode)
- Cloud Setting -> Info list -> User Name (BLE mode)
- Cloud Setting -> Info list -> User Password (BLE mode)
- Cloud Setting -> Edit Button (BLE mode)
- Cloud Setting -> Edit mode -> Cloud Connection (BLE mode)
- Cloud Setting -> Edit mode -> Broker Address (BLE mode)
- Cloud Setting -> Edit mode -> Port (BLE mode)
- Cloud Setting -> Edit mode -> Client ID (BLE mode)
- Cloud Setting -> Edit mode -> UserName (BLE mode)
- Cloud Setting -> Edit mode -> Password (BLE mode)

### Fixed
- Fixed a bug where pending transactions would get stuck in the cloud setting page.
- Fixed a bug where multiple thread running at the same time would issue a loading dialog.



