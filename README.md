# DesignLens
DesignLens 是針對室內裝潢「風格」的一項深度學習專案。    
我們透過 "幸福空間" 這一華人最大的整合裝潢建議網站來蒐集資料並達成了兩項任務。    
在 Task1 當中，我們參考了 Kim等人提出了論文。我們使用預訓練的 VGG16 作為室內設計風格的分類模型。藉由透過蒐集的資料來推薦使用者尋找適合的設計師。    
而在 Task2 當中，我們使用了相片與資料的多模汰模型。透過單獨的MLP處理，我們可以捕捉不同類型的數據特徵來減少模型複雜度與增加更高的可預測性。    

## Task1
我們把整體的任務切分成兩個部分，分別是使用CNN模型對風格分類，第二部分是使用孿生網路來尋找最接近的圖片，最後推薦該圖片的設計工作室。    
![Task1_Model](https://github.com/RLungWu/DesignLens/blob/main/img/Task1_Model.png)    
整體的模型架構如上圖。

### 執行結果
![Task1_Processing](https://github.com/RLungWu/DesignLens/blob/main/img/Task1_processing.png)
輸入：一張裝潢圖片
輸出：推薦的設計公司



## Task2
我們透過案件相關的資訊與裝潢圖片，分別處理並提取案件與圖片特徵，設計適合此任務的多模態模型架構，進行裝潢費用預測。
![Task2_Model](https://github.com/RLungWu/DesignLens/blob/main/img/Task2_Model.png)
### 執行輸入與輸出
輸入：一張圖片與案件資訊(包含：設計風格、房屋類型、房屋坪數、房屋狀況與空間格局)     
輸出：預測裝潢金額    


## 如何運行程式
由於兩個 Task 都是由 .ipynb 檔案所撰寫，因此使用者可以直接執行整份專案。我們強烈建議把檔案放到 Google Colab 當中執行。    
使用者只需要更改自己的檔案連結，即可以訓練出自己的模型。



