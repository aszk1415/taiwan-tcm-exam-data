# Taiwan TCM National Licensing Exam Dataset / 臺灣中醫師國家考試資料集

This repository contains structured data for Taiwan TCM national licensing examinations, including questions, figures, and answer keys.

## 中文版

這個專案整理了臺灣中醫師國家考試的結構化資料，包含題目、圖片與答案，方便查詢、分析、訓練與前端應用。

### 目錄結構

- `index.json`：總索引
- `index.md`：可讀版總索引
- `101/` 到 `115/`：依年份分類的考卷資料
- `<year>/<exam_code>/exam.json`：題目與選項
- `<year>/<exam_code>/assets.json`：題目圖片與圖片選項對照
- `<year>/<exam_code>/answers.json`：答案資料
- `<year>/<exam_code>/images/figures/`：題目圖片
- `<year>/<exam_code>/images/options/`：圖片選項

### 使用方式

1. 先看 `index.json` 找到年份與考卷代碼。
2. 讀 `<year>/<exam_code>/exam.json` 取得題目內容。
3. 若題目有圖片，對照 `<year>/<exam_code>/assets.json` 與 `images/` 目錄。
4. 若要判分或比對答案，讀 `<year>/<exam_code>/answers.json`。

### 答案格式

- 每題都使用 `answer` 陣列
- 單一答案範例：`["B"]`
- 多個可接受答案範例：`["A", "B", "C", "D"]`
- 需要補充時可用 `note`

### 字形正規化

- 本資料集統一使用「鉤藤」。國考原題中可見「鉤藤」與「鈎藤」兩種寫法；為便於檢索與資料一致性，本專案一律正規化為「鉤藤」。

## English

This repository provides structured data for Taiwan TCM national licensing examinations, including question text, figures, and answer keys.

### Layout

- `index.json`: master index
- `index.md`: human-readable index
- `101/` through `115/`: exams grouped by year
- `<year>/<exam_code>/exam.json`: questions and options
- `<year>/<exam_code>/assets.json`: figure and image-option references
- `<year>/<exam_code>/answers.json`: answer data
- `<year>/<exam_code>/images/figures/`: question figures
- `<year>/<exam_code>/images/options/`: image-based answer options

### How to use

1. Open `index.json` to find the year and exam code you need.
2. Read `<year>/<exam_code>/exam.json` for question content.
3. If the exam includes images, use `<year>/<exam_code>/assets.json` with the `images/` folders.
4. For grading or comparison, read `<year>/<exam_code>/answers.json`.

### Answer format

- Every question uses an `answer` array
- Single-answer example: `["B"]`
- Multi-accepted-answer example: `["A", "B", "C", "D"]`
- Use `note` only when a human-readable explanation is needed

### Normalization

- This dataset standardizes both `鉤藤` and `鈎藤` to `鉤藤` for consistency and easier search.
- The obvious misrendering `白光白` is corrected to `㿠白`.
