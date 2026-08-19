# Peace Intel — Style Review

Static design prototype for internal review. Not for distribution. No build step; every page
is a single self-contained HTML file.

## Pages

| | |
|---|---|
| [Landing](https://thatmattgillespie.github.io/peaceintel-style-review/) | General landing page, with an audience routing strip at `#who` |
| [Who it's for](https://thatmattgillespie.github.io/peaceintel-style-review/audiences.html) | The audience page. Opens on a chooser, then reveals one of five versions |
| [Problem statements](https://thatmattgillespie.github.io/peaceintel-style-review/problems.html) | All five problem statements on one sheet, for user interviews |

## How the audience page works

It opens on a fill-in-the-blank sentence — *"I work at ⌄a funding organization as a ⌄senior
leader."* — and reveals the matching version once both blanks are filled. Five combinations,
because practitioners exist on the implementer side only:

| | Senior Leadership | Program Managers | Practitioners |
|---|---|---|---|
| **Funding organization** | ✓ | ✓ | — |
| **Implementing organization** | ✓ | ✓ | ✓ |

Every state is a shareable URL, and **any link carrying both parameters skips the chooser**:

```
audiences.html?v=funders&role=senior-leadership
audiences.html?v=implementers&role=practitioners
```

`?v=` on its own opens the chooser with the organisation already filled in. The old
`funders.html`, `program-managers.html` and `practitioners.html` URLs still work; they redirect
to their equivalent state, so links already shared stay good. Note that the old
`program-managers.html` was written for the funder side, so it lands on Funders → Program
Managers.

Hero, subhead, problem statement and closing CTA change per state; the use-case cards change
per side. Everything else is shared.

## Notes for reviewers

- Type is DIN 2014 (self-hosted from `Fonts/`), Nanum Myeongjo, and Space Mono.
- The use-case card graphics are static stills built in HTML/CSS from the real app components.
  They are not screenshots and not interactive.
- The problem cards are drawn from the Jobs-to-be-Done audit. Two of the five audiences
  (implementer leadership and implementer program managers) have no rows in that audit yet, so
  those cards are written from the nearest jobs — `problems.html` labels which is which.
- `toggle-lab.html` is a design record of the audience-toggle alternatives explored before the
  chooser replaced them. It is not linked from the site.

## Open

- **Corpus stats.** The landing page still shows an older set of numbers than the audience page.
  The July 31 library metrics match the audience page; the landing page needs updating, pending
  a decision on whether to lead with one number instead of five.
- **Copy.** The AI-specific language ("corpus", "LLM agent", "machine-readable") is inventoried
  and awaiting a rewrite.
