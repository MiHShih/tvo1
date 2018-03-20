# 震源機制解\(Fault plane solution\)

SEISAN有四種不同計算方法找出斷層面解。

下面介紹用測站的P波波相之初動方向，來確定震源機制解。可選用的方法有FOCMEC和FPFIT兩種。

首先必須確定測站在Z channel上的初動方向（如3.4.3.3\)，若波形之上下動不清楚，可以放大波形震幅確定初動方向（如3.2.2）。

在下面的圖例中，ASK 測站的 Z channel，放大時間視窗與震幅後，可以明確地判別出初動方向。

![](/assets/seisan-tutorial-045.png)

For this event it should be between 10 and 25 km. If not ok, the depth should be fixed in the S-file by putting an ‘F’ in column 44 on header line.  
 First the FPFIT program is used. It will automatically find a solution in a least squares sense. It does not mean it is correct solution but the best with the available data. Use command ‘fp’.

在解算震源機制解前，必須先確定其震源深度不為 0 或 負值。如範例之震源深度應在 10 - 25 km之間。若可確認深度，可以在 S-file 的 header 的第 44個欄位，加上’Ｆ‘固定其震源深度進行解算。首先，用FPFIT以最小平方法的概念求取震源機制解，。其解不代表正確震源機制，但為現有資料所能求得之最佳解。

在eev環境中執行'fp'。

![](/assets/seisan-tutorial-046.png)

在上圖中，找到了多個解並將第一個解存進S文件中。

下面是儲存在S-file中的一部分。

![](/assets/seisan-tutorial-047.png)

現在可以再eev中用指令'fo'。

可得到下圖，圖中可以看出得到的解，但也可以看到還有其他得可能性存在。

![](/assets/seisan-tutorial-048.png)

It is possible to see which stations belong to which polarities, give command ‘f’.

![](/assets/seisan-tutorial-049.png)

and the following plot comes up showing stations and polarities.

![](/assets/seisan-tutorial-050.png)We will now try the FOCMEC program. This program will not automatically find a solution but show all the solutions possible within some given criteria. FOCMEC can also work with amplitude ratios but here only polarities will be used. Start with command ‘f’.

![](/assets/seisan-tutorial-051.png)

and this follows

![](/assets/seisan-tutorial-052.png)

The search is limited to a requirement that all polarities are ok, however, often there are no solutions without allowing some bad polarities. The search is in a 5 deg grid, allowing a finer grid will find more solutions and a courser grid fewer.  
 The solutions found are seen below. It is seen that the majority of the solutions are similar to the FPFIT solution. However searching with a smaller grid size will give hundreds of solutions so obviously the fault plane solution is not very constrained.

![](/assets/seisan-tutorial-053.png)

One of the solutions can be selected by moving the cursor to the corresponding P or T and pressing ‘p’ or ‘t’. The solution should then be saved:

![](/assets/seisan-tutorial-054.png)

and there are now 2 fault plane solutions in S-file, indicated by the F-lines:

![](/assets/seisan-tutorial-055.png)

The 2 solutions can be plotted with command ‘fo’ as before and we get:

![](/assets/seisan-tutorial-056.png)

It is seen that the two solutions are similar but FOCMEC also had very different solutions. It is always useful to compare solutions from different programs.  
 Doing the exercise yourself might result in quite different solutions since some polarities are uncertain.

