# Install SEISAN 11.0 in CENTOS 7.5 \(64 bit\)\(2018-05-15\)

linux \([http://seis.geus.net/software/seisan/node18.html](http://seis.geus.net/software/seisan/node18.html)\)

1.下載 seisan v11 壓縮檔

並在家目錄中建立 **seismo** 的資料夾，將 **seisan\_11**_\*\*\_**\_**linux64.tar.gz** 在 **seismo\*\* 目錄中解壓縮。

```
tar xzvf *.tar.gz
```

即完成安裝。

2. 設定環境參數

2.1 編輯**COM/SEISAN.bash**

```
SEISARCH="linux64"
export SEISAN_TOP="$HOME/seismo
```

2.2 .修改**~/.profile**

新增到下列一行到 ~/.profile這個檔案

\(CentOS/Fedora則新增至~/.bash\_profile\)

```
source $PATH/COM/SEISAN.bash
```

然後執行

```
source ~/.profile
(source ~/.bash_profile in CentOS/Fedora)
```

3. 重新產生 IASP travel time table，依下面步驟執行。

```
da
remodl
setbrn
```



