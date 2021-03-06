# 斷層面解\(Fault plane solution\)

SEISAN有四種不同計算方法找出斷層面解。

下面介紹用測站的P波波相之初動方向，來確定斷層面解。可選用的方法有FOCMEC和FPFIT兩種。

首先必須確定測站在Z channel上的初動方向（如3.4.3.3\)，若波形之上下動不清楚，可以放大波形震幅確定初動方向（如3.2.2）。

在下面的圖例中，ASK 測站的 Z channel，放大時間視窗與震幅後，可以明確地判別出初動方向。

![](/assets/seisan-tutorial-045.png)

在求斷層面解前，必須先確定其震源深度不為 0 或 負值。如範例之震源深度應在 10 - 25 km之間。若可確認深度，可以在 S-file 的 header 的第 44個欄位，加上’Ｆ‘固定其震源深度進行解算。首先，用FPFIT以最小平方法的概念求取斷層面解。但其解並不代表其正確的斷層面解，但為現有資料所能求得之最佳解。

在eev環境中執行'fp'。

![](/assets/seisan-tutorial-046.png)

在上圖中，找到了多個解並將第一個解存進S文件中。

下面是儲存在S-file中的一部分。

![](/assets/seisan-tutorial-047.png)

現在可以再eev中用指令'fo'。

可得到下圖，圖中可以看出得到的解，但也可以看到還有其他得可能性存在。

![](/assets/seisan-tutorial-048.png)

如果要檢視震源機制球上個測站分佈與初動方向時，可以在eev下給指令'f'。再選擇 '-1'，畫圖時會將測站訊息加上，如下圖：

![](/assets/seisan-tutorial-049.png)

如下圖中顯示出測站與初動方向。

![](/assets/seisan-tutorial-050.png)接下來我們要用FOCMEC 求斷層面解，這個方法會列出所有可能的解，並不會自動給出最佳解。此一方法還可以利用P波跟S波震幅的比值來求解。但下列範例僅使用Ｐ波出動方向來求解。

在eev環境中下指令'f'。在選擇'4'，就會使用focmec求出斷層面解。

![](/assets/seisan-tutorial-051.png)

接下來，如下圖輸入參數。

![](/assets/seisan-tutorial-052.png)

在求解我們可以選擇接受異常初動方向的個數，以利於找尋合理的斷層面解。搜尋的角度也可以自由選擇，例如每五度計算一次，可以得到較精細數量較多的解，角度加大時計算速度較快，但得到的解就較為粗略。

得到的解如下圖所示。可以看出，大部分解決方案與FPFIT解決方案相似。然而，使用更小的角度進行搜索將顯示出數百個解。

![](/assets/seisan-tutorial-053.png)

將游標移至相應的P或T並按'p'或't'即可選擇保存該該解至S-file中。

![](/assets/seisan-tutorial-054.png)

在S-file中有2個斷層面解（行尾用F表示）：

![](/assets/seisan-tutorial-055.png)

兩個解可以用'fo'同時畫出來，結果如下圖所示：

![](/assets/seisan-tutorial-056.png)

圖中可以看出，這兩種方法求出來的斷層面解是相似的，但FOCMEC也存在非常不同的解。此一方法，方便比較不同程序所得到的斷層面解。  


