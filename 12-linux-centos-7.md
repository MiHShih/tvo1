# Install SEISAN 10.4.1 in CENTOS 7.2 \(64 bit\)

1.編輯**COM/SEISAN.bash**

```
SEISARCH="linux64"
export SEISAN_TOP="$HOME/seismo
```

2.修改**~/.profile**

新增到下列一行到 ~/.profile這個檔案

\(CentOS/Fedora則新增至~/.bash\_profile\)

```
source /opt/SEISAN901/COM/SEISAN.bash
```

然後執行

```
source ~/.profile
(source ~/.bash_profile in CentOS/Fedora)
```

嘗試執行_** pr **_更換目錄至 **PRO**

3.修改**PRO/Makefile**

修改下列變數：

```
INSTALL_PRO_PATH = $HOME/seismo/PRO
xlink_gfortran = -lX11 -L/usr/include/X11
```

如果缺少**Xlib.h** 嘗試執行安裝

```
yum install libX11-devel
```

4.產生**libmseed.a**

```
cd $HOME/seismo/SUP
wget https://seiscode.iris.washington.edu/attachments/download/742/libmseed-2.17.tar.gz
tar zxvf libmseed-2.17.tar.gz -C ../LIB/libmseed sudo make
```

5.**DAT/SEISAN.DEF**修改下列變數：

```
WAVEFORM_DIRS      Waveform drectory    $SEISAN_TOP/WOR/seisnet
TEXT_PRINT               Unix example   lpr -Plp1
INIT_IMGMAP_FILE         PC example     $SEISAN_TOP/DAT/IMGWORLD.gif
IMGMAP_PATH              PC example     $SEISAN_TOP/DAT/IMGMAP
INTERNET_BROWSER         Unix example   /usr/bin/google-chrome
ACROBAT_READER           Unix example   /usr/bin/acroread
HELP_DIR                 PC   example   $SEISAN_TOP/INF
```

6.進行最後編譯

