# 🎓 NSYSU TronClass Downloader (中山大學網路大學PDF下載器)

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

這是一個專為 **國立中山大學網路大學 (TronClass)** 設計的 Python 自動化下載腳本。透過模擬完整的 SSO 單一登入流程，全自動解析動態網址並下載課程教材，讓學生能更有效率地獲取與整理學習資源。

## ✨ Features (核心技術與特色)

*   **SSO 登入突破**：自動解析網頁 DOM Tree，抓取動態 `session_code` 與 `execution` 參數，無縫通過學校認證中心。
*   **狀態保持 (Session Management)**：利用 `requests.Session` 自動管理 Cookie，只需登入一次即可持續保持連線狀態。
*   **動態 API 解析**：透過逆向工程分析 TronClass 後台 API 邏輯，自動提取真實檔案下載金鑰。
*   **資安防護 (Secure Input)**：採用終端機互動式讀取帳號密碼，確保密碼零外洩風險。

## 🛠️ Prerequisites (環境要求)

請確保您的電腦已安裝 Python 3.x。本專案依賴以下第三方套件：
*   `requests`
*   `beautifulsoup4`

## 🚀 Installation (安裝步驟)

**【步驟 1】將此專案 Clone 到本機**
```bash
git clone [https://github.com/charlesjian95-source/Tronclass.git](https://github.com/charlesjian95-source/Tronclass.git)
```

**【步驟 2】進入專案資料夾**
```bash
cd Tronclass
```

**【步驟 3】安裝所需套件**
```bash
pip install -r requirements.txt
```

## 💻 Usage (使用教學)

**啟動程式**
```bash
python Downloader.py
```

程式啟動後，請依序在終端機輸入以下資訊：
*   **學號**：例如 `B12345678`
*   **密碼**：您的 TronClass 單一登入密碼
*   **檔案網址**：貼上該章節的 learning-activity 網址 
> 範例網址：https://elearn.nsysu.edu.tw/course/12345/learning-activity#/67890

腳本執行完畢後，PDF 教材將會自動儲存於當前的資料夾目錄下。

## ⚠️ Disclaimer (免責聲明)

1. 本專案僅供程式語言學習、網路架構研究與學術交流使用。
2. 請勿將此腳本用於大量惡意爬取，以免對校方伺服器造成負擔。
3. 下載之課程教材版權均歸原作者及授課教授所有，請遵守智慧財產權，切勿隨意散佈。