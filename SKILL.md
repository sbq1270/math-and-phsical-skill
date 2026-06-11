---
name: math-and-phsical
description: "Create end-to-end Chinese middle-school and high-school math or physics explanation videos from a single problem: write a clear solution script first, wait for user confirmation, create Manim visual or pure-derivation segments per subquestion, render 480p previews for review, then render 1080p final videos with a fixed 4:3 cover/thumbnail, an in-video original-problem display segment, and merged explanation segments. Use when creating, revising, or reviewing Manim teaching videos, formula derivation videos, proof animations, function/geometry/physics visualizations, or complete problem-analysis videos."
---

# MathAndPhsical

Use this skill to design the layout and presentation style for math or physics problem explanation videos. Prefer clear teaching structure over decorative effects.

## Workflow

1. Identify the problem type and teaching goal.
2. Decide whether a visual model helps:
   - Use **visual explanation** when graphs, geometry, number lines, force diagrams, motion, variables, regions, or transformations clarify the idea.
   - Use **pure derivation** when the problem is mainly algebraic calculation, inequality proof, sequence recurrence, symbolic transformation, or logical proof without a helpful diagram.
3. Keep each screen focused on one teaching objective.
4. Reveal information gradually: conditions first, then the current object, then labels, then reasoning.
5. Verify that every label, formula, and text block stays inside the safe area and does not overlap other visual elements.

## End-to-End Problem Video Workflow

Use this workflow when the user starts from one complete problem and wants a finished explanation video.

1. Parse the problem and identify all subquestions, known conditions, targets, and natural teaching stages.
2. Write a complete solution narration/script first. Make the solution clear, rigorous, classroom-friendly, and easy for middle-school or high-school students to follow.
3. Stop after the written solution and ask the user to confirm or revise the explanation. Do not start video production until the user confirms the solution script.
4. After confirmation, split the video into segments according to the problem structure:
   - Usually create one video per subquestion.
   - Add a short concept-introduction segment only when it is necessary for understanding the later subquestions.
   - Name and order the segments clearly so they can later be merged without confusion.
5. Implement the Manim videos using either Layout A or Layout B for each segment.
6. Render preview videos at 480p first. Provide the preview paths and ask the user to review the content, pacing, layout, labels, and formula readability.
7. Iterate on the 480p previews until the user confirms that all segment videos are acceptable.
8. After confirmation, render every segment again at 1080p.
9. Create the video cover/thumbnail using the fixed cover style in **Cover Style**. This is a separate cover asset unless the user explicitly asks to insert it into the video.
10. Create an in-video problem-display segment before the explanation begins. This segment should show the original problem statement itself, use the same calm dark classroom style as the approved final videos, and contain no teaching goals, outlines, summaries, or extra commentary unless the user explicitly asks.
11. Merge the in-video problem-display segment and all final explanation segments into one complete explanation video, preserving the intended order.
12. Deliver the final merged video path and mention that it is ready for later voiceover, background music, subtitles, or manual editing. Also provide the cover/thumbnail path when created.

## Cover Style

Use this fixed style for the cover/thumbnail of a complete problem explanation video.

- Use a 4:3 cover image by default, preferably 1440x1080 unless the user requests another size.
- Use a dark background, large centered typography, and a quiet mathematical visual accent.
- Put the exam/course line on the first row, for example "2026高考数学".
- Put the paper/question line on the second row, for example "新一卷第18题".
- Make the first row white and the second row warm yellow.
- Use a faint cyan ellipse/coordinate-axis motif behind the text and short cyan accent lines below.
- Do not put the full problem statement, solution outline, teacher notes, or extra explanatory text on the cover.
- Keep the text large, centered, high-contrast, and readable as a thumbnail.

## In-Video Problem Display

Use this as the first video segment before the explanation begins.

- Show the original problem statement itself, including all known conditions and subquestions.
- Use the same dark, high-contrast, classroom-friendly style as the approved complete videos.
- The style should feel consistent with the later Manim explanation: restrained colors, readable formulas, and generous spacing.
- Do not add teaching goals, outlines, summaries, decorative slogans, or commentary.
- If the problem is long, split it into readable lines or pages rather than shrinking the text too much.
- This segment is part of the merged explanation video and should appear before the first explanation segment.

## Shared Presentation Rules

