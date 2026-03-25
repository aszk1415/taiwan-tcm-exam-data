# Taiwan TCM National Licensing Exam Dataset / 臺灣中醫師國家考試資料集

This repository publishes the public `public/` export of the Taiwan TCM national licensing exam dataset.

## 中文版

這個專案公開的是 `public/` 目錄中的資料，內容包含臺灣中醫師國家考試的題目、圖片與答案。  
如果你只想查資料，直接打開 `public/index.json` 或對應的年度資料夾即可。

### 主要結構

- `public/index.json`：總索引
- `public/index.md`：可讀版總索引
- `public/<year>/<exam_code>/exam.json`：題目與選項
- `public/<year>/<exam_code>/assets.json`：題目圖片與選項圖片對照
- `public/<year>/<exam_code>/answers.json`：答案資料
- `public/<year>/<exam_code>/images/figures/`：題目圖片
- `public/<year>/<exam_code>/images/options/`：圖片選項

### 使用方式

1. 先看 `public/index.json` 找到要查的年度與考卷。
2. 讀 `public/<year>/<exam_code>/exam.json` 看題目內容。
3. 若題目有圖片，對照 `public/<year>/<exam_code>/assets.json` 與 `images/` 目錄。
4. 若要判分或比對答案，讀 `public/<year>/<exam_code>/answers.json`。

### 答案格式

- 單一答案用一元素陣列，例如 `['B']`
- 多個可接受答案用多元素陣列，例如 `['A', 'B', 'C', 'D']`
- 需要說明時可加 `note`

## English

This repository publishes the public `public/` export of the Taiwan TCM national licensing exam dataset.

### Layout

- `public/index.json`: master index
- `public/index.md`: human-readable index
- `public/<year>/<exam_code>/exam.json`: questions and options
- `public/<year>/<exam_code>/assets.json`: question-image and option-image references
- `public/<year>/<exam_code>/answers.json`: answer data
- `public/<year>/<exam_code>/images/figures/`: question figures
- `public/<year>/<exam_code>/images/options/`: image-based answer options

### How to use

1. Open `public/index.json` to find the year and exam you need.
2. Read `public/<year>/<exam_code>/exam.json` for the question text.
3. If an exam includes images, use `public/<year>/<exam_code>/assets.json` and the `images/` folders.
4. For grading or comparison, read `public/<year>/<exam_code>/answers.json`.

### Answer format

- A single correct answer is stored as a one-item array, such as `['B']`
- Multiple accepted answers are stored as an array, such as `['A', 'B', 'C', 'D']`
- Add `note` only when a human-readable explanation is needed
