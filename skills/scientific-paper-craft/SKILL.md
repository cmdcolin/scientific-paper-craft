---
name: scientific-paper-craft
description: Structure and revision techniques for scientific and software-tool papers, drawn from published writing guidance. Covers sentence stress, paragraph arcs, figure captions, Methods detail, Discussion order and visualization-paper framing. Use when drafting or revising a manuscript, planning a revision pass, or reviewing a paper's organization. Run anti-ai-writing-tropes after this one.
---

# Scientific paper craft

Techniques for revising a research or software-tool paper, each with its source.
Where a project's own style rules conflict with anything here, the project's
rules win.

## Topic and stress position

Gopen & Swan, "The Science of Scientific Writing" (*American Scientist*, 1990).
Readers look at the start of a sentence for context and at the end for the
point. Writers often reverse this: known material lands in the stress position
and the new fact sits mid-sentence before a trailing qualifier.

- Start a sentence or clause with what the reader already knows.
- End it with the new information.
- End a paragraph's key sentence on the paragraph's point.
- A dangling "it", "this" or "that" in topic position gives the reader nothing to
  link to. Name the subject.

## Paragraph arcs

Mensh & Kording, "Ten Simple Rules for Structuring Papers" (*PLOS Comp Biol*,
2017).

- Each paragraph has Context (the problem or what is known), Content (what you
  did or found) and Conclusion (what it means). A paragraph without Context
  reads as a list of facts.
- The paper nests the same arc: the Introduction sets context for the whole,
  each Results subsection is its own arc, and the Discussion closes the
  outermost one.
- Name the single central contribution before drafting, and let every section
  serve it. A paper with two central claims reads as unfocused even when both
  are true.

## Hype words

Vinkers et al. (*BMJ*, 2015) found positive superlatives in PubMed abstracts
(*novel, robust, innovative, unprecedented*) up 1,404% from 1974 to 2014. Style
guides such as *J. Org. Chem.* ban *convenient, efficient, elegant, facile,
first, new, novel, simple, unique, unprecedented, versatile, powerful, crucial,
groundbreaking, transformative*.

The words are not false. They assert a judgment the reader should reach from
evidence. Delete the adjective: if the sentence claims the same thing, the
adjective was rhetoric. Replace it with the number or the figure that would make
the reader reach the judgment.

## Figures and captions

Journal caption guidance (AJE, TAA) and Tufte.

- A reader skims the abstract, figures and conclusions before deciding to read.
  Each figure has to work without the body text.
- Caption order: a one-line title saying what the figure shows, the minimum
  needed to read it (what is plotted, what a color or mark means), then one
  sentence with the result.
- Label panels, axes and encodings in the figure or caption. Never send the
  reader to Methods to decode an axis.
- One figure carries one message. A figure that supports two claims may be two
  figures.

## Active voice

NIH and Nature style guidance and Strunk & White agree. A passive with no actor
hides who did what: "errors were observed" against "we observed errors in the
alignment track". In software papers, say what the software does.

Keep idiomatic passives ("is required") and passives whose actor does not
matter. Do not give software intent ("the track decides"): it executes.

## Omit needless words

Strunk & White: "vigorous writing is concise." Cut content that does not
inform. Do not cut the connectives that let a sentence parse, or the result is
stilted rather than short. In Methods, padding competes with the detail a reader
needs to repeat the work.

## Reproducibility

Romano & Moore, "Ten Simple Rules for Writing a Paper About Scientific
Software" (*PLOS Comp Biol*, 2020). A Methods section, read with its cited
references, has to let a reader repeat every procedure.

- Give versions, parameters and hardware at the precision needed to reproduce a
  benchmark number.
- Tie every reported number to a named, current run.
- State what the harness does. A clause explaining why the alternative was
  rejected is a justification, not a method. Move it to the Discussion with
  evidence, or cut it.

## Discussion order

State the key findings, place them against prior work to locate the novelty,
state limitations, then speculate. Speculation after limitations reads as
informed by them.

- Forward-looking claims are earned only here, and only on findings Results
  already supports.
- Introduce no new data, citations or ratios in the Discussion.

## Visualization papers

Munzner, "A Nested Model for Visualization Design and Validation" (*IEEE TVCG*,
2009). A contribution sits at one of four levels, and validation differs at each:

1. Domain situation: who the users are and what problem they have.
2. Data and task abstraction: the operations and data types, independent of any
   visual design.
3. Encoding and interaction idiom: the marks, channels and interactions.
4. Algorithm: the implementation that computes or renders the idiom.

A flaw at a lower number cascades down. A slow idiom, a level-4 symptom, can be a
level-2 abstraction mistake. Attribute each claim to its level. A rendering
benchmark is a level-4 result and does not justify a level-3 design choice.

## Revision order

1. Structure: does each section and paragraph have its arc, and does the
   Abstract alone state the central contribution?
2. Sentence flow: read each paragraph's sentence endings in sequence. Do they
   carry the new information?
3. Hype sweep: grep for the banned words above and any project word list. Cut
   each one or replace it with a measurement.
4. Captions: can each figure be read from its caption alone?
5. Methods: could a reader rerun every number in Results from Methods as
   written?
6. Discussion: does every claim trace to something earlier in the paper?

Run `anti-ai-writing-tropes` after this pass. It catches tics such as mannered
compression and comma-hung appositives, and some "be concise" advice above
would conflict with it if applied afterward.

## Sources

- Gopen & Swan, "The Science of Scientific Writing," *American Scientist* 78(6),
  1990.
- Mensh & Kording, "Ten Simple Rules for Structuring Papers," *PLOS Comp Biol*,
  2017.
- Romano & Moore, "Ten Simple Rules for Writing a Paper About Scientific
  Software," *PLOS Comp Biol*, 2020.
- Medvedev, "Ten Simple Rules for Writing Algorithmic Bioinformatics Conference
  Papers," *PLOS Comp Biol*, 2020.
- Vinkers, Tijdink & Otte, "Use of positive and negative words in scientific
  PubMed abstracts between 1974 and 2014," *BMJ*, 2015.
- Munzner, "A Nested Model for Visualization Design and Validation," *IEEE TVCG*,
  2009.
- Strunk & White, *The Elements of Style*.
- AJE and TAA figure-caption guidance.
