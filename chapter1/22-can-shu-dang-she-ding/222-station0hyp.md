STATION0.HYP 列出了定位程式HYP中使用的參數。 

參數檔中有數個的參數需要修改有關於：

* coda magnitude 的計算,

* 測站位置,

* 一維速度模型

* network code



#### **利用尾波計算規模**

所使用到到參數 **TEST\(7\), TEST\(8\) and TEST\(9\)**:

**MAG = TEST\(7\) +TEST\(8\) \* LOG\(T\) + TEST\(9\) \* DELTA **

where

**T** is the coda length in seconds,  
**DELTA** is the hypocentral distance in km.

The default SEISAN values for the coda magnitude parameters are those determined by Richter for Northern California.

          Default values: 7: 0.087, 

                                     8: 2.0,

                                     9: 0.0035 \(Lee, 1972\)

So default MAG = 0.087 +2.0 \* LOG\(T\) + 0.0035 \* DELTA

Values for these parameters are often different at volcanoes. 

Here, we use the coda magnitude parameters determined for Mt. St. Helens, or

  
                   RESET TEST\(07\)=-2.46

                   RESET TEST\(08\)=2.82

                   RESET TEST\(09\)=0.00



#### **測站位置：**

Follow the format of the examples in STATION0.HYP for station location.

依照範例中格式，將測站座標加入檔案中。  
 

#### 一維速度模型：

速度模型格式參照下方範例，範例為 Mt. St. Helens. 所使用的速度模型。 

![](/assets/Screen Shot 2018-04-18 at 4.44.17 PM.png)

'N' 代表 Moho 面深度。

#### S/P velocity ratio：

S/P velocity radio in the example below is given by the value 1.74 in the line:

_**33.0 1000.3300. 1.74 15 1.0 00.5**_ 



```
RSET TEST(02)=500.0
RESET TEST(07)=-3.0
RESET TEST(08)=2.6
RESET TEST(09)=0.001
RESET TEST(11)=99.0
RESET TEST(13)=5.0
RESET TEST(34)=1.5
RESET TEST(35)=2.5
RESET TEST(36)=0.0
RESET TEST(41)=20000.0
RESET TEST(43)=5.0
RESET TEST(51)=3.6
RESET TEST(50)=1.0
RESET TEST(56)= 1.0
RESET TEST(58)= 99990.0
RESET TEST(40)=0.0
RESET TEST(60)=0.0
RESET TEST(71)=1.0
RESET TEST(75)=1.0
RESET TEST(76)=0.910
RESET TEST(77)=0.00087
RESET TEST(78)=-1.67
RESET TEST(79)=1.0
RESET TEST(80)=3.0
RESET TEST(81)=1.0
RESET TEST(82)=1.0
RESET TEST(83)=1.0
RESET TEST(88)=1.0
RESET TEST(85)=0.1
RESET TEST(91)=0.1
```

```
  YM012322.72N12245.19E   9
  YN032756.73N123 6.22E  20
  YM0624 7.77N12556.76E 131
```

```
  3.79       1.0
  4.41       2.0
  4.88       3.0
  5.34       5.0
  5.66       7.0
  5.99       9.0
  6.34      17.0
  6.90      36.0
  7.80      80.0      B

15.0 1100.2200. 1.78
```



