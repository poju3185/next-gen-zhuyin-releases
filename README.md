# Next-Gen 注音

macOS 的注音輸入法，用本機的小模型依前後文選字，不連網。

## 下載

**[下載最新版（.pkg）](https://github.com/poju3185/next-gen-zhuyin-releases/releases/latest)**

需要 Apple Silicon 的 Mac、macOS 14 以上。

## 安裝

1. 先結束「系統設定」。
2. 打開 .pkg，照畫面安裝。
3. 跳出詢問時按「允許」。
4. 從選單列的輸入法選單切換到「Next-Gen 注音」。

沒出現的話：系統設定 → 鍵盤 → 輸入方式 → 編輯⋯ → ＋ → 繁體中文 → Next-Gen 注音。

## 使用

- 大千鍵盤，要打聲調：3 4 6 7 是 ˇ ˋ ˊ ˙，空白鍵是一聲。
- Enter 送出；空白鍵或 ↓ 開候選，1–9 選字。

## 隱私

不連網，打的字不會離開你的 Mac；紀錄檔只記處理時間，不記內容。

## 移除

在系統設定移除輸入方式，再刪掉 `~/Library/Input Methods/NextGenZhuyin.app`。

## 第三方授權

- 詞庫：[小麥注音](https://github.com/openvanilla/McBopomofo)（MIT）
- 推論：[ONNX Runtime](https://github.com/microsoft/onnxruntime)（MIT）
- 模型訓練語料：[PTT](https://huggingface.co/datasets/yuhuanstudio/PTT-pretrain-zhtw)、[OpenSubtitles](https://opus.nlpl.eu/)（[opensubtitles.org](http://www.opensubtitles.org/)）、[Dcard](https://huggingface.co/datasets/iddle/dcard_conversations)、[新聞](https://huggingface.co/datasets/liswei/news-collection-zhtw)、[網頁](https://huggingface.co/datasets/liswei/common-crawl-zhtw)、[台灣風格網頁](https://huggingface.co/datasets/agentlans/traditional-chinese)（ODC-By）、[維基百科](https://huggingface.co/datasets/liswei/wikipedia-zhtw-dedup)（CC BY-SA）

授權全文與出處在 app 的 `Contents/Resources/NOTICE.txt`。
