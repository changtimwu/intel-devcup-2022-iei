# Install JupyterLab and OpenVINO Notebooks
Intel OpenVINO 官方範例, 以 jupyter notebook 形式呈現, 含括多種應用

## 安裝步驟
*  Install Python, Git and all essential tools
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python3-venv build-essential python3-dev git-all
```
* Install OpenCL drivers
skip this step if you have done [GPU configuration for OpenVINO](https://github.com/changtimwu/intel-devcup-2022-iei/blob/main/openvino_setup.md#%E8%A8%AD%E5%AE%9A-gpu-configuration)
```
sudo apt-get install intel-opencl-icd
```

* Create a Virtual Environment
```
python3 -m venv openvino_env
```
* Activate the Environment
```
source openvino_env/bin/activate
```
* Clone the Repository
```
git clone --depth=1 https://github.com/openvinotoolkit/openvino_notebooks.git
cd openvino_notebooks
```
* Install all packages 
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## 完整過程影片
* 

## 參考資料
* https://github.com/openvinotoolkit/openvino_notebooks/wiki/Ubuntu
