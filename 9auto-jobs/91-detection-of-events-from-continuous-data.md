The program CONDET can be used to detect events in one or more continuous databases, either a SEISAN continous data base or an archive \(SeisComp or BUD types\).

CONDET 可用於搜尋一個或多個連續數據庫中的地震事件，可以是SEISAN的連續數據庫或其他程式的波形資料（SeisComp或BUD類型）。

該程序分兩步驟，首先在單一channel 上運行檢測器，其次檢測超過最小數量站的事件。 可以應用在臨時地震網的數據（例如，餘震監測，其中連續記錄而沒有事件檢測）以及用於即時資料參數的調整與測試。

程式中有三種不同的檢測方法:

1\) standard squared STA/LTA,

2\) Carl John- son’s detector.

3\) correlation with master event.

執行方式如下，利用 Seiscomp 所建立波形資料庫 \(SDS\)，進行測試。

* 進入 WOR/TVO

* Copy parameter file condet.par from DAT to WOR/TVO. Start by checking the CONDET input file ‘condet.par’, use SEISAN manual for explanation. Parameters to change in the exercise are the detection algorithm, the respective detection parameters, the filters and the network detection settings.

* Now run the program by typing ‘condet’, it automatically uses condet.par as input file. The program runs one station after the other. The main output files are ‘condet.out’ listing all the trigger times, ‘extract.batch’ – a script file to extract the data using the program WAVETOOL, and ‘condet.trace’ which lists the data intervals that were read. Check all these files.



