# 開啟事件波形

_**EEV**_通常每次檢視一個月中的所有事件，執行指令為

```
eev 199606 TEV       <== eev yearmonth 資料庫名稱
```

成功呼叫資料庫之後可得到

```
1996 6 Reading events from base TEST_ 2
# 1 3 Jun 1996 19:55 35 D 47.760 153.227 0.0 N 1.1 5.6WHRV 12 ?
```

第一行，顯示1996年6月有多少事件在資料庫中，上面範例中讀取2個events（最多可以顯示200 000筆資料），然後是發震時間，'D'代表distance earthquake，經度，緯度和深度，'N'代表一個新事件，rms of travel time residuals（1.1），規模5.6Mw。 12是指在S文件中有波向到時的測站數目。

下面例子中，要到第二筆資料，直接按enter即可。

```
1996 6 Reading events from base TEST_ 2
# 1 3 Jun 1996 19:55 35 D 47.760 153.227 0.0 N 1.1 5.6WHRV 12 ? 
# 2 25 Jun 1996 03:37 31 L 61.689 3.259 15.0 N 3.0 3.3LTES 35 ?
```

# 



