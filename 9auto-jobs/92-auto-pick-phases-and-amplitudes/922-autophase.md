# AUTOPHASE

AUTOPHASE 指令只能從EEV環境中執行，因此它只能是用於一個地震事件。 使用起來非常簡單，且不需要任何參數文件。因此，所有資料庫中之 station 與 channels 都會被使用。

AUTOPHASE 可同時選擇P和S phases，並且還會在清晰的P波上決定上下動。



* Select event 19960705, same as used for AUTOPICK.

* Delete already picked phases using the editor or the EEV command dels, make sure to keep all header lines.

* Give command ‘ap’ and phases should be picked and saved in S-file. There is no need to delete old phases since they are all deleted automatically.

* Plot event and inspect automatic picks, note that all picks are marked as I for impulsive. Also note that for some phases, polarity is picked.

* Locate event



