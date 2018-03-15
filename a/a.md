# 擷取事件波形資料

看到有訊號的波形，並需要擷取放進資料庫時, 首先選擇一個適當時間長度的視窗, 然後選擇 "Regis" 按鈕或'p' 將此筆資料註冊進資料庫。這一個動作會為該波型訊號，建立一個 S-file, 放在 /REA 目錄中, 並將波形檔放在 /WAV 目錄中。

操作過程如下：

原始瀏覽波形視窗![](/assets/Screen Shot 2018-03-15 at 3.37.13 PM.png)

選擇適當時間長度之波形資料

![](/assets/Screen Shot 2018-03-15 at 3.41.53 PM.png)

按下Regis 或 直接按 'p'，進入下列對話畫面：

```
 ENTER EVENT TYPE L,R OR D                         <== 註冊地震類別，L:local R:regional D:distance
 Second. optional character for event ID (e.g. E)
 Third optional character for model ID (e.g. J) lv <== 輸入lv，進入火山地區地震類型選單。

 Current volcano sub-classes:
 ---------------------------------------
 Number Sub-Class Description
 ---------------------------------------
     1 vt        volcano-tectonic
     2 hybrid    hybrid
     3 lp        long-period
     4 tremor    volcanic tremor
     5 rf        rockfall
     6 un        unknown
     7           QUIT
 ---------------------------------------
 Please enter number for sub-class :
 (Negative number to add to sub-class)
1                                                   <== 選擇地震類型 vt
 Sub-class vt     selected.
  Give operator code (max 4 char)
mh                                                  <== 輸入操作者名稱

  Give 2-5 letter data base, ,, for local dir, return for default base
TVE
 Output channels on screen: s
 No output, just register:  n
 No output, just ARC line:  a
 Output all channels:   enter

wavetool -start 20141003104126 -arc  -duration       17.1 -wav_out_file SEISAN -chansel extract.inp -cbase cbase.inp
Number of archive channels defined          42
Total duration:   17.0100021

                   42114 276 10 3 10 41 26.000 17.010
                   
YC03HH E    0.00    17.01 YC03HH N    0.00    17.01 YC03HH Z    0.00    17.01
YC05HH E    0.00    17.01 YC05HH N    0.00    17.01 YC05HH Z    0.00    17.01
YC11HH E    0.00    17.01 YC11HH N    0.00    17.01 YC11HH Z    0.00    17.01
YC12HH E    0.00    17.01 YC12HH N    0.00    17.01 YC12HH Z    0.00    17.01
YL05HH E    0.00    17.01 YL05HH N    0.00    17.01 YL05HH Z    0.00    17.01
YM01HH E    0.00    17.01 YM01HH N    0.00    17.01 YM01HH Z    0.00    17.01
YC03 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4
YC03 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4
YC03 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4
YC05 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4
YC05 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4
YC05 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4
YC11 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4
YC11 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4
YC11 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4
YC12 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4
YC12 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4
YC12 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4
YL05 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4
YL05 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4
YL05 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4
YM01 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4
YM01 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4
YM01 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4
YM06 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4
YM06 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4
YM06 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

```



```
                            42114 276 10  3 10 41 26.000    17.010
```

YC03HH E    0.00    17.01 YC03HH N    0.00    17.01 YC03HH Z    0.00    17.01

YC05HH E    0.00    17.01 YC05HH N    0.00    17.01 YC05HH Z    0.00    17.01

YC11HH E    0.00    17.01 YC11HH N    0.00    17.01 YC11HH Z    0.00    17.01

YC12HH E    0.00    17.01 YC12HH N    0.00    17.01 YC12HH Z    0.00    17.01

YL05HH E    0.00    17.01 YL05HH N    0.00    17.01 YL05HH Z    0.00    17.01

YM01HH E    0.00    17.01 YM01HH N    0.00    17.01 YM01HH Z    0.00    17.01

YC03 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YC03 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YC03 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YC05 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YC05 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YC05 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YC11 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YC11 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YC11 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YC12 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YC12 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YC12 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YL05 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YL05 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YL05 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YM01 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YM01 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YM01 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YM06 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YM06 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YM06 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YM08 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YM08 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YM08 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YM09 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YM09 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YM09 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YM11 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YM11 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YM11 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YM13 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YM13 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YM13 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YM14 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YM14 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YM14 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YM15 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YM15 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YM15 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

YM19 HH E114 276T10W 3 10 41 26.000  100.00   1701                          4

YM19 HH N114 276T10W 3 10 41 26.000  100.00   1701                          4

YM19 HH Z114 276T10W 3 10 41 26.000  100.00   1701                          4

Output waveform file name is 2014-10-03-1041-26S.NSN\_\_\_042

S-file name:   /Users/shih/seismo/REA/TVE\_\_/2014/10/03-1041-25L.S201410

GO AHEAD \(Y/N\)

y

cp   2014-10-03-1041-26S.NSN\_\_\_042 /Users/shih/seismo/WAV/2014-10-03-1041-26S.NSN\_\_\_042

File transferred to WAV \*\*\*\*\*\*\*\*\*\*

Continue plot\(y/n=default\)

y

