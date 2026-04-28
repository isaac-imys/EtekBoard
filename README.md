ETEK Control Board (Arduino-Compatible Board Package)
這個 repository 提供 ETEK 系列控制板 在 Arduino IDE 中的 Boards Manager 定義套件。
使用者只要加入本套件的 JSON URL，即可在 Arduino IDE 內安裝並使用 ETEK 相關控制板。

📌 內容說明
本 repo 包含：

Boards Manager 描述檔

package_EtekBoard_index.json
ETEK 控制板套件 ZIP

EtekBoard-2.x.x.zip
可供 Arduino IDE 透過 Boards Manager 安裝
目前版本已支援 ETEK 系列控制板，並提供核心設定、腳位定義、編譯環境、範例架構等。

🚀 安裝方式（Arduino IDE）
1. 在 Arduino IDE 加入 Boards Manager URL
打開 Arduino IDE → File → Preferences
找到 Additional Boards Manager URLs 並加入：

https://raw.githubusercontent.com/firmament79/ETEK/main/package_EtekBoard_index.json

若已有其他網址，可用逗號分隔。

2. 安裝 ETEK Control Board 套件
開啟 Tools → Board → Boards Manager
搜尋 ETEK 或 EtekBoard
點選 Install 安裝
完成後，ETEK 系列控制板即可在 Board 選單中選擇使用。

🧩 選擇你的控制板
安裝完成後，可在以下路徑找到相關選項：

Tools → Board → ETEK Boards → (選擇你的板子)

若你正在開發自訂板卡，需要修改核心檔、pins_arduino.h、variant 等設定，也可以直接解壓 ZIP 檔進行客製化。

🛠 範例程式（建議放在後續更新）
你可以新增一些 ETEK 控制板專用示範程式，例如：

基本 IO 控制
雙手啟動流程
真空吸附 + 壓合動作流程
LoadCell 荷重元讀取
多汽缸流程控制範例
未來若你放入 examples/ 資料夾，本 README 也會自動引導。

🔗 與 ChatGPT / Codex 搭配使用（可選）
若你使用 ChatGPT 建立控制板程式碼助手，可將此 repo 連結到 GitHub Connector：

ChatGPT 設定 → Connected Apps → GitHub
授權 repo：firmament79/ETEK
在自訂 GPT 中勾選使用 GitHub 作為知識來源
這樣助手就能讀取此 repo 的板卡定義，自動產生能直接編譯的 ETEK 控制板程式碼。

📦 檔案結構
ETEK/ ├─ package_EtekBoard_index.json # Boards Manager 主描述檔 ├─ EtekBoard-2.1.8.zip # 套件版本 2.1.8 ├─ EtekBoard-2.1.9.zip # 套件版本 2.1.9 (示例) └─ ...（未來版本）

🧾 更新方式（給開發者）
若需更新板卡套件版本：

修改 / 解壓 ZIP → 調整核心、variant、pins
重新壓縮為： EtekBoard-x.y.z.zip
更新 package_EtekBoard_index.json 中：
version
url
archiveFileName
size（可用 zip 檔案大小）
checksum（可用 SHA-256）
Commit & Push
使用者就能在 Arduino IDE 的 Boards Manager 裡更新到最新版。
📮 聯絡方式 / Issues
如有控制板功能建議、BUG 回報或需要範例程式，可在 GitHub 建立 Issue。

歡迎一同改善 ETEK 控制板的開發體驗！

© 2025 ETEK Control Board
