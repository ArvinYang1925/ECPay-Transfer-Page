# ECPay-Transfer-Page

一個 **免編譯、單檔 HTML** 小工具，用來：

1. 手動貼上 **Bearer Token**
2. 輸入（或網址帶入）**Order ID**
3. 向後端 `POST /api/v1/orders/:id/checkout`
4. 取得後端產生的 HTML `<form>`，立即自動轉跳到綠界付款頁面

---

## 快速使用

| 步驟 | 說明                                                 |
| ---- | ---------------------------------------------------- |
| 1    | 下載或 `git clone` 此專案                            |
| 2    | 打開 `index.html`，若需要可修改 `window.BACKEND_URL` |
| 3    | 直接在瀏覽器開啟檔案（或用任何靜態伺服器）           |
| 4    | 貼上登入後取得的 **Bearer Token**                    |
| 5    | 輸入 **Order ID**，或在網址加 `?orderId=<uuid>`      |
| 6    | 按「**進行結帳**」→ 瀏覽器自動導向綠界               |

---

## 目錄結構

ECPay-Transfer-Page
└─ index.html # 主頁面，內含 Tailwind CDN

---

## 注意事項

- HashKey / HashIV 僅存在於後端，**前端不應曝光**
- 本頁面僅用於測試跳轉，金額與訂單驗證須由後端負責
- 正式環境請以 HTTPS 服務，並返回正式金流網址

MIT © Arvin Yang
