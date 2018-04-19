# AUTOPIC

AUTOPICK 可以處理在SEISAN資料庫中之一個或多個地震事件。 該指令也可以在EEV環境中直接輸入'z'執行，或使用指令AUTO直接處理多個地震事件。

此指令之參數檔 AUTOPIC.INP，預設存放於DAT。 在AUTOPIC中，所有要使用的 station 和 channel 必須在參數文件中定義。

```
% This is the parameterfile needed by program: --- PREPROCESS ---
%
% The following rules apply:
% 1. All lines with % in the first column are comment lines
% 2. Lines with a blank in column 1 are read for fixed parameters.
% 3. All lines starting with "filter_x", where x is a number,
%    are read for filter variable parameters
% 4. All lines with * in the first column are read for stations to process
% 5. A breif explanation of all parameters is given in preprocess.inf
%
% FIXED PARAMETERS THAT ARE USED THROUGHOUT THE PROGRAM
% ----------------------------------------------------------------------
% Lwind Ishift Isigma Cohmin  Ndmin  Svelo  Nfilt   Crat   Lwin  Thres
%     !      !      !      !      !      !      !      !      !      !
% ----------------------------------------------------------------------
    4.0   30.0   06.0    0.1    3.0   2.75    4.0    1.6   30.0    3.0
%
%
% PARAMETERS THAT ARE FILTER DEPENDANT
% ----------------------------------------------------------------------
%Filter_nr    Window        F1        F2    Thrsh1    Thrsh2
%        !         !         !         !         !         !
% ----------------------------------------------------------------------
filter_1         0.8       2.0       4.0      2.30      3.0
filter_2         0.6       5.0      10.0      2.30      3.00
filter_3         0.4       8.0      16.0      2.30      3.00
filter_4         2.0       0.5       2.0      4.0       5.0
%
%
% STATIONS TO USE IN THE PROCESSING
% ----------------------------------------------------------------------
*SUE  S  Z 3 component
*BER  S  Z
*HYA  S  Z
*KMY  S  Z 3 component
*ODD1 S  Z 3 component
*BLS5 S  Z 3 component
```

執行步驟如下：

* cd WOR/TVO

* 複製 AUTOPIC.INP 至工作目錄，並修改所需參數。

* 執行 EEV 進入資料庫

* 使用EEV指令 'dels' 刪除資料庫中之已挑選之波相到時（亦可使用編輯器刪除），但必須確定保留所有標題行。

* 使用EEV指令 'z' ，所得到結果會直接儲存至S-files.

* 檢查波像到時。 所有挑選之波像會設定為 E for emergent.

* 進行地震定位。

* 針對波相到時好的 channel，執行 'am' 自動計算地震規模。



