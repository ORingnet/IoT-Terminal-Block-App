# Release Notes

## 2.6.1 A1
### 重大更新 
- 加入App Config 切換機制
- 第一次連進裝置時, 除了新建藍芽密碼, 再加上新建裝置名稱

### 目前功能
- Dashboard (功能正常)
- I/O (功能正常)
- DI (功能正常)
- DO (功能正常)
- AI (功能正常)
- RTD/TC (功能正常)
- Device Info (功能正常)
- Cloud Setting (功能正常)
- Gateway (功能正常)
- Remote Control (功能正常)

### 尚未完成 
- Network Status
- Error Status

### 更新解決的 ISSUE
[#28702 ](http://192.168.2.30/redmine/issues/28705)  
[#27865 ](http://192.168.2.30/redmine/issues/27865)  
[#28705 開關 DO/Relay swich自行彈回](http://192.168.2.30/redmine/issues/28705)  
[#28707 設定之密碼可輸入低於6碼和超過12 碼](http://192.168.2.30/redmine/issues/28707)  
[#28716 Trigger無法設定](http://192.168.2.30/redmine/issues/28716)  
[#28720 Reset password UI 無須輸入Current password也可修改密碼](http://192.168.2.30/redmine/issues/28720)  
[#28852 Dashboard,IO 顯示值不會自動更新](http://192.168.2.30/redmine/issues/28852)  
[#28868 AI configure - Alarm設定失效](http://192.168.2.30/redmine/issues/28868)  
[#28871 RTD/TC switch 選單問題](http://192.168.2.30/redmine/issues/28871)  

### 待解決ISSUE
[#28714 DI/DO/Relay/AI/RTC/TC 內的 箭頭 符號](http://192.168.2.30/redmine/issues/28714)  
[#28874 RTD/TC/CJC 讀值的顯示問題](http://192.168.2.30/redmine/issues/28874)  


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
