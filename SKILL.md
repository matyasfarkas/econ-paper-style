---
name: econ-paper-style
description: Write or edit economics research papers in a plain, precise register modelled on Christiano and Lindé, with AI writing patterns removed (humanizer). Use when drafting or revising a working paper, journal submission, abstract, introduction, conclusion, referee response, policy note or slides, or when the user asks for a style pass, an editorial pass, to "humanize" a draft or to remove "AI slop".
---

# Economics paper style

The reader is a macroeconomist who will check every sentence. Write the way Christiano and Lindé write: plain words, declarative sentences, each result stated with the condition under which it holds, and no rhetoric.

The patterns to remove, with before and after pairs from real editorial passes, are in `references/patterns.md`.

If the user gives a writing sample, such as an earlier draft in the target voice, read it first and match its sentence length, word choice and the way it introduces numbers. Write new text to match it rather than re-styling text that already reads well.

## Claims

- Every claim is a model result, a verified citation or a data fact. If it is none of these, leave it out and list it in the change log under "Not written, because unsupported".
- Take numbers from the output files as reported, and give what each number is compared with. "Covers x of the y percent of GDP" says more than "covers the gap". After any change to the model or calibration, check every number again.
- Choose the verb the result supports. If lending falls, do not write "stops"; if a channel weakens a loop that still runs, do not write "prevents".
- State a conditional result as conditional, and name the condition.
- Write "to our knowledge, no model combines ..." rather than "the first".
- Report a null result as imprecise and give the interval. Do not write "not a precisely estimated zero".
- If a headline variable is moved by a modelling shortcut, say so and name the outcomes the reader should rely on.
- Keep a claims ledger (claim, source file or citation with page, status) for anything quoted in the paper.

## Structure

- **Abstract.** About 150 words, no citations. Give the question, the mechanism in one sentence, and the main magnitudes.
- **Introduction.** Open with facts or a short quotation from a primary source, then the question and the answer in one contribution sentence. Follow with the model in a paragraph, then the results as short paragraphs that each open with an italic label (`\emph{Monetary policy.}`), then policy, the related literature told as a story, and a roadmap that is specific to the paper. Keep the introduction qualitative; numbers belong in the abstract and the results sections. (The econ-write guide puts magnitudes in the introduction; this skill keeps them out.)
- **Thesis.** State it in one contribution sentence. The abstract and the introduction may share it word for word; the conclusion restates it in new words. Do not add an "Our contribution" paragraph that repeats it, and state the mechanism at most once per section.
- **Conclusion.** Under one page. Restate the result in new words, give the implications, and state the limitations flatly, each with a concrete extension and a citation where one exists. It does not echo the abstract.
- **Less is more.** The main text carries only the ingredients that deliver the one message. Side results, extra episodes, robustness and benchmark detail go to appendices. One clear exhibit is better than several partial ones.

## Words

- Define plain names once and keep them ("We call the entrepreneurs firms").
- Write "households and firms", not "agents".
- Use "we" for the authors. Use the present tense for model results and the past tense for history.
- Every topic sentence states content. There are no staged openers, no one-line closers and no headings that announce a contrast.
- No em dashes (`---` or `—`). Use a comma, a semicolon, parentheses or two sentences. En dashes are for ranges only (`2000--01`).
- Put no evaluative adjective in front of a number. Compare with "against": "output falls x percent, against y percent in the benchmark".

## Doing a style pass

1. Read the whole document before changing anything: main text, appendices and table and figure notes. Structural repetition only shows across sections.
2. Mark and remove the patterns in `references/patterns.md`, strongest first. Keep every fact, number and citation; a rewrite that drops a claim is an error.
3. Run the mechanical checks from the paper folder (quote the globs; zsh expands them otherwise). Adjust the section file pattern to the paper's layout:
   ```
   grep -rnE --include='*.tex' -- '^[^%]*(---|—)' .   # em dashes outside comments: must return nothing
   grep -rniE '\b(additionally|crucial(ly)?|delve|pivotal|underscore[sd]?|showcas\w*|tapestry|testament|landscape|intricate|interplay|vibrant|meticulous|garner|bolster\w*|importantly|notably)\b' --include='*.tex' .
   grep -rniE 'not (only|just|merely)|in short|put simply|what matters|is what makes|the key ' --include='*.tex' .
   texcount -total sections/0*.tex   # main-text sections only; "Words in text" against the target
   ```
   The greps flag text for a reading, not for automatic deletion. A contrast stays when both halves are claims the paper supports.
4. For a whole-paper audit, ask a fresh reviewer (for example a subagent on a stronger model) to list structural repetition: the thesis stated twice in a section, repeated caveats, a conclusion that echoes the abstract. Apply what holds up.
5. Compile with no undefined references or citations, and check the page count.
6. Write a short change log for the coauthors: what changed and why, corrections to earlier claims, and the claims that were not written because they were unsupported.

## Disclosure

If an AI tool helped prepare the paper, say so on the title page and state that the authors are responsible for all content. An IMF Working Paper also carries the standard IMF disclaimer.
