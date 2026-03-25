# Public Dataset Layout

Each exam lives under `public/<year>/<exam_code>/`.

Files:

- `exam.json`: question text and options only.
- `assets.json`: image references keyed by question id.
- `answers.json`: compact public answer file. Use an array for every answer; a single correct answer is a one-item array.
- `images/figures/`: question-related figures.
- `images/options/`: image-based answer options.

Answer schema:

- [schemas/public_answers.schema.json](../../schemas/public_answers.schema.json)

Image references are stored as repo-relative paths so they can be used directly in GitHub or downstream tooling.
