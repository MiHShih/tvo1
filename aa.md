# 波相到時選取\(I\)

如下圖所示，以4個測站的Z channels為例。為了選擇 P-arrival，將滑鼠移動至P-arrival並按下'1'，P 標記隨即出現在圖上。此處用IP表示，其中'I'表示impulsive。同樣，將滑鼠油標移動到S-arrival並按下'8''，即出現S 標記。通常情況下，在水平方向 \(N and E \)上之channel 讀取S-arrival。

如下圖，是在 Z channel上挑選P-arrival的。

![](/assets/seisan-tutorial-017.png)

從下圖中可以看出，3個測站的P- 和 S- arrivals 以及1個測站（EGD）只讀取了P-arrival。

其結果會儲存於 S-file, 完成後用'q'退出視窗。



### 開始定位前，必須確認的項目：

* 選擇波相到時：

```
1 IP 
2 EP 
3 IPG 
4 EPG 
5 IPN 
6 EPN 
7 IS 
8 ES
9 ISG
0 ESG + ISN / ESN
```

* 振幅最大值
* 確認初動
* 決定weight \(Quality\)

The keys are defined as follows

```
Weight Linux Windows
 1       !     ! 
 2       @     " 
 3       #     # 
 4       $     $ 
 5       %     % 
 6       ^     & 
 7       &     / 
 8       *     ( 
 9       (     ) 
 0       )     =
```

* 確定尾波\(coda\)





開啟 S-file 檢查波相到時參數，可用't'列出S文件，如內容下圖：

![](/assets/Screen Shot 2018-03-13 at 3.45.25 PM.png)

