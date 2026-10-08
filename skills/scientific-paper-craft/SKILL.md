---
name: scientific-paper-craft
description: Structure and revision techniques for scientific and software-tool papers, drawn from published writing guidance. Covers the central contribution, paragraph arcs, sentence stress, hype words, figure captions, evidence for tool claims, Discussion order and visualization-paper framing. Use when drafting or revising a manuscript, planning a revision pass, or reviewing a paper's organization. Run anti-ai-writing-tropes after this one.
---

# Scientific paper craft

Techniques for drafting and revising a research or software-tool paper, each
with its source. Where a project's own style rules conflict with anything here,
the project's rules win.

## Central contribution

Mensh & Kording rule 1: focus the paper on one contribution and communicate it
in the title. "Papers that simultaneously focus on multiple contributions tend
to be less convincing about each." Medvedev rule 1 asks for the main novel
contribution stated clearly and succinctly.

- Write the key idea in one sentence before drafting (Peyton Jones), and state
  it in the Introduction: "The main idea of this paper is ...".
- List the contributions as claims, and point each claim to the section that
  supports it. Medvedev rule 5: the rest of the paper supports every claim in
  the Introduction.
- Place related work where the venue's convention puts it (Peyton Jones
  suggests the end).
- Credit precisely. Say what you took from prior work: the evidence that an
  approach works, the idea, or the code. "Following X's example" tells the
  reader the implementation derives from X. When it was independent, write what
  happened: "X's success with Y inspired this work, which we implemented
  independently."
- Keep the Introduction short and anchor every sentence. Peyton Jones puts the
  problem and the contributions on the first page. Cite your own prior release
  at its first mention, cite the datasets that document the need, and give the
  field gap in a peer's words with a citation.

## Paragraph arcs

Mensh & Kording rule 3, context-content-conclusion. The context sets up the
story, the content advances it, and the conclusion resolves it.

- The arc nests. The abstract holds all three parts, with the knowledge gap as
  context, the methods and results as content, and the interpretation as
  conclusion. The Introduction narrows from the field to the gap. Each Results
  paragraph opens with the question it answers and ends on its conclusion.
- Rule 4: keep each paragraph on one topic, and give parallel ideas parallel
  structure.