- Put the current original problem text at the top of each explanation segment. Do not use only a short summary title such as "求方程" or "面积关系"; for example, when explaining subquestion (2), the top area should show the original text of subquestion (2), or the relevant original subpart if the explanation is split into (i), (ii).
- Keep the top problem text readable and naturally spaced. If the original text is long, split it into multiple short lines or multiple problem-display pages; do not squeeze characters, over-compress formulas, or let text crowd the top edge.
- Do not add meta-instructions such as "look left" or "read right".
- Keep the screen calm, high-contrast, and classroom-friendly.
- Use large readable text, generous spacing, and restrained colors.
- Use consistent colors for known conditions, current variables, highlighted steps, conclusions, and contradictions.
- Avoid showing too much at once. Hide, fade, or clear stale content before starting a new stage.
- Keep formulas short where possible. Split long formulas or long reasoning chains into multiple steps.
- Make explanations detailed and accurate enough for students to follow. Do not skip non-obvious algebraic transformations, geometric relations, sign conditions, or equality conditions.
- Prefer methods and notation familiar to Chinese middle-school and high-school students. Avoid university-style notation or methods such as determinants, linear algebra, advanced calculus, measure theory, or abstract mappings unless the problem explicitly requires them or the user asks for them. When an advanced-looking idea has a high-school alternative, use the high-school version.
- Avoid label collisions. Move labels away from curves, points, arrows, axes, shapes, and other text.
- Do not let text touch screen edges, cross panel boundaries, or cover important graphics.
- Make animation serve the explanation: each motion should show a relationship, transformation, comparison, or logical dependency.

## Layout A: Visual Explanation

Use this layout when a graph, geometric diagram, physical model, motion process, or spatial relation helps students understand the problem.

### Screen Structure

- Place the current original problem text across the top. This top strip is the third layout area, separate from the left visualization area and the right reasoning area.
- Use the left side as the main visualization area and let it occupy the larger part of the screen.
- Use the right side for reasoning, proof steps, calculations, or concise narration.
- Place given conditions, definitions, or key known information near the upper-left area as fixed reference content.

### Left Visualization Area

- Show only visual aids: coordinate systems, graphs, number lines, geometric figures, force diagrams, motion paths, regions, arrows, points, auxiliary lines, or highlighted intervals.
- Do not place long proof text or conclusion-heavy derivation at the lower-left area.
- Keep labels minimal and spatially separated.
- Use labels to identify objects, not to replace the proof.
- For math:
  - Function problems: emphasize graph shape, intervals, monotonicity, moving points, and comparison positions.
  - Geometry problems: emphasize figure structure, auxiliary lines, equal angles, equal lengths, parallel/perpendicular relations, and changing viewpoints.
  - Probability/statistics problems: emphasize sample space, tree diagrams, tables, distributions, or area models when useful.
- For physics:
  - Mechanics problems: emphasize object model, forces, acceleration, velocity, displacement, constraints, and reference direction.
  - Electricity/magnetism problems: emphasize circuits, fields, current direction, potential difference, equivalent transformation, and key measuring points.
  - Waves/optics/thermal problems: emphasize path, phase, image formation, energy transfer, or state changes.

### Right Reasoning Area

- Put proof ideas, derivations, formulas, and calculations on the right.
- Show one sub-goal at a time. Clear or fade the right panel before starting the next sub-goal.
- Use numbered steps for proofs and calculations.
- Align numbered steps carefully: the step number and the corresponding text/formula must sit at the same visual height, with a stable number column and a stable content column.
- Use generous and consistent line spacing. Fractions, radicals, and multi-symbol formulas need more vertical room than plain text; do not let adjacent numbered lines look compressed or misaligned.
- If one proof or one sub-goal must be split across multiple right-panel pages, keep the numbering continuous across pages. For example, if the first page ends at step 7, the next page should begin at step 8, not step 1.
- Highlight only the current step or the step just concluded.
- If reasoning is long, split it into multiple screens instead of shrinking everything too much.

## Layout B: Pure Derivation

Use this layout when the problem does not need a meaningful visual model.

### Screen Structure

- Place the current original problem text at the top.
- Use a central derivation board as the main area.
- Put known conditions and target conclusions at the top of the board or upper-left of the board.
- Do not force an empty diagram area when no diagram helps.

### Derivation Board

- Reveal formulas and reasoning line by line.
- Keep one main logical thread on screen.
- Use spacing to separate assumptions, transformations, conclusions, and side notes.
- Split long derivations into stages. Finish one stage, then clear or fade it before the next.
- When a single derivation is split into multiple stages, keep numbered steps continuous across stages rather than restarting from 1.
- For classification problems, first show the classification framework, then handle each case separately.
- For contradiction, construction, substitution, induction, or parameter methods, mark the current strategy briefly before the detailed steps.

### Formula Handling

- Use aligned equations when several transformations belong to the same chain.
- Break long expressions across lines before they approach the edge.
- Add short side notes such as "by monotonicity", "substitute the condition", "multiply by a positive number", or "case analysis" only when they clarify a non-obvious step.
- Avoid full-sentence commentary beside every formula.

## Final Check

Before delivering or rendering, check:

- The chosen layout matches the problem type.
- The top problem text is the current original subquestion, not merely a short summary title, and it is clear without crowding.
- Conditions and target conclusions are easy to find.
- Numbered steps have aligned number/content baselines or centers, stable spacing, and continuous numbering across pages within the same proof.
- The solution uses high-school-accessible notation and methods unless the user explicitly approves a more advanced approach.
- Every visual label is readable and non-overlapping.
- The right panel or derivation board has no overflow.
- Each stage has a single focus.
- Stale content has been cleared before a new proof, case, or calculation begins.
- The final video feels like a teacher guiding students through the idea, not a page of static notes.
