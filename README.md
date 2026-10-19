# 台灣在地繁中提示詞庫｜tw-prompts

**台灣人每天用得到的 AI 提示詞，填空就能用。** 免費、可商用（CC0）。

🌐 線上版（搜尋＋填空複製）：https://prompts.penguindriver.com/

適用 ChatGPT、Claude、Gemini 等任何 AI 助理。

## 收錄內容

| 分類 | 內容 |
|---|---|
| 🛒 電商賣場 | 蝦皮標題、商品詳情頁、負評回覆、檔期企劃 |
| 📣 社群行銷 | IG 貼文、Threads 串文、短影音腳本、輪播圖卡 |
| 💬 LINE 客服 | 官方帳號歡迎訊息、自動回覆、客訴、推播 |
| 🏪 在地店家 | Google 商家簡介與評論回覆、菜單、排班、定價 |
| 💼 職場公文 | 會議紀錄、商務 Email、公文簽呈、簡報大綱 |
| 📝 求職履歷 | 104 自傳、成果量化、面試模擬、薪資談判 |
| ⚖️ 稅務法規 | 綜所稅準備、勞基法、加班費、租屋契約、消費糾紛 |
| 🧺 團購開團 | 開團文、團購規則、廠商詢價、訂單對帳 |
| 📚 學習教學 | 入門規劃、出題、教案、英文批改、讀書計畫 |
| 🏠 生活家庭 | 晚餐規劃、家庭記帳、旅遊行程、防詐騙檢查 |

共 100 則，每則都有【變數】填空和使用提示。

## 檔案

- `prompts.csv`：UTF-8（含 BOM，Excel 直接開），欄位 `id, category, title, prompt, tip`
- `prompts.json`：同內容，含分類資料與 `vars`（每則要填的變數）

## 在程式或 AI 工具裡使用

**API**
```
GET https://prompts.penguindriver.com/api/prompts?q=蝦皮&cat=ecom
GET https://prompts.penguindriver.com/api/prompts/ecom-01
```

**MCP 伺服器**（Claude、Cursor 等）
```
claude mcp add --transport http tw-prompts https://prompts.penguindriver.com/mcp
```
```json
{ "mcpServers": { "tw-prompts": { "url": "https://prompts.penguindriver.com/mcp" } } }
```
工具：`search_prompts`、`get_prompt`（可帶 `values` 直接填好變數）、`list_categories`

## 投稿與許願

想要哪一類台灣情境的提示詞，或想分享你的寫法：開 Issue，或寄信到 hot198271@gmail.com。收錄內容同樣以 CC0 釋出。

## 授權

提示詞內容以 [CC0 1.0 公有領域](https://creativecommons.org/publicdomain/zero/1.0/deed.zh-hant) 釋出：可以複製、修改、商用，不需要署名。

AI 產出的稅務、法律、健康資訊請以主管機關最新公告為準。

由 [企鵝司機 penguindriver](https://penguindriver.com/ig) 維護。
