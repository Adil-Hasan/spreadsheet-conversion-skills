# Content Correction Accuracy Instructions

## Purpose

Use these instructions to preserve the accuracy, meaning, wording, and subject integrity of source content during cleanup or correction.

The goal is to fix clear mistakes without changing the author’s intended meaning, style, structure, or level of detail.

## Core Accuracy Principles

1. **Do not invent content.**  
   Do not add missing facts, examples, explanations, terms, formulas, references, headings, captions, names, dates, or values unless they are clearly present or strongly supported by the source.

2. **Preserve the original meaning.**  
   Corrections must keep the same intended idea. Do not rewrite, simplify, expand, or modernize clean source text just because another version sounds better.

3. **Correct only strongly supported errors.**  
   Fix spelling, OCR, typing, punctuation, formula, unit, grammar, or wording errors only when the intended correction is clear from the source text, nearby context, repeated context, or standard subject knowledge.

4. **Keep uncertain text faithful.**  
   If the intended correction is unclear, keep the safest faithful version instead of guessing. Mark or report the uncertainty separately when needed.

5. **Preserve source order and structure.**  
   Keep paragraphs, line breaks, lists, numbering, statements, labels, equations, and references in their original order unless the source is clearly corrupted and the intended structure is obvious.

6. **Do not paraphrase clean text.**  
   If a sentence is already readable and meaningful, leave it unchanged except for required formatting or obvious typo cleanup.

## Correction Scope

Allowed corrections include:

- OCR mistakes
- Typing mistakes
- Broken punctuation
- Missing or extra spaces
- Obvious spelling errors
- Broken Bangla or English words
- Formula transcription errors
- Unit formatting errors
- Symbol/subscript/superscript errors
- Clearly malformed mathematical or scientific notation
- Clear subject-specific terminology errors

Not allowed unless strongly supported:

- Adding new explanations
- Removing source ideas
- Changing the difficulty or tone
- Replacing valid wording with preferred wording
- Changing facts, values, units, dates, names, or formulas by assumption
- Completing incomplete content by guessing
- Reordering content for style alone

## Semantic Correction Rules

After basic cleanup, perform a final meaning check.

The corrected content should read as coherent, sensible source text. Do not leave mechanically converted text that is technically formatted but semantically broken.

Fix unnatural or impossible wording only when the intended phrase is strongly supported.

Examples:

- `জ্বলীয় দ্রবণ` → `জলীয় দ্রবণ`
- `অববিটাল` → `অরবিটাল`
- `ইল্লেকট্রন` → `ইলেকট্রন`
- `বন্ধন জোড়` → `বন্ধনজোড়`
- `সামস্যা` → `সমস্যা`
- `আঙ্গল` → `আঙুল`
- `কাধ` → `কাঁধ`
- `হাটু` → `হাঁটু`

Do not change literary, regional, or older wording if it is valid and not corrupted.

## Bangla Text Accuracy

For Bangla content:

1. Preserve original Bangla wording as much as possible.
2. Fix only clear spelling, OCR, or punctuation corruption.
3. Do not replace valid Bangla style with a more modern or preferred phrasing.
4. Keep Bangla explanatory text outside mathematical notation.
5. Do not merge separate Bangla lines unless the source clearly shows they belong together.
6. Do not split a complete sentence unless the source clearly requires it.

## English Text Accuracy

For English content:

1. Fix clear OCR or typing errors.
2. Preserve original capitalization unless it is clearly wrong.
3. Preserve technical terms and proper nouns.
4. Do not rewrite clean sentences for style alone.
5. Do not convert British/American spelling unless the source is inconsistent because of OCR or typing error.

## Mathematical and Formula Accuracy

Mathematical expressions, variables, formulas, symbols, numeric values, and units must be preserved carefully.

