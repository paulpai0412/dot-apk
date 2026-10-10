# dotdot Android 實機測試版

這個公開 repository **只用於發布 APK 與安裝說明**，不是原始碼 repository。程式碼仍保留在 private repo；不發布登入憑證、私人資料或歷史測試證據。

## 下載

- [下載 dotdot 0.2.0 APK](https://github.com/paulpai0412/dot-apk/releases/download/v0.2.0-test-eeebff4/dotdot-0.2.0-eeebff4.apk)
- [版本說明與 SHA-256](https://github.com/paulpai0412/dot-apk/releases/tag/v0.2.0-test-eeebff4)

## 安裝

1. 在 Android 手機下載 APK；依系統提示允許目前瀏覽器／檔案管理員安裝未知來源應用。
2. 安裝並開啟 dotdot，使用自己的 ChatGPT 帳號登入。
3. 需要語音時，再允許麥克風與通知權限。

此版本是個人測試 client，綁定既定 Dot／環境；不是任意 ChatGPT 帳號都能使用的通用 App。下載 APK 不會取得任何帳號或 Page／Drive 的存取權。

**若手機已有另一份 dotdot，請先嘗試覆蓋安裝。若顯示簽章不相容或無法更新，請回報錯誤；不要為了安裝直接卸載舊版或清除資料，以免失去素材與未完成操作紀錄。**

## 建議第一輪實機測試

- 登入與取消登入是否正常。
- 外屏／內屏顯示、折疊切換與大字設定。
- 短語音的收音、播放、暫停與結束；使用此帳號已能存取的指定 Dot。
- 切前後台、鎖屏／解鎖後的行為，麥克風使用提示能否正常停止。

語音連線與操作可能消耗帳號資源，並留下雲端工作紀錄。初輪請不要用真正重要的資料測試寫入；若結果不明，保留畫面与紀錄，不連按重送。不要公開分享登入回呼 URL、token 或私人對話截圖。

## 本版範圍與核對

- 版本：`0.2.0`；package：`local.dot.context`；versionCode：`2`。
- Android 8.0／API 26 以上；包含 `arm64-v8a`，可供 vivo X Fold3 Pro 安裝測試。
- 程式版本：`eeebff431930c3636bc45732f756d11b69bf1db7`。
- 使用既有 release 簽章；已核對 APK Signature Scheme v2／v3 及 16 KB ZIP alignment。
- 已重新離線建置 release，所有非簽章 ZIP entries 與此已簽署 APK 的內容一致。
- 164 個 core tests 重新執行，失敗與錯誤均為 0。
- release 不含 debug fixtures／androidTest 素材；manifest 未啟用 debuggable，allowBackup 與 cleartext traffic 為 false。

這是 **prerelease 實機測試版**，不是完整 V1 交付；vivo 實體收音／播放與生命週期尚待使用者驗證。LLM Wiki、自動專案分類與 backlinks 尚未實作。
