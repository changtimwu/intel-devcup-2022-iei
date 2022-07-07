# Install OpenVINO for Ubuntu 20.04

## 安裝 Intel® Distribution of OpenVINO™ toolkit v.2022
* 取得並安裝 Intel 官方 GPG key
```
wget https://apt.repos.intel.com/intel-gpg-keys/GPG-PUB-KEY-INTEL-SW-PRODUCTS.PUB 
sudo apt-key add GPG-PUB-KEY-INTEL-SW-PRODUCTS.PUB
```
* 使用下列指令將 Intel APT repo 加入
```
echo "deb https://apt.repos.intel.com/openvino/2022 focal main" | sudo tee /etc/apt/sources.list.d/intel-openvino-2022.list
sudo apt update
```
* 列出所有 OpenVINO packages
```
apt-cache search openvino
```
* 安裝 OpenVINO 2022.1.0 版本
```
sudo apt install openvino-2022.1.0
```
* 檢查已經安裝的 OpenVINO package
```
apt list --installed | grep openvino
```
* 安裝最新版本 opencv
```
sudo apt install openvino-opencv
```

## 設定 GPU dconfiguration
* 至下列目錄
```
cd /opt/intel/openvino_2022/install_dependencies/
```
* 安裝 OpenCL driver
```
sudo -E ./install_NEO_OCL_driver.sh
``` 

## 安裝過程影片
* https://youtu.be/uxdKVyWNe4M

## 參考資料
* [Install Intel® Distribution of OpenVINO™ Toolkit for Linux Using APT Repository](https://docs.openvino.ai/latest/openvino_docs_install_guides_installing_openvino_apt.html)
* [Configurations for Intel® Processor Graphics (GPU) with Intel® Distribution of OpenVINO™ toolkit](https://docs.openvino.ai/latest/openvino_docs_install_guides_configurations_for_intel_gpu.html)
