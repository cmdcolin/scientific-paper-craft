# scientific-paper-craft

A skill for Claude Code that drafts and revises research and software-tool
papers. Each technique comes from a published source, listed under
[References](#references). Run
[anti-ai-writing-tropes](https://github.com/cmdcolin/claudish) afterward to
catch generated-prose habits.

## Big ideas

The numbers and tools in the examples below are placeholders.

### Put the new fact at the end of the sentence

Readers look at the start of a sentence for context and at the end for the
point (Gopen & Swan). Start with what the reader already knows, and end on the
new information.

| Before | After |
|---|---|
| Memory use falls by 40% when the index is built with the new settings. | With the new settings, the index uses 40% less memory. |

### Give every paragraph context, content and conclusion

A paragraph that opens on a result with no context reads as a list of facts
(Mensh & Kording). Open with the problem or what is known, give what you did or
found, and close with what it means. The same arc nests: the Introduction sets
context for the paper, and each Results subsection is its own arc.

Name the single central contribution before drafting. A paper with two central
claims reads as unfocused even when both are true.

### State the key idea and list the contributions

Peyton Jones suggests writing the key idea down in one sentence before
drafting, and stating it plainly in the Introduction. Then list the
contributions as claims, each of which the paper substantiates:

> The main idea of this paper is to index alignments by region. We make three
> contributions: a file format (Section 3), a query algorithm (Section 4) and a
> benchmark against a full scan (Section 5).

Each claim points to the section that supports it, so a reader can check the
list against the paper. He also suggests putting related work at the end, which
a venue's convention may override.

### Replace a hype word with its evidence

Positive words in PubMed abstracts rose 880% between 1974 and 2014 (Vinkers et
al.), and some journals tell authors not to use *novel*, *unique* or
*unprecedented*. Delete the adjective. If the sentence still makes the same
claim, the adjective was rhetoric, and a number or a figure is what makes the
reader reach the judgment.

| Before | After |
|---|---|
| We present a novel, efficient tool for indexing alignments. | The index answers a region query in 12 ms, against 3 s for a full scan. |

### Make each figure readable from its caption

A reader skims the abstract, figures and conclusions before deciding to read
(AJE). Write the caption as a one-line title, the minimum needed to read the
figure, then one sentence with the result. Label axes and encodings in the
figure, so no reader opens Methods to decode them.

| Before | After |
|---|---|
| Figure 3: Benchmark results. | Figure 3: Query time against region size. Each point is the median of 20 runs; the blue line is the indexed query. Query time grows with region size for the scan and stays flat for the index. |

### Cut words that carry no information

Strunk & White: "vigorous writing is concise." Cut a clause that informs
nothing, and keep the connectives that let a sentence parse, or the result reads
as stilted instead of short.

| Before | After |
|---|---|
| It should be noted that the index was found to be smaller than the scan output. | The index is smaller than the scan output. |

### Write Methods a reader can rerun

A Methods section, read with its cited references, has to let a reader repeat
every procedure (Romano & Moore). Give versions, parameters and hardware at the
precision a benchmark needs, and tie each reported number to a named run. A
clause that explains why you rejected an alternative is a justification. Move it
to the Discussion with evidence, or cut it.

### Order the Discussion: findings, prior work, limitations, speculation

State the key findings, place them against prior work to locate the novelty,
state limitations, then speculate (Annesley). Speculation after limitations
reads as informed by them. The Discussion introduces no new data or citations.

### Attribute each visualization claim to one level

A visualization contribution sits at one of four levels: the domain situation,
the data and task abstraction, the encoding and interaction idiom, or the
algorithm (Munzner). A rendering benchmark is a level-4 result, and it does not
justify a level-3 design choice. A flaw at one level carries down to the levels
below it.

### Revise in a fixed order

Check structure first, then sentence flow, then a hype sweep, then captions,
then Methods, then the Discussion. Fixing sentences before structure polishes
paragraphs the paper may cut.

## Install

As a plugin:

```
/plugin marketplace add cmdcolin/scientific-paper-craft
/plugin install scientific-paper-craft@scientific-paper-craft
```

Or copy the skill into your personal skills directory:

```sh
git clone https://github.com/cmdcolin/scientific-paper-craft
cp -r scientific-paper-craft/skills/scientific-paper-craft ~/.claude/skills/
```

Claude loads the skill when its description matches the task, or when you ask
for it by name, e.g. "revise this manuscript with the scientific-paper-craft
skill".

## References

- Gopen & Swan, ["The Science of Scientific Writing,"](https://www.jstor.org/stable/29774235)
  *American Scientist* 78(6):550-558, 1990: topic and stress position.
- Mensh & Kording, ["Ten Simple Rules for Structuring Papers,"](https://doi.org/10.1371/journal.pcbi.1005619)
  *PLOS Comput Biol* 13(9):e1005619, 2017: the context-content-conclusion arc
  and the single central contribution.
- Romano & Moore, ["Ten Simple Rules for Writing a Paper About Scientific Software,"](https://doi.org/10.1371/journal.pcbi.1008390)
  *PLOS Comput Biol* 16(11):e1008390, 2020: reproducibility in software papers.
- Medvedev, ["Ten Simple Rules for Writing Algorithmic Bioinformatics Conference Papers,"](https://doi.org/10.1371/journal.pcbi.1007742)
  *PLOS Comput Biol* 16(4):e1007742, 2020.
- Annesley, ["The Discussion Section: Your Closing Argument,"](https://doi.org/10.1373/clinchem.2010.155358)
  *Clin Chem* 56(11):1671, 2010: limitations in the Discussion.
- Vinkers, Tijdink & Otte, ["Use of positive and negative words in scientific PubMed abstracts between 1974 and 2014,"](https://doi.org/10.1136/bmj.h6467)
  *BMJ* 351:h6467, 2015: growth in positive words.
- [*J. Org. Chem.* author guidelines](https://researcher-resources.acs.org/publish/author_guidelines?coden=joceah),
  American Chemical Society: the list of words to avoid.
- Munzner, ["A Nested Model for Visualization Design and Validation,"](https://doi.org/10.1109/TVCG.2009.111)
  *IEEE TVCG* 15(6):921-928, 2009: the four levels.
- AJE, ["Writing an Effective Figure Legend,"](https://www.aje.com/arc/writing-effective-figure-legend):
  caption structure.
- Tufte, *The Visual Display of Quantitative Information*, Graphics Press, 1983.
- Peyton Jones, ["How to write a great research paper,"](https://www.microsoft.com/en-us/research/academic-program/write-great-research-paper/)
  Microsoft Research: the key idea, the contribution list and related work.
- Strunk & White, *The Elements of Style*: active voice and concision.
