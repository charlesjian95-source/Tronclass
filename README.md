# 🎓 NSYSU TronClass 終極下載器

這是一個專為國立中山大學網路大學（TronClass）設計的 Python 自動化下載腳本。透過模擬完整的 SSO 單一登入流程，全自動解析動態網址並下載課程教材。

## ✨ 核心技術
* 運用 `requests.Session` 維持 Cookie 狀態與登入連線。
* 使用 `BeautifulSoup` 解析 DOM Tree，突破 SSO 動態防偽造登入機制。
* 透過逆向工程分析 TronClass API，自動提取真實下載 Token 與二進位檔案。

## 🛠️ 使用方式
1. 安裝所需套件：`pip install requests beautifulsoup4`
2. 執行腳本：`python Downloader.py`
3. 依序輸入學號、密碼與 TronClass 學習活動網址，即可自動下載 PDF 檔案至同目錄。
