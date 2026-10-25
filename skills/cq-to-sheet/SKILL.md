---
name: cq-to-sheet
description: Convert Creative Question documents into Excel sheets using the CQ schema, faithful content cleanup, and PPT-safe math formatting. Use when extracting and formatting CQs from source documents into a workbook.
---

CQ Sheet Builder converts Creative Question files into Excel. Use CQ.txt only as extraction base; old headers there are deprecated. Use EQUATION_AND_LATEX_RULES.txt for math handling, except PPT unit-spacing below. Use CQ_5_ROW_EXAMPLE.xlsx as the 5-row layout reference. Use Content_Correction_Accuracy_Instructions.md for content cleanup accuracy.

Headers exactly: Question-Frame, Number, Question, Image-Holder, Question-Image, Topic-Pill, Topic, Board-Pill, Board, Question 1, Question_1, Question 2, Question_2, Question 3, Question_3, Question 4, Question_4.

Extract only valid CQs: number, passage before ক, then ক, খ, গ, and optional ঘ. Ignore MCQ, answers, solutions, explanations, headings, page numbers, and unrelated content. Preserve source order, wording, and structure. Do not invent passages, subquestions, board names, topics, images, equations, values, formulas, labels, captions, references, examples, explanations, dates, or missing academic content.

Correct source content conservatively. Fix only clear, strongly supported OCR, spelling, punctuation, spacing, numbering, label, formula, unit, symbol, subscript/superscript, Bangla/English typo, broken-word, grammar, chemistry, physics, biology, terminology, and LaTeX errors. Preserve meaning, style, order, difficulty, and level of detail. Do not paraphrase clean text, modernize valid wording, simplify, expand, remove ideas, change tone, or alter facts, values, units, dates, names, variables, or formulas by assumption. Correct only when the intended fix is clear from source, nearby context, repeated context, or standard subject knowledge. If doubtful or partly unreadable, keep the safest faithful version, mark affected cells when appropriate, and report doubts unless the user explicitly requires file-only output. In file-only workflows, place necessary doubts inside the workbook only when safe for import.

For Bangla, preserve original wording; fix only clear OCR/spelling/punctuation/spacing corruption; keep Bangla outside math; do not merge/split lines or sentences unless clearly required; do not replace valid literary, regional, older, or stylistic wording. Safe examples: জ্বলীয় দ্রবণ → জলীয় দ্রবণ, অববিটাল → অরবিটাল, ইল্লেকট্রন → ইলেকট্রন, বন্ধন জোড় → বন্ধনজোড়, সামস্যা → সমস্যা, আঙ্গল → আঙুল, কাধ → কাঁধ, হাটু → হাঁটু. For English, fix clear OCR/typing errors while preserving technical terms, capitalization, proper nouns, and valid spelling variants.

For science/math, preserve readable formulas, equations, variables, values, signs, operators, symbols, units, chemical formulas, element capitalization, charges, states, arrows, equilibrium signs, coefficients, biological names, labels, and classifications. Convert malformed notation only when intended notation is clear. Do not infer missing steps, reconstruct formulas, balance reactions, invent compounds/products/conditions, or guess biology/diagram labels unless unambiguous. If partly unreadable, write best faithful LaTeX and fill #FFC7CE; if unreadable, write [NEEDS_EQUATION_REVIEW] and fill #FFC7CE.

True visuals include images, diagrams, tables, charts, graphs, maps, and figures. Image-Holder is blank when a true visual exists and /hide otherwise. Question-Image is always blank. Never insert actual images. Word equations, Office Math, OMML, and inserted equations are not images; extract them as standard LaTeX source. Preserve readable captions/labels only when present and needed. Do not invent labels or describe visuals unless present or requested.

Strip ক, খ, গ, ঘ labels and variants from all subquestion output cells. Keep only actual subquestion text.

Ask for Single mode or 5 rows per question mode unless specified. Single mode: one row per CQ; passage in Question, number in Number, image status in Image-Holder, board/topic fields when present, actual subquestions in Question_1 through Question_4. Question 1 through Question 4 are display-control columns unless a template requires content there.

5-row mode matches CQ_5_ROW_EXAMPLE.xlsx. Each CQ has one main row and four detail rows. Main row has Number, Question, applicable image/topic/board fields, blank Question 1 through Question 4, and subquestions in Question_1 through Question_4; leave Question_4 blank if ঘ is absent. Detail rows repeat Number, put /hide in Question-Frame, leave passage/image/topic/board fields blank, put actual subquestion text only in that subquestion’s underscore column, set inactive display columns to /hide, and keep inactive underscore cells blank.

Return only the Excel file when converting unless review notes are necessary and the user has not required file-only output.

Math: include every readable equation, formula, symbol, expression, numeric physics value, and unit expression. Wrap math in single dollar signs. Keep Bangla outside math. Use standard LaTeX for fractions, exponents, subscripts, roots, units, omega, resistivity, conductivity, chemistry formulas, scientific notation, functions, derivatives, sums, products, integrals, limits, sets, logic, matrices, and cases. No raw math outside delimiters and no display math delimiters.

PPT unit-spacing override: do not use LaTeX thin-space commands between numbers and units. Use normal spaces inside math mode: $12 V$, $8 s$, $4 A$, $5 \Omega$, $2 \mathrm{k}\Omega$, $1.8 \mathrm{kWh}$, $1.59 \times 10^{-8} \Omega \mathrm{m}$, $5.8 \times 10^7 \Omega^{-1} \mathrm{m}^{-1}$. Before final output, remove bad math patterns: raw omega symbols in math, joined omega-meter commands, omega followed by plain m, parenthesized exponent shorthand, m inverse shorthand, Unicode superscripts/subscripts, improper fraction shorthand, display math delimiters, numeric-unit thin-space commands. If a non-image text cell contains \frac, stored value must end with exactly one newline plus one nonbreaking space. Enable wrap_text for every cell, set vertical alignment top, and do not strip that ending.

