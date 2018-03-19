# 地震定位

### 開始定位前，必須確認的項目：

* ##### 選擇波相到時：

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

* ##### 振幅最大值
* ##### 確認初動
* ##### 決定weight \(Quality\)

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

* ##### 確定尾波\(coda\)

完成確認讀取波相到時等參數的工作後，執行EEV，選取要定位的地震事件。使用_** 'l' **_進行定位，可以得到下面訊息：

![](/assets/seisan-tutorial-016.png)確認定位結果後，執行'_**u'**_將結果更新至資料庫中。

資料更新過程訊息如下：

![](/assets/Screen Shot 2018-03-15 at 11.33.47 PM.png)![](/assets/Screen Shot 2018-03-15 at 11.34.04 PM.png)下面介紹，幾種方法幫助確認定位結果與波相到時的品質。

