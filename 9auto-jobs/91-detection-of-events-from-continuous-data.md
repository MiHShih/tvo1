# CONDET

CONDET 可用於搜尋一個或多個連續波形資料庫中的地震，可以使用SEISAN本身的連續資料或其他程式的建立之波形資料庫（SeisComp 或 BUD）。

這個指令分兩步驟，

1. 在個測站之單一 channel 上進行搜尋。
2. 依照同時段內所偵測之訊號數量，初步判斷是否為地震事件。 

指令中有三種不同的搜尋方法:

1\) standard squared STA/LTA,

2\) Carl John- son’s detector.

3\) correlation with master event.

執行方式如下，文中利用 Seiscomp 所建立波形資料庫 \(SDS\)，進行測試。

1. 進入 WOR/TVO
2. 將參數文件 condet.par 從 DAT 複製到 WOR/TVO。並修改的 condet.par 參數檔中所選用的搜尋方法及其參數，濾波器
3. 執行 condet 時，會自動讀取 condet.par。

主要輸出文件如下：

* condet.out: 列出所有訊號的時間。
* extract.batch: 使用WAVETOOL 擷取地震事件之波形資料的 scripts 檔。
* condet.trace:列出讀取的數據間隔。



