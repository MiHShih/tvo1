# 建立資料庫

當您想使用 SEISAN 與自己的資料, 首先必須建立自己的**目錄結構，確定測站座標**以及**速度模型**。

建立資料庫可以使用 _**MAKEREA**_，完成後會在REA 和 WAV 目錄結構下新增目錄。

輸入**MAKEREA**指令後，要求輸入**資料庫名稱** \(必須是1-5 字母和大寫\), **開始時間** \(年和月份\), **結束時間** \(年和月份\) 和**創建的結構** \(REA 或 WAV\)。然後螢幕上會顯示建立的資料庫目錄名稱。

```
[~/SEISMO]$ makerea
  Give 1-5 letter base name, UPPER CASE
TET00
  Give start time, year month, e.g. 198302
201101
  Give end time, year month, e.g. 198303, blank for one month
201812
  Create REA or WAV structure or BOTH
BOTH
```



