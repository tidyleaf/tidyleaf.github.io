---
title: ChatGPT 對話匯出：存成 Markdown、PDF 的四種方法
description: ChatGPT 對話匯出怎麼做？ChatGPT 沒有「下載這段對話」的按鈕。這篇比較四種方法：設定裡的「匯出資料」備份全部對話紀錄、複製貼上、瀏覽器列印成 PDF，以及一鍵把整段對話存成 Markdown 或 PDF 的擴充功能，說明每種做法的步驟、優缺點、隱私與注意事項，以及手機上能怎麼做。
lang: zh-TW
---

# ChatGPT 對話匯出：存成 Markdown 或 PDF

ChatGPT 沒有「下載這段對話」的按鈕。想把對話紀錄匯出成檔案，有四種做法：設定裡的「匯出資料」會把所有對話打包寄到你的信箱（JSON 和 HTML，不是 Markdown）；單則回覆可以用複製按鈕；整頁可以用瀏覽器列印存成 PDF；想要一段完整對話直接變成乾淨的 `.md` 或 PDF 檔，就需要瀏覽器擴充功能。下面依序說明。

## 方法一：ChatGPT 內建的「匯出資料」（全部對話，適合備份）

1. 網頁版點左下角的頭像（手機 App 從選單裡的帳號進入），進入「設定」（Settings）。
2. 選「資料控管」（Data controls）→「匯出資料」（Export data）→ 確認匯出。
3. OpenAI 會寄一封信到你的帳號信箱，裡面有下載連結。通常幾分鐘到幾小時內會收到，對話多時會比較久。
4. 下載的 zip 檔裡有 `conversations.json`（所有對話的原始資料，對話很多時可能拆成幾個編號的 JSON 檔）和 `chat.html`（可以用瀏覽器打開的網頁）。

- **適合：** 完整備份整個帳號的對話紀錄。
- **不適合：** 只想要其中一段對話。它一次給你全部，`conversations.json` 是一層層的訊息節點，要寫程式才能轉成好讀的文字；`chat.html` 是一整頁長網頁，沒有 Markdown 格式。下載連結大約 24 小時後失效，過期就要重新申請匯出。ChatGPT Business 或 Enterprise 的工作區帳號可能沒有這個選項。

## 方法二：複製貼上（單則回覆）

每則 ChatGPT 回覆下方都有複製按鈕，貼到筆記軟體裡通常會保留 Markdown 格式（標題、清單、程式碼區塊）。

- **適合：** 只需要一兩則回答。
- **不適合：** 整段對話。要一則一則複製，還得自己標註哪句是你問的、哪句是 ChatGPT 答的。直接用滑鼠框選整頁再貼上，格式通常會亂掉。

## 方法三：瀏覽器列印成 PDF（不用安裝任何東西）

在對話頁面按 `Ctrl + P`（Mac 是 `Cmd + P`），目的地選「另存為 PDF」。

- **適合：** 臨時要一份 PDF，又不想裝東西。
- **注意：** ChatGPT 的網頁不是為列印設計的，側邊欄、按鈕可能一起印進去，長的程式碼可能被截斷或換頁切開。很長的對話要先捲到最上面，確認訊息都載入了再列印。印出來的效果每次不一定，送出前請先檢查。

## 方法四：用擴充功能一鍵匯出 Markdown 或 PDF

瀏覽器擴充功能可以在對話頁面加一個「匯出」按鈕，把整段對話寫成一個檔案。我們做的 **Tidyleaf AI Chat Exporter** 就是做這件事。先說明：Tidyleaf 就是我們，這是我們的產品。

免費功能，不用註冊帳號：

- 把目前開著的對話匯出成 **Markdown、純文字、JSON 或 PDF**，從頁面右側的 Export 按鈕或工具列的小視窗操作。
- 每則訊息都標上 **User** 或 **Assistant**，分得清誰說的。
- **程式碼區塊保留語言標籤和原本的縮排**；表格、清單、標題、引用和連結都轉成正確的 Markdown。
- **數學式保留 LaTeX 原始碼**（放在 `$` 和 `$$` 之間），可以直接貼進 Obsidian、Notion、Typora 或論文。
- 圖片和附件會變成連結，或 `[Attachment: 檔名]` 這樣的標記。
- 可以把整段對話複製成 Markdown，或把滑鼠移到單則訊息上按「Copy MD」。
- PDF 匯出會打開一個乾淨的列印頁面，在列印視窗選「另存為 PDF」即可，不會印到側邊欄和按鈕。
- 同一個擴充功能也能用在 **claude.ai 和 gemini.google.com**。

