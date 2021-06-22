### Config 觸發機制

> 大部分寫入行為會在進入edit之後
> 除了I/O Page 中的RTD switch 是直接外在外面
> 

### 使用的點位與認知
- 41018 (Cloud Config Mode)
  > 0:Normal mode
  > 1:Cloud config mode
  > 

- 4XXXX (App Config Mode)
  > 0:Normal mode
  > 1:App Config Mode
  > 在Device 在4XXXX 被切換成1時, 預設保護時間5 min 為app mode
  >  
- 離開app mode 條件為:
   1.  App Config Mode 由 0 -> 1 後的5 分鐘
   2.  APP 主動將 App Config Mode 設定回 0

### 應用場景模擬
- 準備進入edit 中做設定
  1. 點擊edit 前發送Read 指令檢查41018 
  2. 若41018 為0 表示裝置目前在一般模式,app 可以開始下控.若是為1 表示Cloud 設定中, 跳出提示(Device is busy)
  3. 在為0 的情況下, 對 4XXXX做寫入為1,並進入Edit模式
  4. 在按下apply 前, 檢查Device 的4XXXX 是否為1
  5. 若 4XXXX 為1, 正常送出寫入指令後, 將4XXXX 設定回 0, 並離開Edit 模式
  6. 若 4XXXX 為0, 先發送Read 指令檢查41018 
  7. 若 41018 為1, 則離開Edit 模式
  8. 若 41018 為0, 則對4XXXX做寫入為1,再正常送出寫入指令後, 將4XXXX 設定回 0, 並離開Edit 模式

- 無編輯模式下的寫入設定
  1. I/O page 中 RTD/TC 的Switch 切換
  2. 切換行為觸發時, 先發送Read 指令檢查41018
  3. 若41018 為0 表示裝置目前在一般模式,app 可以開始下控.若是為1 表示Cloud 設定中, 跳出提示(Device is busy)
  4. 在為0 的情況下, 對 4XXXX做寫入為1,再正常送出寫入指令後, 並將4XXXX 設定回 0


  
