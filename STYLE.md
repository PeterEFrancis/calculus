# Calculus book style guide

Use this guide for additions and revisions. It records the author's chosen
conventions; an inconsistent older passage is not a reason to copy the
inconsistency. Keep changes focused and preserve the surrounding voice.

## Voice and explanations

- Write directly to a student taking a first or second calculus course.
  Use conversational **we**, **you**, contractions, and occasional light humor.
- Start with the idea or picture, then give the precise statement and calculation.
  Explain what a calculation means and why the next step helps.
- Prefer familiar language and short, connected explanations. Keep necessary
  hypotheses explicit without making the exposition needlessly formal.
- Natural transitions include “Notice that,” “In other words,” “Remember,” and
  “Let's.” Use them when they help, not as a formula for every paragraph.
- Introduce new vocabulary in bold. Separate a definition from an informal
  explanation or a useful analogy.
- Work through the algebra students need to follow. In longer computations,
  put short explanations on the right of aligned steps when helpful.
- Include an illustrative worked example when introducing a method.

## Mathematical language and notation

- Always use `\varepsilon`, not `\epsilon`.
- Introduce new symbols and named facts before their first use, even when
  their proofs come later. Distinguish **Euler's formula**,
  `e^{i\theta}=\cos\theta+i\sin\theta`, from its special **Euler's identity**,
  `e^{i\pi}+1=0`.
- Use `f'(x)` for a function's derivative and square brackets for the derivative
  of an expression: `[f(x)g(x)]'`, not `(f(x)g(x))'`. Prefer this notation to
  `\frac{d}{dx}` when the variable is already clear.
- A **critical number** is an input `a` in the domain with `f'(a)=0` or with
  `f'(a)` nonexistent. A **critical point** is the graph point `(a,f(a))`.
  This book's critical-number convention includes defined domain endpoints
  where a two-sided derivative does not exist.
- Continuity at a point requires the function to be defined there. At an
  included interval endpoint, use the appropriate one-sided condition.
- A discontinuity can occur at an omitted interior input when the function is
  defined on a punctured open neighborhood: holes and poles count. Unrelated
  numbers outside the domain and excluded domain endpoints do not count.
- Distinguish an undefined substitution, an indeterminate form, and an infinite
  limit. Informal substitution can guide a limit calculation; justify the
  resulting limit with the appropriate method.
- State domain, sign, and nonzero-denominator conditions where they matter.
  Do not silently treat an infinite limit as a finite real value.

## Examples, lists, and margin notes

- Put worked examples in `exampleblock`. Use `[breakable]` for long examples.
  The existing style provides the left indentation, bracket, pale shading,
  internal padding, and small **EX** marker.
- Do not repeat “For example” just to announce an already marked example.
- Definitions, reference formulas, general derivations, and theorem statements
  are not examples merely because they contain calculations.
- Ordinary lists can use regular bullets. Use numbered steps for an actual
  procedure or a sequence of tasks. Do not use a bullet as an example marker.
- Use `\mar{...}` for a short question, drawing prompt, or useful variation.
  Place ordinary margin notes outside `exampleblock`; `\marginpar` is not safe
  inside that box.

## Figures

- Draw mathematical figures in native TikZ. Keep reusable drawings in
  `content/figures/` and include them with `\input`.
- The decorative sea-monster engraving on the quote page is an intentional
  raster exception.
- Use the shared colors defined in `Calculus.tex`:

  | Color | Use |
  | --- | --- |
  | `figureblue` | Base blue from the volume figures; mix with white for shading. |
  | `figureaccent` | Main blue outlines, highlighted curves, and dimensions. |
  | `figuresecondary` | Darker blue for a contrasting curve or component. |
  | Black, gray, white | Axes, ordinary geometry, context, guides, and backgrounds. |

- Use pale blue for selected slices or regions and gray for surrounding context.
  Preserve useful shading differences on three-dimensional solids.
- For transparent solids and highlighted slices, use actual `fill opacity`
  or an isolated transparency group for a surface made of many patches.
  Include complete rear rims and edges so they show through the front faces;
  draw hidden edges dashed and visible front edges solid.
- Keep washer cross-section ellipses vertical. Use continuous shading across
  each highlighted face so separate semicircle fills do not create a seam.
- Distinguish comparisons with solid/dashed lines or markers as well as color.
  Keep legends and explanatory prose consistent with those line styles.
- Use the book's math font, generally `\small` labels, and about `.7pt` lines.
  Dense reference diagrams may need `\footnotesize`. Avoid shrinking an entire
  diagram until its text becomes unreadable.
- Standalone diagrams and diagrams referenced elsewhere belong in a `figure`
  environment with a concise numbered caption. Put `\label` after `\caption`.
- Small sketches explained directly within an example or proof may remain
  unnumbered and uncaptioned.
- Do not put a separate rectangular frame around a figure. The shaded bracket
  belongs to the whole example, not to each diagram inside it. This does not
  prohibit boxes that are part of a diagram, such as flowchart nodes.
- Keep labels clear of curves and dimensions. Connect boundaries accurately,
  distinguish visible and hidden edges, and put axis ticks on the actual axes.

## Theorems, proofs, and organization

- Give theorem statements descriptive names: `\begin{thm}[Name]`.
- Use only results established in the book or basic mathematics. Check the
  dependency order and avoid circular arguments.
- Write proofs for a Calculus 1 student. Explain the idea before the details,
  why a helper function or bound is chosen, and the key algebraic steps.
  Define unfamiliar proof vocabulary where it is used.
- For later topics, briefly recall the chapter's definitions and build on
  elementary algebra, geometry, and the calculus already developed. Avoid
  unexplained real-analysis results such as compactness or uniform continuity.
  State basic starting assumptions about real numbers explicitly.
- Put Differential Equations after Integration and Applications, followed by
  Sequences and Series. Keep sequences, series, and power series together in
  that order.
- Order the Pre-Calculus chapters as Functions on the Real Line, Algebra,
  then Trigonometry. Algebra has separate subsections for properties of
  exponents, properties of logarithms, the Binomial Theorem, and completing
  the square. Call the logarithm identities **properties**, rather than rules.
- Include Moments and Centroids in Applications of Integrals.
- Order the integration applications as Areas, Arc Length, Volumes and
  Surface Area, Average Values, Moments and Centroids, Work, then Probability.
- Keep the separate **Proofs** part at the end, outside the lettered Appendix.
  Background facts come first; chapter groups follow the book's order.
- Use `\proofchapter` for chapter groups and `\proofheading` for individual
  proofs. Named theorem headings use **Name (Theorem #.#)** with an automatic
  reference, not a typed number. Other proof headings use the result's name.
  Headings for special limits consist of the limit in mathematical notation.
- Proofs use readable prose and calculations under those headings, with a
  `proof` environment for the argument; do not wrap them in theorem boxes.
- Use `\proofref{proof:key}` at the source result and the same key in
  `\proofheading`. The existing macros create the small shaded margin links
  and the return page link. Preserve their placement and labels.
- Begin each chapter and each proof chapter group on a new page. The table of
  contents goes through subsections, not subsubsections.
- Appendix chapters use letters. Avoid hardcoded chapter, theorem, figure,
  proof, or page numbers in cross-references.

## Editing practice

- Edit the existing chapter and shared macros in place; reuse established
  environments instead of adding a competing visual system.
- Compile the main document after LaTeX changes and let references settle.
  For visual changes, check the affected layout when available. Keep checks
  proportional to the change.
- Update this guide when the author chooses a new convention. A local style
  guide is not a request to change unrelated passages or publish to GitHub.
