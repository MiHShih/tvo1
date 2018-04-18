SEISAN.DEF 中定義了SEISAN中使用的環境參數。 請注意，參數必須與'Par 1'和'Par 2'標記對齊，因為Fortran讀取該文件，是讀取固定格式。

SEISAN.DEF中有幾個參數必須依照不同需求與資料庫修改。

需要修改的參數是：

_**WAVEFORM\_BASE **_: 資料庫名稱，本手冊使用 _**TVE 。**_

_**ARC\_ARCHIVE **_: SDS 之檔案位置  

_**ARC\_CHAN**_ : 定義使用測站與channel

_**COPY\_WAVE DIR **_: 資料庫的名稱，供註冊地震事件時使用，本手冊使用 _**TVE**_。

_**MERGE\_WAVEFORM **_: 用於在註冊地震事件時，命名所使用的network名稱。

_**MAP\_LAT\_BORDER , MAP\_LON\_BORDER**_: 在 EEV 中的 MAP指令 使用，繪製當前地震周圍的地圖。 這兩個參數決定從震央到地圖邊緣的距離。

_**EPIMAP\_STATIONS**_: 決定是否繪製測站，‘Ａ’將會畫出測站。

_**EPIMAP\_MAP\_FILE**_: 地圖名稱。



Example 1

```

KEYWORD............Comments.............Par 1.....Par 2
WAVEFORM_BASE      Waveform base name   BAYAN
#
#   seisan cont dat abase
#
CONT_BASE          REA continuous base  RUND
CONT_BEFORE        start min before     20.
CONT_AFTER         start min after      1.
#
# position in file name where year yyyy and month mm starts
#
CONT_YEAR_MONTH_POSTION_FILE
#
# archive
#

# TVO
ARC_CHAN                                YM01 HHETW
ARC_CHAN                                YM01 HHNTW
ARC_CHAN                                YM01 HHZTW

ARC_ARCHIVE                             /Users/shih/archive

```



