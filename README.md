# PI Code Agent

本專案依據 [Pi Monorepo](https://github.com/badlogic/pi-mono) 介紹，建立 [PI Code Agent](https://shittycodingagent.ai/) 操作環境並實務測試。

Pi Code Agent 為一個整合型的 Command-Line interface Agent，可使用 Gemini、Claude、Codepilot、Codex 等 15 個大語言模型服務，並提供訂閱方案登入與 API 權杖登入。

+ Gemini 服務取得與登入參閱 [infra-gemini-cli](https://github.com/eastmoon/infra-gemini-cli) 專案
+ Claude 服務取得與登入參閱 [infra-claude-cli](https://github.com/eastmoon/infra-gemini-cli) 專案
+ Codepilot 服務取得與登入參閱 [infra-ghc-cli](https://github.com/eastmoon/infra-ghc-cli) 專案

## 指令

使用 Windows Subsystem for Linux ( WSL ) 模擬 Linux 環境，並確保於本機運行服務。

+ 啟動環境 ```wsl-env.bat```
+ 安裝程序 ```./install.sh```

安裝完畢後會因為缺乏環境路徑無法使用 Pi 介面，對此，僅可離開 WSL 後再次啟動 ```wsl-env.bat``` 進入環境，即可使用。

僅設計 WSL 環境，主要是若用大語言模型用戶方案登入，會有反向回呼驗證程序，這個驗證會跳轉網址到本地的特定連結埠，為確保驗證程序完成；原則上，使用 Docker 並且網路設定為 Host 應有相同的效果。
