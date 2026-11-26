<div align="center">

<img src="assets/banner.svg" alt="Academic Humanizer: personalized editing for AI-assisted academic drafts, keeping your voice and every claim, number, and citation intact" width="860">

[![license](https://img.shields.io/badge/license-MIT-2f8f57?style=flat-square)](LICENSE)
&nbsp;![version](https://img.shields.io/badge/version-0.3.2-2f8f57?style=flat-square)
&nbsp;![skill](https://img.shields.io/badge/skill-papers_and_grant_proposals-1c1a15?style=flat-square)
&nbsp;![built by](https://img.shields.io/badge/built_by-NSF,_CAREER,_NIH_R01-555?style=flat-square)

</div>

## Fork note — Vietnamese adaptation / Bản tiếng Việt

This fork keeps the original English skill **unchanged** (root `SKILL.md`, v0.3.3,
byte-identical to upstream) and adds a Vietnamese adaptation in the [`vi/`](vi/) folder:

- [`vi/SKILL.md`](vi/SKILL.md) — skill `academic-humanizer-vi` **v0.3**: editing rules for
  Vietnamese academic and technical writing (papers, theses, technical reports) and
  tender / project proposals, derived from the framework of the original skill.
- [`vi/Danh-muc-dau-hieu-AI-VI.md`](vi/Danh-muc-dau-hieu-AI-VI.md) — catalogue of
  Vietnamese AI-writing tells (49 patterns: general, academic, translationese) plus
  protected exceptions that must not be "fixed" (legitimate hedging, normative passive
  voice, standardised terminology, decimal commas).
- Two term whitelists (technical fields; Chemistry–Medicine–Biology) and two variant
  files (by document type; by field — Chemistry / Medicine / Biology) live in `vi/`
  alongside the skill; since v0.3 the skill treats all of them as mandatory reading.

Status: Vietnamese catalogue and rules reviewed and approved through the project's
decision gates (G1 passed); corpus benchmarking (G3) is still to come.

## Install this fork (EN + VI skills)

With the skills CLI (requires Node.js). Type the repo name exactly, **including the
`-VN` suffix**:

```bash
# Vietnamese skill — Claude Code
npx skills add datbi201/academic-humanizer-VN --skill academic-humanizer-vi -a claude-code -g -y
# Vietnamese skill — OpenAI Codex
npx skills add datbi201/academic-humanizer-VN --skill academic-humanizer-vi -a codex -g -y
# Vietnamese skill — Google Antigravity
npx skills add datbi201/academic-humanizer-VN --skill academic-humanizer-vi -a antigravity -g -y
# English skill: same commands with --skill academic-humanizer
```

Update later with `npx skills update`, then start a new agent session. Manual
(ZIP) installation and a full Vietnamese guide: [HUONG-DAN-CAI-DAT.md](HUONG-DAN-CAI-DAT.md).

---

## Why we built this

Some of us write a lot of papers and grant proposals, and our team started using AI to help with
drafts. The problem is that AI-assisted drafts come out generic and verbose, with "In recent years..."
openers, inflated phrasing, and over-long sentences. They also drift from the author's own voice and
lose the precision scholarship depends on.

There are tools called "humanizers," but they are built for blogs and marketing. Run one on a paper or
an NSF proposal and it flattens the precision along with everything else. The careful wording academic
writing depends on is the first thing to go.

So we put together our own. To calibrate it, we had the AI compare its own drafts with our team's
accepted papers and funded proposals, and we went through the differences by hand. It is nothing fancy,
and it is not about gaming review, defeating detectors, or adding fake novelty. We wanted AI-assisted
drafts to read clearly and in the author's own voice, with the numbers, citations, and claims left
exactly as written.

## Ethics and disclosure

This is an editing aid for clarity and voice, calibrated to an author's own prior accepted work. It does
not generate findings, invent data, or change citations, and it is not designed to evade AI-use
detection. Using it does not remove your obligation to disclose AI assistance: always follow the
disclosure policy of the venue you submit to.

## See it work

> [!CAUTION]
> **Before** (a generic AI draft):
>
> In recent years, continual learning has attracted increasing attention and achieved remarkable
> success. However, existing methods still face crucial challenges. In this proposal, we propose a novel
> framework that leverages cutting-edge techniques to delve into these intricate problems, paving the way
> for a transformative paradigm that will revolutionize the field.

> [!TIP]
> **After** (clear, in the author's voice, with claims tied to evidence):
>
> Continual learning matters, but today's methods stay empirical and their principles are unclear. That
> limits reliability and progress. This proposal builds a principled framework on three fronts:
> adaptation, soft supervision, and cross-domain knowledge. We demonstrate it on autonomous driving and
> network management.

**More before/after passes** are in [`examples/before-after.md`](examples/before-after.md): a general
example, an NIH Specific Aims page, and a funded NSF CAREER summary.

---

## What it does

- **Sharpens clarity and voice:** trims generic AI phrasing ("paves the way", "extensive experiments", "to the best of our knowledge", "In recent years...", delve/underscore/tapestry, rule-of-three, very long sentences, em-dashes) and brings the draft closer to the author's own style.
- **Keeps claims tied to evidence:** no verb stronger than the data (`prove` → `show empirically`), and
  vague magnitudes become attributed ranges.
- **Leaves real scholarship alone:** evidence-tied hedging, passive voice where it fits, `we`,
  definitions, symbols, and every citation. It doesn't change a number or a reference.
- **Has a separate mode for grant proposals (NSF, NIH):** it keeps the vision a paper would trim, and
  spends most of the effort on the first pages, since that's what reviewers score.

## Install

```bash
git clone https://github.com/AIScientists-Dev/academic-humanizer ~/.claude/skills/academic-humanizer
```

It is a plain `SKILL.md` plus examples, so it also runs as a skill or system prompt for **Codex** and
**MorphMind**. Point your agent at `SKILL.md`.

## Use

```
/academic-humanizer
[paste a section, or point at main.tex]
# optionally: "match my voice from prior_paper.pdf; target venue: ICLR"
```

## Make it yours

The rules here reflect one group's voice. Fork the repo and adapt them to your own: point it at a few of
your past papers, keep the checks that fit your field, and adjust the rest. It is meant to be
personalized, not a one-size-fits-all filter.

## How it works

Six layers: general AI-tell catalog → academic-specific tells → preserve scholarly conventions →
claim↔evidence matching → voice/venue calibration → funding-proposal mode (NSF/NIH structure,
first-page primacy, claim↔feasibility). The audit→rewrite loop is defined in [`SKILL.md`](SKILL.md).

## References

Layer 6 distills the *stable* structure of NSF and NIH proposals. For current, binding requirements
(page limits, formatting, deadlines), consult the source:

- NSF: [Proposal & Award Policies & Procedures Guide (PAPPG)](https://www.nsf.gov/policies/pappg)
- NSF: [CAREER program](https://new.nsf.gov/funding/opportunities/career-faculty-early-career-development-program)
- NIH: [Write Your Application](https://grants.nih.gov/grants/how-to-apply-application-guide/format-and-write/write-your-application.htm) (Specific Aims, Significance, Innovation, Approach)

## Acknowledgments

- **[blader/humanizer](https://github.com/blader/humanizer)** (MIT). *Focus:* removing general
  AI-writing patterns for blog, casual, and encyclopedic text. This skill reuses its general AI-tell
  catalog (Layer 1) and extends it for academic prose.
- **[koaeraser/ARMS](https://github.com/koaeraser/ARMS)**. *Focus:* an autonomous pipeline for
  statistics/methodology research papers (idea → validated, revised manuscript). A complementary,
  broader-scope project that informed the claim-evidence and numerical-precision emphasis here.

This skill is the narrower piece: a single-purpose **editing pass** that sharpens clarity and matches
claims to evidence while preserving the author's scholarly voice.

## License

MIT.
