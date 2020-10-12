# 使用GCP部署機器學習API
[![Yes](https://img.youtube.com/vi/3X2aWAy9xJw/0.jpg)](https://www.youtube.com/watch?v=3X2aWAy9xJw)

此範例使用鳶尾花朵資料集進行 `XGBoost` 分類器模型訓練。將模型儲存起來，並使用 Flask 建置 API 介面提供輸入值預測。最後並部署到 Google Cloud Platform。

## 今日學習目標
- 動手部署自己的機器學習 API 
    - 使用 GCP 免費雲端平台部署應用程式

## GCP 設定
### 建立一個虛擬機器
每個Google帳號都有免費一年300美金額度的試用，啟用後首先一開始點選 Compute Enging 並新增建立 VM 執行個體。

[點我](https://console.cloud.google.com/?hl=zh-TW)進入 GCP 控制台。

![](https://i.imgur.com/5BDeg41.png)

新建一個虛擬機需要注意以下幾個事情：

1. 主機區域 (通常主機離你越遠相對的費用就會比較便宜，相對的速度會比較慢)
2. 機器規格設定 (各位可以依據需求配置你的虛擬機)
3. 系統 (今天的範例使用 Ubuntu18.04 LTS)
4. 防火牆 (開啟 HTTP 流量，也就是 80 PORT 被允許存取)

![](https://i.imgur.com/2iyJT0z.png)
![](https://i.imgur.com/v7GKCf4.png)

### SSH 進入虛擬主機
邊教學使用 Google 瀏覽器開啟 SSH 進入虛擬機的方式，一方面也比較簡單，若你是長期使用的資深的玩家可以考慮利用金鑰的方式直接從本機電腦的終端機進行連線存取雲端伺服器的方式。

![](https://i.imgur.com/1Rl4haK.png)
![](https://i.imgur.com/9IQ3DpR.png)


### 安裝 Python
要在 Linux 環境中安裝 Python 3，請安裝相對應的套件。[python3](https://packages.debian.org/stable/python3)、[python3-dev](https://packages.debian.org/stable/python3-dev)、 [python3-venv](https://packages.debian.org/stable/python3-venv)。

```
sudo apt update
sudo apt install python3 python3-dev python3-venv build-essential
```

輸入以下指令安裝 Python 以及 PIP 管理工具。

```
wget https://bootstrap.pypa.io/get-pip.py
sudo python3 get-pip.py
```

## 執行 API
你可以直接 Fork 此[專案](https://github.com/1010code/Flask-API-example-with-ML-model-GCP)到你自己的 GitHub 帳號中，或是直接 clone 專案到你的 GCP 中。

```
git clone https://github.com/1010code/Flask-API-example-with-ML-model-GCP.git
cd Flask-API-example-with-ML-model-GCP
```

### 安裝必要套件
使用 `pip3` 指令安裝必要的套件。

```
pip3 install -r requirements.txt
```

### 執行
使用 `python3` 指令且在 `sudo` 環境下執行程式，即可監聽 80 PORT。

```
sudo python3 run.py
```

## 補充
大家在本機開發時執行 Python 程式應該都是使用 `python xxx.py` 的方式執行，但我們部署到雲端伺服器時如果使用此方法應該會發現當你關閉終端機時你的程式就會結束服務。因此在部署時候建議各位要使用 Gunicorn 將 API 背景執行。

> 下面是我之前拍攝的 GCP 系列影片，可以給各位參考哦！

- [[GCP教學-Python] #1 部署第一個Python Flask API程式](https://andy6804tw.github.io/2020/03/27/gcp-python-ep1/)
- [[GCP教學-Python] #2 將臨時外部IP改為靜態IP位置](https://andy6804tw.github.io/2020/03/28/gcp-python-ep2/)
- [[GCP教學-Python] #3 利用iptable轉發PORT號](https://andy6804tw.github.io/2020/03/29/gcp-python-ep3/)
- [[GCP教學-Python] #4 建立防火牆規則](https://andy6804tw.github.io/2020/03/31/gcp-python-ep4/)
- [[GCP教學-Python] #5 使用Gunicorn將API背景執行](https://andy6804tw.github.io/2020/04/10/gcp-gunicorn/)

本系列教學簡報 PDF & Code 都可以從我的 [GitHub](https://github.com/andy6804tw/2020-12th-ironman) 取得！