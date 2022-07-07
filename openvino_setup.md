# Install Openvino

## 安裝 Intel® Distribution of OpenVINO™ toolkit v.2022
```
wget https://apt.repos.intel.com/intel-gpg-keys/GPG-PUB-KEY-INTEL-SW-PRODUCTS.PUB 
```


## 設定 GPU configuration
在指定 inference engine 指定 device 為 GPU, 可獲得比 CPU 更高為了非
* 至下列目錄
```
cd /opt/intel/openvino 2022./install_dependencies/
```
* 安裝 driver
```
sudo -E ./install_NEO_OCL_driver.sh
``` 

## 安裝過程參考應片
*

## 參考資料
* [Install Intel® Distribution of OpenVINO™ Toolkit for Linux Using APT Repository](https://docs.openvino.ai/latest/openvino_docs_install_guides_installing_openvino_apt.html)
* [Configurations for Intel® Processor Graphics (GPU) with Intel® Distribution of OpenVINO™ toolkit](https://docs.openvino.ai/latest/openvino_docs_install_guides_configurations_for_intel_gpu.html)
