# **Koikatsu Shader Fixer (戀活 Shader 修復工具)**

這是一個由Gemini生成，簡單但強大的 Python 工具，專門用於修復 **Koikatsu (戀活！)** 角色卡中因 Shader 名稱不一致導致的讀取錯誤。

主要解決在不同整合包環境（例如 Madevil 整合包與 HF Patch）之間轉移角色卡時，因 HarvexARC Shader 命名定義不同（/ 與 \- 的差異）而導致材質遺失或變為粉紅色的問題。

## **⚠️ 問題背景**

* **Madevil 環境**：通常使用 HarvexARC/XRay 作為 Shader 名稱。  
* **HF Patch / 標準環境**：通常識別 HarvexARC-XRay。  
* **結果**：當您讀取來自 Madevil 環境的存檔時，遊戲會報錯 Could not load shader: HarvexARC/XRay。

此工具會自動掃描並修正這個字串，讓卡片在標準環境下正常運作。

## **✨ 功能特點**

* **自動掃描**：自動偵測所在目錄下的所有 .png 角色卡。  
* **二進位替換**：直接修改檔案數據，不破壞圖片結構。  
* **安全備份**：修改前會自動產生 .bak 備份檔，防止數據丟失。  
* **智能過濾**：只處理包含錯誤 Shader 名稱的卡片，忽略正常的卡片。

## **📦 環境需求**

* Python 3.x  
* 必要函式庫：Pillow

## **🚀 安裝與使用**

### **方法一：使用 Python 直接運行**

1. 確保您已安裝 Python。  
2. 安裝依賴套件：
   
   ```
   pip install Pillow
   ```

4. 下載 fix\_shader.py。  
5. 將腳本放入您的角色卡資料夾中（例如：Koikatu\\UserData\\chara\\female）。  
6. 執行腳本：  
   * 雙擊 fix\_shader.py  
   * 或在終端機執行：python fix\_shader.py

### **方法二：使用 EXE 執行檔**

如果您沒有安裝 Python，可以下載 EXE 使用。

1. 將 Koikatsu\_Shader\_Fixer.exe 放入角色卡資料夾。  
2. 雙擊執行即可。
## **Roadmap**
**補齊剩下的Shader**
