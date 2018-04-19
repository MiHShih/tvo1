# CONDET

CONDET 可用於搜尋一個或多個連續波形資料庫中的地震，可以使用SEISAN本身的連續資料或其他程式的建立之波形資料庫（SeisComp 或 BUD）。

這個指令分兩步驟，

1. 在個測站之單一 channel 上進行搜尋。
2. 依照同時段內所偵測之訊號數量，初步判斷是否為地震事件。 

指令中有三種不同的檢測方法:

1\) standard squared STA/LTA,

2\) Carl John- son’s detector.

3\) correlation with master event.



執行方式如下，利用 Seiscomp 所建立波形資料庫 \(SDS\)，進行測試。

* 進入 WOR/TVO

* 將參數文件 condet.par 從 DAT 複製到 WOR/TVO。首先檢查 CONDET 輸入文件 'condet.par'。修改的參數中所選用的檢測算法及其參數，濾波器和網路檢測設定。

* Now run the program by typing ‘condet’, it automatically uses condet.par as input file. The program runs one station after the other. The main output files are ‘condet.out’ listing all the trigger times, ‘extract.batch’ – a script file to extract the data using the program WAVETOOL, and ‘condet.trace’ which lists the data intervals that were read. Check all these files.

* 使用 condet時，會自動讀取condet.par。主輸出文件是列出所有觸發時間的'condet.out'，'extract.batch' - 使用程序WAVETOOL提取數據的腳本文件，以及列出讀取的數據間隔的'condet.trace'。 檢查所有這些文件。



