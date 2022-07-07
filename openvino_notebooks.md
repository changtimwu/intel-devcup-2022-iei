# Install JupyterLab and OpenVINO Notebooks

## 安裝步驟
* 安裝 Python, Git 所有基本工具與更新
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python3-venv build-essential python3-dev git-all
```
* 安裝 OpenCL drivers
此步驟可以省略, 如果你執行過 [GPU configuration for OpenVINO]([https://github.com/changtimwu/intel-devcup-2022-iei/blob/main/openvino_setup.md#%E8%A8%AD%E5%AE%9A-gpu-configuration](https://github.com/changtimwu/intel-devcup-2022-iei/blob/main/openvino_setup.md#gpu-configuration))
```
sudo apt-get install intel-opencl-icd
```

* 建立 Python Virtual Environment
名為 `openvino_env`
```
python3 -m venv openvino_env
```
* 進入此 Environment
進入後, 提示符號會變為 `(openvino_env)`
```
source openvino_env/bin/activate
```
* 取得 openvino notebooks 
```
git clone --depth=1 https://github.com/openvinotoolkit/openvino_notebooks.git
cd openvino_notebooks
```
* 安裝 openvino notebooks 所有相依套件
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## 啟動 jupyterlabs
* 進入 `openvino_env` virtualenv
```
source openvino_env/bin/activate
```
* 啟動 jupyterlab server
```
cd openvino_notebooks
jupyter lab notebooks
```
會看到如下訊息, 請將訊息中 token 記下來, 如下圖中的, token 為 `0fcdb4b589a7c73503684a94a28e243774f50e7c3ff61c9b` 
```
(openvino_env) devcon@drpctgl:~/openvino_notebooks$ jupyter lab notebooks 
[I 2022-07-06 18:15:49.826 ServerApp] jupyterlab | extension was successfully linked.
[I 2022-07-06 18:15:49.827 ServerApp] Writing Jupyter server cookie secret to /home/devcon/.local/share/jupyter/runtime/jupyter_cookie_secret
[I 2022-07-06 18:15:50.008 ServerApp] notebook_shim | extension was successfully linked.
[I 2022-07-06 18:15:50.028 ServerApp] notebook_shim | extension was successfully loaded.
[I 2022-07-06 18:15:50.029 LabApp] JupyterLab extension loaded from /home/devcon/openvino_env/lib/python3.8/site-packages/jupyterlab
[I 2022-07-06 18:15:50.029 LabApp] JupyterLab application directory is /home/devcon/openvino_env/share/jupyter/lab
[I 2022-07-06 18:15:50.032 ServerApp] jupyterlab | extension was successfully loaded.
[I 2022-07-06 18:15:50.033 ServerApp] Serving notebooks from local directory: /home/devcon/openvino_notebooks/notebooks
[I 2022-07-06 18:15:50.033 ServerApp] Jupyter Server 1.18.1 is running at:
[I 2022-07-06 18:15:50.033 ServerApp] http://localhost:8888/lab?token=0fcdb4b589a7c73503684a94a28e243774f50e7c3ff61c9b
[I 2022-07-06 18:15:50.033 ServerApp]  or http://127.0.0.1:8888/lab?token=0fcdb4b589a7c73503684a94a28e243774f50e7c3ff61c9b
[I 2022-07-06 18:15:50.033 ServerApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
```
若要希望能從遠端進入, 必須加上 `--ip=0.0.0.0` 啟動, 如下
```
jupyter lab notebooks --ip=0.0.0.0
```
* 開啟 browser 存取 jupyterlab
URL 需帶入剛剛紀錄下來的 token 
```
local :  http://localhost:8888/labs?token=<token>
remote : http://<edge box ip>:8888/labs?token=<token>
```
## 完整過程影片
* https://youtu.be/BrwXdjY_UO8

## 參考資料
* https://github.com/openvinotoolkit/openvino_notebooks/wiki/Ubuntu