在 ChatGPT 上，它用你已經登入的身分，像 ChatGPT 自己的網頁一樣向網站要這段對話，所以拿到的是整段對話目前的分支，而不只是畫面上看得到的部分。沒有伺服器、不需要帳號、不追蹤；對話不會上傳到任何地方。唯一會送出去的只有 Pro 授權金鑰，用來向我們的付款服務商 Polar 確認是否有效。

**Tidyleaf Pro**（每年 24 美元或每月 3.99 美元，[購買 Pro](https://buy.polar.sh/polar_cl_pRlV10W256IBneP7Bu1WVfpK5ArTh7jMw2a863HOnbf)）另外提供：一次把所有 ChatGPT 或 Claude 對話批次匯出成 zip（每段對話一個 Markdown 檔）、Obsidian 格式（開頭帶 YAML 屬性：標題、來源網站、網站有提供時的模型、建立日期、網址、標籤）和可直接匯入 Notion 的格式。上面列的免費功能一直免費。

**Tidyleaf AI Chat Exporter 即將上架 Chrome 線上應用程式商店。** 上架前請先看 [tidyleaf.github.io](https://tidyleaf.github.io)。
<!-- TODO(store-link): 審核通過後，把上一行換成 Tidyleaf AI Chat Exporter 的 Chrome Web Store 連結。 -->

其他選擇：ChatGPT Exporter 等擴充功能，以及 Greasy Fork 上的使用者腳本（需要先裝 Tampermonkey 之類的腳本管理器），也能把 ChatGPT 對話匯出成 Markdown 或 PDF。不管用哪一個，都請先看它的隱私權政策，確認對話不會被上傳到開發者的伺服器。

## 該用哪一種？

| 你想要 | 建議做法 |
|---|---|
| 備份帳號裡所有對話 | 內建「匯出資料」 |
| 一兩則回答放進筆記 | 回覆下方的複製按鈕 |
| 臨時一份 PDF，不想裝東西 | 瀏覽器列印「另存為 PDF」 |
| 一整段對話存成 `.md` 或乾淨的 PDF | 匯出擴充功能 |
| 所有對話各自一個 Markdown 檔，或放進 Obsidian | 有批次匯出的擴充功能（Tidyleaf Pro 有） |

## 檢查匯出結果的四個重點

不論用哪種方法，重要的對話匯出後請檢查：

1. **程式碼區塊有沒有保留語言**，例如 `` ```python ``，編輯器才會正確上色。
2. **數學式是不是 LaTeX 原始碼。** 有些工具會把算好的公式存成一堆 Unicode 符號，之後無法編輯。
3. **有沒有標出發言者**，分得出哪句是你的提問。
4. **長對話是否完整。** 只讀畫面的工具，可能漏掉還沒載入的訊息。

## 常見問題

**ChatGPT 有官方的單一對話匯出功能嗎？**
沒有單一對話的檔案下載。官方做法是「匯出資料」，一次匯出全部對話。「分享」連結產生的是別人可以打開的網頁，不是你可以保存的檔案。

**ChatGPT 對話紀錄可以匯出成 PDF 嗎？**
可以。不裝東西的話，用瀏覽器列印「另存為 PDF」，但版面可能不整齊。用 Tidyleaf AI Chat Exporter 選 PDF，會先打開乾淨的列印頁面，再在列印視窗選「另存為 PDF」。

**匯出用的擴充功能會看到我的對話嗎？**
要存檔就一定要讀取對話，重點是它把對話送去哪裡。Tidyleaf AI Chat Exporter 在你的電腦上產生檔案，不會把對話送到任何地方；它只會連到 chatgpt.com、claude.ai、gemini.google.com 和檢查 Pro 金鑰用的 Polar。詳見[隱私權政策](../chat-exporter/privacy)（英文）。

**可以一次匯出所有 ChatGPT 對話嗎？**
可以。內建「匯出資料」會給你全部對話，但都在同一個 JSON 檔裡。想要每段對話各自一個 Markdown 檔，可以用 Tidyleaf Pro 的批次匯出，帳號對話多時需要幾分鐘，下載完成前請保持分頁開著。

**手機上可以匯出嗎？**
擴充功能只能在電腦版瀏覽器使用。手機上最簡單的是用回覆的複製按鈕；要完整備份，手機 App 和網頁版的設定裡都有「匯出資料」，匯出的是整個帳號的對話，包含在手機上聊的。

## 相關文章

- [ChatGPT 對話資料夾：整理聊天紀錄的方法](chatgpt-folders-zh-tw)
- [Netflix 雙語字幕：同時顯示兩種字幕](netflix-dual-subtitles-zh-tw)
- [Export a ChatGPT conversation to Markdown](export-chatgpt-conversation-markdown)（英文版）

*Tidyleaf 是獨立的瀏覽器擴充功能開發者，與 OpenAI 無任何關係，也未獲其背書或贊助。「ChatGPT」是 OpenAI 的商標，僅用於說明本擴充功能適用的網站。*