- End every sentence that states a fact on its consequence ("so its redraw time
  grows with the reads in view"), or open the next sentence on the cause. When
  the cause is your own work, say so: "because we put our optimization work
  into the parsers".
- Keep parallel items at one level of detail. A general list stays general, and
  the specific example goes in Results.

## Sentence stress

Gopen & Swan: "Put in the topic position the old information that links
backward; put in the stress position the new information you want the reader to
emphasize." The topic position is the start of a sentence, and the stress
position is its end.

- Start a sentence with what the reader already knows, and end it on the new
  fact.
- Name the subject in topic position, so the reader has something to link to.
- When new information lands in a stress position that nothing later uses,
  check for a logical gap.

## Hype words

Positive words in PubMed abstracts rose 880% from 1974 to 2014 (Vinkers et
al.). The *J. Org. Chem.* author guidelines list *convenient, efficient, elegant, expedient, facile, first, new, novel,
practical, simple, unique, unprecedented* and *versatile* as words to leave out.
Add *powerful, crucial, groundbreaking, robust, innovative* and
*transformative*.

Delete the adjective. If the sentence still makes the same claim, the adjective
was rhetoric. Where the claim needs support, give the number that lets the
reader reach the judgment.

## Figures and captions

AJE's figure-legend guide: a caption lets the reader interpret the figure
without the main text.

- Open with a title that says what the figure shows, add only the methods needed
  to read it, state the result, then define the features.
- Label panels, axes and encodings in the figure or caption, so the reader
  decodes an axis without opening Methods.
- Give each figure one message. A figure that supports two claims may be two
  figures.

## Evidence for tool claims

- Medvedev rules 6 and 7: a paper needs a strong theoretical contribution or an
  experimental evaluation, and it compares against other work. A method that
  seems obviously better still gets the comparison.
- Medvedev rules 9 and 10: describe the algorithm precisely, verify its
  correctness in the experiments, and analyze running time or memory.
- Romano & Moore: evaluate on high-quality data that is ideally already well
  characterized, and cite the release the paper describes with its own DOI.
  Rule 8: keep the code, the documentation and the paper consistent.
- Give versions, parameters and hardware at the precision a reader needs to
  repeat each number, and tie each number to a named run.
- Put the reasons for rejecting an alternative in the Discussion with evidence.
  Methods describes what you did.

## Discussion order

Mensh & Kording rule 8: discuss how the gap was filled, the limitations of the
interpretation, and the relevance to the field. Annesley also puts limitations
in the Discussion. Order the section as findings, prior work, limitations, then
speculation, so that the speculation reads as informed by the limitations.

- Forward-looking claims belong here, built on findings Results supports.
- Every data point, citation and ratio in the Discussion appears earlier in the
  paper.

## Visualization papers

Munzner's nested model: a contribution sits at one of four levels, and each
level has its own validation.

1. Domain situation: the users and their problem.
2. Data and task abstraction: the operations and data types, independent of any
   visual design.
3. Encoding and interaction idiom: the marks, channels and interactions.
4. Algorithm: the implementation that computes or renders the idiom.

A mistake at a higher level carries down to the levels below it, so a slow
idiom, a level-4 symptom, can come from a level-2 abstraction mistake. Attribute
each claim to its level: a rendering benchmark is a level-4 result, and a
level-3 design choice needs level-3 evidence.

## Active voice and concision

Strunk & White: prefer the active voice, and "vigorous writing is concise."
Concision "requires not that the writer make all his sentences short ... but
that every word tell."

- Name the actor. In a software paper, say what the software does.
- Idiomatic passives ("is required") and passives whose actor does not matter
  are fine.
- Cut clauses that inform nothing. Keep the connectives (*so*, *because*,
  *which*) that join ideas and write full sentences. A long sentence whose
  clauses each carry information is fine.
- Define a term in a relative clause that says what it contains: "a walk that
  lists, in order, the nodes the haplotype passes through".

## Three-stance review

For a sentence that will not come right or a claim that carries the paper,
launch three fresh subagents, one per stance, on the same passage:

- an editor: clarity, idle words, copyedit flags, whether the next sentence
  follows
- a hostile referee: what they would write, which claim lacks support, the
  minimal change they would accept
- a skimming reader: where they stumble aloud, pronoun antecedents, term drift
  against neighbouring sentences, whether they keep reading

Each gets the passage with its neighbours, the project's rules, what the author
has already rejected, and exact questions. Each returns a verdict first, the
exact text in question and an exact replacement. Adopt what two of three agree
on and put the rest to the author. Run the referee first on anything with a
number. Sonnet-class models are enough.

To generate candidates, give a persona with a method: an editor reading the
whole abstract aloud, a PI writing by ear, a science writer listening for
cadence, each with the rejected list. Ask for ten, each with the following
sentence attached so the join is visible, and grade them yourself.

## Revision order

Revise a paragraph whole. The sentences of a paragraph were written to follow
one another, so rewrite it as a unit and then check the rules against the
result.

1. Structure: does the paper serve one contribution, does each section and
   paragraph have its arc, and does the abstract alone state the contribution?
2. Sentence flow: read each paragraph's sentence endings in sequence. Do they
   carry the new information?
3. Hype sweep: grep for the words above and any project word list. Cut each one
   or replace it with a measurement.
4. Captions: can each figure be read from its caption alone?
5. Evidence: could a reader rerun every number in Results from Methods as
   written, and does each Introduction claim have support?
6. Discussion: does every claim trace to something earlier in the paper?
7. Feedback: ask someone outside the project where they stopped understanding
   (Peyton Jones, Mensh & Kording rule 10), or run the three-stance review on
   the passages that carry the paper.

Run `anti-ai-writing-tropes` after this pass. It catches tics such as mannered
compression and comma-hung appositives, and applying the concision advice above
afterward would undo its fixes.

## Sources

- Gopen & Swan, ["The Science of Scientific Writing,"](https://www.jstor.org/stable/29774235)
  *American Scientist* 78(6):550-558, 1990.
- Mensh & Kording, ["Ten Simple Rules for Structuring Papers,"](https://doi.org/10.1371/journal.pcbi.1005619)
  *PLOS Comput Biol* 13(9):e1005619, 2017.
- Romano & Moore, ["Ten Simple Rules for Writing a Paper About Scientific Software,"](https://doi.org/10.1371/journal.pcbi.1008390)
  *PLOS Comput Biol* 16(11):e1008390, 2020.
- Medvedev, ["Ten Simple Rules for Writing Algorithmic Bioinformatics Conference Papers,"](https://doi.org/10.1371/journal.pcbi.1007742)
  *PLOS Comput Biol* 16(4):e1007742, 2020.
- Annesley, ["The Discussion Section: Your Closing Argument,"](https://doi.org/10.1373/clinchem.2010.155358)
  *Clin Chem* 56(11):1671, 2010.
- Vinkers, Tijdink & Otte, ["Use of positive and negative words in scientific
  PubMed abstracts between 1974 and 2014,"](https://doi.org/10.1136/bmj.h6467)
  *BMJ* 351:h6467, 2015.
- [*J. Org. Chem.* author guidelines](https://researcher-resources.acs.org/publish/author_guidelines?coden=joceah),
  American Chemical Society.
- Munzner, ["A Nested Model for Visualization Design and Validation,"](https://doi.org/10.1109/TVCG.2009.111)
  *IEEE TVCG* 15(6):921-928, 2009.
- AJE, ["Writing an Effective Figure Legend."](https://www.aje.com/arc/writing-effective-figure-legend)
- Peyton Jones, ["How to write a great research paper,"](https://www.microsoft.com/en-us/research/academic-program/write-great-research-paper/)
  Microsoft Research.
- Strunk & White, *The Elements of Style*.