1. Do not omit readable formulas or equations.
2. Convert malformed notation only when the intended notation is clear.
3. Preserve original values, variables, signs, operators, and units.
4. Use standard notation for fractions, exponents, subscripts, roots, sets, intervals, ratios, functions, and angles.
5. If a formula is partially unreadable, keep the best faithful transcription and mark the uncertainty.
6. Do not infer missing mathematical steps unless the source clearly supports them.

Examples of safe corrections:

- `Q/t` → `\frac{Q}{t}` when clearly intended as a fraction
- `x²` → `x^2`
- `x₁` → `x_1`
- `10⁻⁵` → `10^{-5}`
- `m^-1` → `m^{-1}`

## Unit and Symbol Accuracy

1. Preserve numeric values exactly.
2. Keep units attached to the correct values.
3. Fix clear unit-symbol corruption.
4. Do not change units unless the source clearly contains an OCR or typing error.
5. Use readable spacing between numbers and units.
6. Do not convert unit systems unless explicitly requested.

Examples of safe corrections:

- `5 Ω` → `5 \Omega`
- `1.8 kwh` → `1.8 kWh`
- `1.59×10⁻⁸ Ωm` → `1.59 \times 10^{-8} \Omega m`

## Chemistry Content Accuracy

For chemistry content:

1. Preserve element capitalization exactly.
2. Fix clear OCR errors in chemical formulas.
3. Use subscripts for chemical formula numbers when formatting allows.
4. Preserve charges, states, arrows, equilibrium signs, and coefficients.
5. Balance or reconstruct reactions only when the intended reaction is unambiguous from the source and standard subject context.
6. Do not guess unknown compounds, products, variables, or reaction conditions.

Common safe normalizations:

- `O2` → `O_2`
- `H2` → `H_2`
- `Cl2` → `Cl_2`
- `CO2` → `CO_2`
- `H2O` → `H_2O`
- `H2SO4` → `H_2SO_4`
- `HNO3` → `HNO_3`
- `Cao` → `CaO`
- `HCI` → `HCl`
- `KCI` → `KCl`
- `C1` → `Cl`
- `NaOCI` → `NaOCl`
- `PH` or `pll` → `pH`

## Physics Content Accuracy

For physics content:

1. Preserve quantities, variables, units, and signs exactly.
2. Keep scalar/vector meaning intact.
3. Fix broken notation only when clearly supported.
4. Keep formulas readable and standard.
5. Do not change physical quantities or units by assumption.
6. Keep numeric values granular and readable.

## Biology Content Accuracy

For biology content:

1. Preserve biological terms, names, labels, and classifications.
2. Fix clear OCR or spelling corruption in terminology.
3. Do not invent labels, parts, processes, or relationships.
4. Do not dump broken or scattered visual labels into the cleaned text unless they are meaningful and needed.
5. Preserve capitalization for scientific names when present.

## Visual or Diagram-Related Text

When content comes from or refers to a diagram, table, chart, graph, map, or figure:

1. Preserve meaningful captions and labels if readable.
2. Do not invent missing labels.
3. Do not convert scattered unreadable visual fragments into body text.
4. Do not describe the visual unless the description is present in the source or explicitly requested.
5. If visual text is unreadable, mark it for review instead of guessing.

## Low-Confidence Handling

Use a clear review marker when content cannot be corrected confidently.

Recommended markers:

- `[UNCLEAR_TEXT]`
- `[NEEDS_REVIEW]`
- `[NEEDS_EQUATION_REVIEW]`
- `[UNREADABLE]`

Use markers sparingly. Prefer faithful transcription when readable enough.

## Final Content Check

Before finalizing corrected content, verify:

1. No source meaning was changed.
2. No missing content was invented.
3. No readable equation, value, symbol, or unit was omitted.
4. Clean text was not unnecessarily paraphrased.
5. Corrections are strongly supported.
6. Uncertain corrections are marked or reported.
7. Bangla and English text remain readable and natural.
8. Subject-specific notation is accurate.
9. Formatting changes did not alter facts or meaning.
10. The final result remains faithful to the original source.
