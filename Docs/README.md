# 資料讀取與紀錄系統

**這是一個基於QMH框架展示的程式，功能皆未進行實作。**
此系統基於 LabVIEW 的 QMH（Queued Message Handler）架構設計，實現設備通訊、資料讀取、顯示與紀錄的完整功能。

## 功能概述
- 與設備通訊，讀取約 335 個資料項目。
- 支援波形圖與數值面板兩種顯示模式。
- 提供連續紀錄與手動紀錄功能。
- 可將紀錄的資料存檔。

## 系統架構
系統由以下模組組成：
1. **通訊模組**
   - 與設備建立通訊並讀取資料。
2. **資料處理模組**
   - 將原始資料解析並格式化。
3. **檔案處理模組**
   - 負責建立檔案並進行資料紀錄與存檔。

## 使用說明
### 1. 啟動系統
- 開啟 Main.vi，執行程式。

### 2. 設定參數
- **通訊設定**：輸入設備的通訊參數（如 IP、Port 或 Baud Rate）。
- **顯示設定**：選擇顯示模式（波形圖或數值面板）。
- **紀錄設定**：
  - **連續紀錄**：設定每筆資料的間隔時間。
  - **手動紀錄**：設定每次按下按鈕時紀錄的筆數。

### 3. 開始紀錄
- 按下啟動按鈕，系統將開始讀取資料並進行顯示與紀錄。

### 4. 停止系統
- 按下停止按鈕，系統將停止所有操作並存檔。

## 系統需求
- LabVIEW 2020 或以上版本。
- 支援的通訊協定（如：RS232、TCP/IP）。

## 檔案結構
- **Main.vi**：主程式。
- **Modules**：模組資料夾，包含以下子模組：
  - **Comm Module.vi**：通訊模組。
  - **Data Processing Module.vi**：資料處理模組。
  - **File Handling Module.vi**：檔案處理模組。
- **UI.vi**：使用者介面。

## 注意事項
- 請確認設備通訊設定正確。
- 波形圖模式適用於動態資料觀察，數值面板適用於靜態資料檢視。
- 儲存的檔案格式為 CSV，便於後續分析。

## 聯絡方式
若有任何問題，請聯繫 [marco_yang@msn.com]。
