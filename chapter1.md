# 資料結構

整個 SEISAN 系統位於子目錄下的主目錄 **seismo** \(建議預設值，可以設定不同的名稱\)。

資料庫和相關主要參數檔包括以下內容:

```
REA: Earthquake readings and full epicenter solutions in a database 
WOR: The users work directory, initially empty
TMP: Temporal storage of files, initially empty
PRO: Programs, source code and executables
LIB: Libraries and subroutines
INC: Include files for programs and subroutines in PRO and LIB 
COM: Command procedures
DAT: Default and parameter files, e.g. station coordinates
WAV: Digital waveform data files
CAL: System calibration files
INF: Documentation and information
ISO: Macroseismic information
SUP: Supplementary files and programs
```

SEISAN 的資料目錄結構為樹狀, 用於快速訪問 **REA** 目錄中的每個檔案, 為一個簡單的資料庫顯示給使用者。

下圖顯示了 SEISAN 資料庫的樹狀結構。![](/assets/Screen Shot 2018-03-13 at 10.46.21 PM.png)再次說明，

_**REA 目錄包含波相到時和地震定位資料**_, 如震源、震源機制解等。

_**WAV 目錄包含波形資料**_。

_**WOR 目錄包含多個對應著不同計劃、目的的測站等參數檔所分別建立的子目錄。**_為實務上，工作時所使用的資料夾位置。

_**CAL 目錄包含所有測站的儀器參數檔。**_

**REA** 目錄有一個或多個子目錄, 對應于不同的資料庫 \(最大5個字元\), 為了簡單起見, 這裡假定只有資料庫 "AGA" 存在 \(參見下圖\)。為了快速搜尋和互動式工作, 地震事件在每年的目錄和每月的子目錄中儲存在單個檔案 \(**S-file**\) 中。當新資料輸入到資料庫中時, 它將作為單個事件檔存儲。但是, 一旦互動式工作完成後, 執行更新資料庫時，單個事件檔就會被加到檔案的最後面, 並且還會存儲在每月檔中。![](/assets/Screen Shot 2018-03-13 at 10.53.42 PM.png)

