MULPLT.DEF lists parameters used in the MULPLT program. Note that the parameters must be aligned with the ‘Par 1’ and ‘Par 2’ markers since the file is read by Fortran, which reads a fixed format statement. None of these parameters need to be modified, although it is usually convenient to modify some of the ‘FILTER X’ settings to frequencies useful in band-passing data for spectral analysis, particle motion and magnitude determination. There are some suggested filter settings in the MULPLT.DEF example listed below.

定義mulplt程序中所使用的參數。 請注意，參數必須與'Par 1'和'Par 2'標記對齊，因為Fortran讀取該文件，讀取固定格式。

通常這些參數都不需要修改，儘管通是將一些“FILTER X”設置修改參數，以利於 spectral analysis，particle  montion和magnitude determination。

下面列出的MULPLT.DEF示例中有一些建議的過濾器設置。

![](/assets/Screen Shot 2018-04-18 at 4.55.28 PM.png)

DEFAULT CHANNELS 可在特定目的時，選擇並需要的channels 顯示在mulplt的畫面中，以利於作業。若沒有設定DEFAULT CHANNELS 則會將資料庫中所有channels列出。

