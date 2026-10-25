# Next-Gen 注音

macOS 的注音輸入法。每打完一個音節，app 裡的小模型會看游標前的文字和整段注音，一次決定整段的字，
詞庫負責詞和候選。全部在你的 Mac 上執行，不連網。

## 下載

**[下載最新版（.pkg）](https://github.com/poju3185/next-gen-zhuyin-releases/releases/latest)**

- 需要 Apple Silicon（M1 以後）的 Mac，macOS 14 Sonoma 以上。
- 安裝檔經過 Apple 公證。只裝在你自己的帳號，不需要管理者密碼。

## 安裝

1. 打開下載的 `NextGenZhuyin-<版本>.pkg`，照畫面裝完。
2. 從選單列的輸入法選單切換到「Next-Gen 注音」。
3. 選單裡沒有的話：系統設定 → 鍵盤 → 文字輸入 → 輸入方式 → 編輯⋯ → 左下角「＋」→ 繁體中文 → 「Next-Gen 注音」→ 加入。

更新：下載新版的 .pkg 再裝一次。裝完如果還是舊版的行為，登出再登入一次。

## 怎麼打

- 大千（標準）鍵盤，要打聲調：3 4 6 7 是 ˇ ˋ ˊ ˙，空白鍵是一聲。
- 每打完一個音節，整段會重新判斷；Enter 送出。
- 沒有正在組的注音時，空白鍵或 ↓ 打開游標前那個字的候選：1–9 選字，Esc 關掉。選過的字不會再變。
- Shift＋標點鍵打全形標點，Shift＋字母打英文字母；Caps Lock 開著時直接打英文。

還沒有的功能：使用者詞和學習、省略聲調、按錯鍵的自動修正。

## 隱私

- 不連網：模型和詞庫都在 app 裡，打的字不會離開你的 Mac。
- 為了分辨同音字，會讀游標前同一段的最後 32 個字當前文，只在輸入法裡使用，不會存下來。
- 紀錄檔 `~/Library/Logs/NextGenZhuyin/ime.log` 只記每個按鍵的處理時間和組字區的長度，不記打了什麼字。

## 移除

1. 系統設定 → 鍵盤 → 文字輸入 → 輸入方式，把「Next-Gen 注音」移除。
2. 刪掉 `~/Library/Input Methods/NextGenZhuyin.app`（在 Finder 按 ⌘⇧G，輸入這個路徑）。

## 回報問題

請到這個 repo 的 [Issues](https://github.com/poju3185/next-gen-zhuyin-releases/issues)。這裡只放安裝檔，原始碼不公開。

## 第三方授權與資料來源

- 詞庫：[小麥注音（McBopomofo）](https://github.com/openvanilla/McBopomofo)的 data.txt，MIT License，Copyright (c) 2011-2026 Mengjuei Hsieh et al.
- 推論引擎：[ONNX Runtime](https://github.com/microsoft/onnxruntime) 1.30.0，MIT License，Copyright (c) Microsoft Corporation。
- 模型的訓練語料（授權依各資料集的標示）：
  - PTT：[yuhuanstudio/PTT-pretrain-zhtw](https://huggingface.co/datasets/yuhuanstudio/PTT-pretrain-zhtw)（標示 Apache-2.0）
  - 電影字幕：[OPUS OpenSubtitles](https://opus.nlpl.eu/) v2024 zh_TW，字幕來自 [opensubtitles.org](http://www.opensubtitles.org/)
    （P. Lison and J. Tiedemann, 2016, OpenSubtitles2016, LREC 2016）
  - Dcard：[iddle/dcard_conversations](https://huggingface.co/datasets/iddle/dcard_conversations)（標示 MIT）
  - 新聞：[liswei/news-collection-zhtw](https://huggingface.co/datasets/liswei/news-collection-zhtw)
  - 網頁：[liswei/common-crawl-zhtw](https://huggingface.co/datasets/liswei/common-crawl-zhtw)
  - 台灣風格網頁：[agentlans/traditional-chinese](https://huggingface.co/datasets/agentlans/traditional-chinese) 的 taiwan-style-quality（ODC-By）
  - 維基百科：[liswei/wikipedia-zhtw-dedup](https://huggingface.co/datasets/liswei/wikipedia-zhtw-dedup)（CC BY-SA）
  - 多音字讀音的標註用了 [g2pW](https://github.com/GitYCC/g2pW)（Apache-2.0）和小麥注音詞庫。

授權全文在 app 裡的 `Contents/Resources/`：`NOTICE.txt`、`McBopomofo/`、`onnxruntime/`。
