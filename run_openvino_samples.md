# OpenVINO 範例

## jupyterlab 基本環境簡介
進入 jupyterlab 後, 會看到左側有豐富 openvino notebooks 範例, 你可以選擇任一目錄進入後執行
<img width="1509" alt="image" src="https://user-images.githubusercontent.com/400410/177886119-3915667d-2315-496d-aa00-60957289d122.png">


## 基本範例巡覽
### [001-hello-world](https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/001-hello-world)
* 進入目錄後, 直接點選 `001-hello-world.pynb` 開啟
<img width="429" alt="image" src="https://user-images.githubusercontent.com/400410/177886601-f1422b5e-e20b-408b-92f5-9cc8a836eaf2.png">
* 你可以慢慢瀏覽,編修,執行整份 notebook 任一 cell, 這裡為了方便講解, 我們選擇執行整份 notebook 
<img width="1170" alt="image" src="https://user-images.githubusercontent.com/400410/177886765-d3921f85-df76-49c0-a57e-e5b036981138.png">
* 此範例使用 `MobileNet V3` 模型, 進行image classification, 可觀察到模型內正確推理出圖片內有 flat coated retriever 犬種
<img width="811" alt="截圖 2022-07-08 上午7 22 00" src="https://user-images.githubusercontent.com/400410/177887336-3bf414ad-7238-4482-bb81-43a3728be60c.png">


### [002-openvino-api](https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/002-openvino-api)
* 此範例示範如何列出系統可供 openvino 推理的底層硬體, 在本平台預期要能出現 CPU & iGPU, 如下圖
<img width="869" alt="image" src="https://user-images.githubusercontent.com/400410/177887744-66f31290-f21b-4f2f-a370-ac1356b1db72.png">
* 此範例也示範 GPU 的 model cache 的功能, 可以看到透過 model cache, 載入 model 進入 GPU 會快速許多, 不需要重新編譯
<img width="1049" alt="image" src="https://user-images.githubusercontent.com/400410/177887847-e8f26db1-a6c3-4067-a3d5-759b65b11b06.png">


### [004-hello-detection](https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/004-hello-detection)
* 此範例主要示範文字辨識, 善用 open model zoo 中的 `horizontal-text-detection-0001`, `text-recognition-resnet` 兩個模型, 達到將圖中的任意英文文字辨識, OpenVINO notebook 也提供了其他進階 OCR 範例, 如 (208-optical-character-recognition)[ https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/208-optical-character-recognition] 與 [405-paddle-ocr-webcam](https://github.com/openvinotoolkit/openvino_notebooks/tree/main/notebooks/405-paddle-ocr-webcam) 
<img width="868" alt="image" src="https://user-images.githubusercontent.com/400410/177887903-ae4b839a-ac44-494c-adf1-85f607cc5f1b.png">


## 實際執行影片
* https://youtu.be/zYXgvXCEBK8
