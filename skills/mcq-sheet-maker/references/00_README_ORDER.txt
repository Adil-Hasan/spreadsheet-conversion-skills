MCQ GPT Instruction Pack v6 — Restructured
==========================================

This version restructures the instruction pack so equation-related rules are centralized.

Main design:
- Equation-related rules are contained in ONE file:
  `05_EQUATION_AND_LATEX_RULES.txt`

This single equation file includes:
- Word equation / OMML / Office Math extraction
- Standard LaTeX formatting
- Fractions
- Superscripts/subscripts
- Physics units and values
- Omega/Ohm/resistivity/conductivity handling
- Bad equation pattern cleanup
- Low-confidence equation marking
- Fraction line spacing rule

Use this order when adding modular instruction files:

1. 01_CORE_ROLE_AND_PRIORITY.txt
2. 02_SCHEMA_COLORS_AND_OUTPUT.txt
3. 03_EXTRACTION_AND_COLUMN_RULES.txt
4. 04_IMAGE_AND_VISUAL_RULES.txt
5. 05_EQUATION_AND_LATEX_RULES.txt
6. 06_ANSWER_DUPLICATE_AND_BATCH_RULES.txt
7. 07_FINAL_QC.txt

If the GPT Instructions field has enough space:
- Use `09_FULL_COMBINED_PROMPT.txt`

If the GPT Instructions field is limited:
- Use `08_COMPACT_SYSTEM_PROMPT.txt`
- Upload the modular files as reference knowledge.

Use:
- `10_GPT_BUILDER_SETUP_PROMPT.txt`

to build the custom GPT.

Core rules preserved:
- Word equations are NOT images.
- Equations must be converted into LaTeX and wrapped in `$...$`.
- True diagrams/circuits/graphs/tables/images are Type=Image.
- Image-content cells remain blank and filled #D9EAF7.
- Low-confidence equations contain best LaTeX attempt and are filled #FFC7CE.
- Correct answer instruction cells use /#41FF96 and fill #41FF96.
- `\frac` cells must end with exactly one visible blank line using the forced ending `\n\u00A0`, not raw `\n\n`.
