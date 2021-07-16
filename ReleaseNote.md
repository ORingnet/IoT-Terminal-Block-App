# Release Notes

## v2.6.0 A1 

### 重大更新
- 本次改版將舊的點位變更為新版(v1.0.0)點位

### 測試
- 由於新版本需配合App Config mode 來操作(尚未完成), 故此版本無法做全面性的有效測試

### 目前功能
- Dashboard 數據查看
- I/O 數據查看
- Device Info 數據查看
- Cloud Setting 數據查看
- Gateway 數據查看
- Remote Control (功能正常)

### 新增
1. Ai Config 頁面加入 Detection threshold 模塊(包含 Enable , Detection threshold, XY% Detection threshold)
2. 在 Cloud Setting 中若選擇 ORing Cloud 後按下apply, 只會對Address(41016) 寫入為1 , 不會對 Broker Address 與 port 做寫入

### 尚未完成
- 每一頁可做設定的項目都需要加上 App config Mode 機制
- Network Ststus頁
- 第一次連進裝置時, 除了新建藍芽密碼, 再加上新建裝置名稱
- 移除 DeviceInfo 的 編輯裝置名稱功能
- CloudSetting 的平台選擇項目Cloud Connection 只會在第一次初始化時可以選, 之後若需要重新選擇平台必須手動重置裝置來做初始化
- 新增Error Status 頁面
