# Patterns to remove

The section numbers refer to the humanizer skill (github.com/blader/humanizer, v4.0.0, MIT licence, © 2025 Siqi Chen), which credits Wikipedia's "Signs of AI writing". Read the full list there for patterns not covered here. The examples below are edits made during editorial passes on an unpublished economics working paper; numbers are replaced by x and y.

A pattern is a reason to reread a sentence, not to delete it. A contrast, a colon or a short sentence stays when it carries a claim the paper supports. Several tells together in one passage are the signal.

## Staging instead of stating

**Not X but Y, and contrasts that only add weight (§1).** Includes headings that stage a contrast and the "X instead of Y" rhythm.
- Heading "What the evidence shows and what it does not": removed. One sentence kept, pointing to the experiment that answers the question.
- "not a precisely estimated zero": removed. Give the estimate and its interval.
- "X instead of Y" repeated through a section: compare with "against" ("x percent of lender equity against y").

**One-line closers and dramatic fragments (§2).**
- "What collapses is the flow." / "Firm cash changes the prediction." / "The size of the easing matters most." / "Thinner or more exposed lenders change this little.": removed; the paragraph already said it.
- Punchy topic sentences ("Firm cash changes the bust."): replaced by a topic sentence that states what happens.

**Staged run-up before the point (§4).** Openers that announce, colon reveals and counting.
- "The mechanism is a stop in refinancing." / "The first change, then, is that ..." / "In the model, then, ...": cut; start with the content.
- "Two features", "in two ways", "in three ways", "Two settings" used as a drumroll: drop the count, or keep it only when the list follows at once and the count is right ("three building blocks" listed four; it became "four features").
- Rhetorical colons ("but no further:"): rewrite as one plain sentence.

**Announcing topic sentences (§4, §25).** The commonest tell to survive a word-level pass. The sentence promises content instead of giving it: it sorts results into kinds, says they "differ", "matter" or "depend", or points at a step or section. Delete it and open the paragraph with its first concrete claim. Real fixes from the NSP paper (Farkas and Jakab, November 2026):
- "Such priors do different things depending on what the data already say.": deleted; the paragraph now opens "The narrative on the 2021--2023 surge sets the split between supply and demand at one half without changing the fit."
- "Outside information on these properties can be brought in directly.": deleted; the next sentence says how.
- "That step comes from the structural VAR literature.": the paragraph opens "In structural VARs, Antol\x27in-D\x27iaz and Rubio-Ram\x27irez restrict ..."
- "These are the joint implications of priors that look reasonable one at a time.": became "Priors that look reasonable one at a time thus allow a wide range of transmission, as Del Negro and Schorfheide point out."
- "The likelihood says little about X, and the priors say little more.": an echo built for rhythm; state the fact ("two modes with slopes a factor of two apart fit equally well").
- "This section derives ...", "This appendix describes ...": cut; the first equation or claim follows.
- "In each case the comparison that tells what the prior did is ...": became "In each case we measure the effect of the prior against the posterior without it."
Test: if the sentence could open a paragraph in a different paper, it is staged.

**Cleft and saying forms (§3, §4).**
- "What decides ... is", "is what makes", "what matters is ... whatever its form", "is part of the answer", "The data suggest that the spread matters": say who does what. "Cash protects the lender" beats "What protects the lender is cash."

## Rhythm and punctuation

- **Em dashes (§8).** None, in LaTeX (`---`) or Unicode (`—`). En dashes only in ranges.
- **Forced triads (§6) and repeated openings (§7).** Three parallel items only when there are three things.
- **Numerals opening a sentence.** Rewrite so a word comes first.

## Inflation and vocabulary

- **Overused AI words (§12).** The humanizer list: actually, additionally, align with, bolstered, crucial, deep dive, delve, enduring, enhance, garner, gate (figurative), highlight (verb), interplay, intricate, key (adjective), landscape (abstract), meticulous, pivotal, quietly, robust (figurative; keep robustness checks), showcase, tapestry, testament, underscore (verb), valuable, vibrant.
- **Inflated significance (§13).** No "first", "novel", "striking" or "important" in front of a result; say "to our knowledge" and let the number speak. No evaluative adjective in front of a number.
- **"Agents".** Write "households and firms", or name the sector.

## Headings and document talk

- **Decorative headings (§20).** "How robust" became "Sensitivity"; "Model changes since draft v4" became "Default switches". A heading names its content.
- **Writing about the document (§25).** Cut sentences that describe what a section will do when the next sentence does it. Keep one roadmap paragraph at the end of the introduction.

## Structural repetition (whole-paper audit)

Word-level fixes are not enough; a draft can be clean sentence by sentence and still repeat itself. From one whole-paper audit:
- The thesis appeared a third time in an "Our contribution" paragraph: deleted.
- The conclusion repeated the abstract: rewritten in new words.
- The same caveat ("lenders stand for all lenders") appeared in several sections: kept once.
- The mechanism was stated in every section: kept once each in the mechanism and model sections.

## Precision (not in the humanizer)

Real fixes, with numbers replaced:

| Before | After | Why |
|---|---|---|
| new lending against collateral stops | falls | it falls; it does not stop |
| eight years later | through quarter 40 | the exact horizon of the run |
| cash covers the gap | cash covers most of the gap, x of the y percent of quarterly GDP | the number, with its reference |
| cash prevents this loop | cash weakens this loop | the price of capital still falls |
| a bust on these firms could be deep | the model predicts a deep recession only when the firms hold almost no cash, and the outcomes at two cash ratios | speculation replaced by the results |
| the first model to ... | to our knowledge, no model combines ... | a novelty claim the authors can defend |
| a result stated flatly | the result, with "conditional on the monetary policy rule" | the result holds under a condition; name it |
