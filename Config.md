### Config 觸發機制

> 大部分寫入行為會在進入edit之後
> 除了I/O Page 中的RTD switch 是直接外在外面
> 

### 使用的點位與認知
- 31017 (Device mode flag)(W/R)
  > 0:Normal mode
  > 1:Cloud config mode
  > 2:App config mode
  > 3:Force mode in cloud
  > 4:Force mode in Bluetooth
  > 5:FOTA 

- Device 主動離開app mode 條件為:
   1.  Device mode flag 由 0 -> 2 的 10min後
   2.  Device mode flag 在變為2 的 2min內沒有config類型指令
   
### 應用場景模擬

#### Edit模式
- 準備進入edit 中做設定前
  1. 點擊edit 前發送Read 指令檢查31017
  2. 若31017為0 表示裝置目前在Normal mode.若是為非 (0 or 2) 則跳出提示(Device is busy)
  3. 在為0 的情況下, 對 31017做寫入為2,並進入Edit模式

- 已進入edit 中做設定 (並在2min內完成設定並送出)
  1. 在按下apply 前, 檢查Device 的31017 是否為2
  2. 在2min中內所以31017為2, 正常送出寫入指令後, 並離開Edit 模式

- 已進入edit 中做設定 (編輯時間超過2min)
  1. 在按下apply 前, 檢查Device 的31017 是否為2
  2. 因為超過2min,所以31017為非2, 主動離開Edit 模式(避免資料不同步)
  
#### 無Edit模式
- 無Edit模式下的寫入設定,即刻31017為0 (切換時已決定設定值所以不會有超過2min的問題)
  1. I/O page 中 RTD/TC 的Switch 切換
  2. 切換行為觸發時, 先發送Read 指令檢查31017
  3. 若31017為0 表示裝置目前在Normal mode.若是為非 (0 or 2) 則跳出提示(Device is busy)
  4. 在為0 的情況下, 對 31017做寫入為2,再正常送出寫入指令

- 無Edit模式下的寫入設定,即刻31017為2 (切換時已決定設定值所以不會有超過2min的問題)
  1. I/O page 中 RTD/TC 的Switch 切換
  2. 切換行為觸發時, 先發送Read 指令檢查31017
  3. 若31017為0 表示裝置目前在Normal mode.若是為非 (0 or 2) 則跳出提示(Device is busy)
  4. 在為2 的情況下, 對 31017做寫入為2(可選),再正常送出寫入指令
  
