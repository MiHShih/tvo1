# 讀取SDS \(Seiscomp3 Data Structure\) 格式的連續紀錄。

開啟terminal，輸入 mulplt。

選取讀取波形資料來源，範例選取 arc 代表選取 SDS連續資料格式。

```
[~/seisan/WOR]$ mulplt
  Filename, number, filenr.lis (all)
  Continuous SEISAN data base: cont
  Large SEED volume: conts
  Archive: arc
  Make a choice
arc                                                    <== 選取波形來源
 Give start time, yyyymmddhhmmss
20141003100000                                         <== 選取檢視波形起始時間
 Interval in min
3                                                      <== 檢視波形之時間窗
  Number of archive channels with data:          42
  Number of archive channels with data:          42
```

![](/assets/309384ce-a471-4a22-be5b-6796c9ce1f6c.png)選取要檢視的測站。欲檢視所有測站，選取 a ,在選取 o。

![](/assets/754897c7-b51e-4492-80e7-2cf5ae479aa5.png)快速瀏覽波形。

```
  Plot options: Interactive picking          Return
                Multi trace plot on screen, def (0)
                Multi trace plot on screen      (1)
                Multi trace plot on screen+laser(2)
                Multi trace plot on laser       (3)
                Continuoues on screen           (4)
                Continuoues on screen + laser   (5)
                Continuoues on laser            (6)
                Stop                            (q)
0                                                      <== 檢視波形方法
  Low and high cut for filter, return for no filter
return                                                 <== 輸入濾波頻段
```

![](/assets/12300de6-d109-47ee-931b-373413db16b8.png)

讀取波形成功，可以開始作業了。

