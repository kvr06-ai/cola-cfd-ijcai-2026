# COLA Manipulation Bound — IJCAI-ECAI 2026 CFD Workshop Submission

Workshop submission of the COLA manipulation-bound paper to the **4th IJCAI Workshop on Computational Fair Division** (CFD), co-located with IJCAI-ECAI 2026 in Bremen, Germany (August 15-17, 2026).

## Status

- **Paper:** 5 pages of content + 1 page references, IJCAI-ECAI 2026 format, two-column.
- **Compiles via** `tectonic` cleanly (no errors, no overfull boxes).
- **Authors:** Timothy Highley (La Salle University), Kaushik Rajan (Independent).
- **Workshop policy:** non-archival, single-blind (author names allowed).
- **Submission system:** OpenReview at https://openreview.net/group?id=ijcai.org/IJCAI-ECAI/2026/Workshop/CFD
- **Deadline:** May 9, 2026 AoE (per CFP; verify before submitting — May 4 / May 9 dates were both visible on the page).

## Build

```sh
cd paper
tectonic main.tex
```

Outputs `main.pdf`. The `\pdfinfo` block is guarded with `\@ifundefined` so the document compiles under XeTeX-based engines (tectonic) as well as pdftex; the official IJCAI workflow uses pdftex which honors the directive.

## Layout

```
paper/
  main.tex         # Single-file paper, IJCAI-ECAI 2026 format
  references.bib   # 7-entry bibliography
  ijcai26.sty      # IJCAI 2026 style file (vendored)
  named.bst        # IJCAI 2026 BibTeX style (vendored)
  figures/         # Figures referenced from the paper
README.md
.gitignore
```

## Relationship to the WIP paper

The workshop submission is a peeled, fair-division-flavored version of the longer WIP paper at `../../wip-papers/cola-manipulation-bound/`. Compressed from 23 pages single-column to 5 pages two-column; emphasises:

- The fair-division angle via Coreno-Balbuzanov axioms (RP, EF1, SP).
- The closed-form manipulation bound (~4%).
- The Capped COLA per-series lemma (a fresh contribution from our work).
- A brief empirical validation via the cap sweep table.

Cuts that didn't fit the 7-page limit:
- Detailed historical NBA lottery context.
- All three case studies (SAC, PHI Process, MIL Countdown) from the WIP paper.
- Trade-handling section (4 trade rules × 4 cells).
- Lottery-day attribution discussion.
- Three-closures-of-the-pool-manipulation-gap framing.

## Workshop submission policy notes

- **Non-archival:** dual submission to a venue like SAGT 2026 / WINE 2026 is permitted.
- **Single-blind:** author names visible to reviewers.
- **Line numbers required for review** (the `\linenumbers` command is uncommented).
