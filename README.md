# skill-factory-experiments

Three unrelated-domain Claude Code skills, built the same way, to test whether
a "knowledge → SKILL.md" pipeline generalizes instead of being a one-off
trick.

Each skill turns general/public domain knowledge (not a specific copyrighted
book or course) into a checklist-driven skill: core concepts, a numbered
procedure, a "things people miss" checklist, and a fixed output format that
refuses to guess when required information is missing.

## Skills

### real-estate-auction-analysis
Analyzes Korean court real-estate auction listings for encumbrances the
winning bidder would inherit — senior liens, tenants with priority claims,
unrecorded liens that only show up on a site visit. Built from general
Korean civil-procedure knowledge (law and procedure are not copyrightable),
not from any specific book. **Reference checklist, not legal advice** — see
the disclaimer in the skill itself.

Tested against a synthetic case with a tenant whose priority date predates
the senior lien: correctly flagged the missing fact (whether the tenant
filed a distribution claim) instead of guessing at the assumption amount.

### seo-longtail-keyword-strategy
Judges whether a keyword is winnable for a small/new site before you write
the post — head vs. longtail, search intent, competitor type, whether the
site has anything to differentiate on.

Tested against two real keywords from an actual blog's publishing history:
correctly rejected a keyword that failed in practice ("AI 회의록 정리법" —
already occupied by large outlets) and correctly approved a keyword that
the site had, independently, already published successfully the same day.

### smartstore-listing-optimization
Reviews an e-commerce product listing (title, image, detail page, price)
for exposure vs. conversion problems, and separately flags deceptive-
advertising risk (undisclosed paid/gifted reviews, guaranteed-effect
health claims).

Tested against a listing with both marketing weaknesses and a real
compliance violation (an unqualified "prevents a medical condition" claim):
correctly ranked the compliance risk above the marketing suggestions rather
than burying it in a flat list.

## Install

```
/plugin marketplace add qkrehgk1-wq/skill-factory-experiments
/plugin install real-estate-auction-analysis@skill-factory-experiments
/plugin install seo-longtail-keyword-strategy@skill-factory-experiments
/plugin install smartstore-listing-optimization@skill-factory-experiments
```

## Why free

These are experiments in a method (does the pipeline generalize), not
commercial products. No warranty, no support commitment — use, fork, adapt.

## License

MIT
