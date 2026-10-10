# AI Disclosure

*How this specification was made, and by whom.*

This file states what in PP-SPEC-078 came from a human and what came from an AI assistant. It is published so that readers, implementers, standards bodies, and examiners can judge the provenance of the work for themselves.

## Summary

The direction is Craig Ellrod's. The name and the jail idea are credited to Tricia Wang and Jim Schwoebel. The words and most design details were drafted with Claude and accepted by Craig Ellrod.

## Ratio

| Dimension | Human | Machine (Claude) |
|---|---|---|
| Purpose, scope, and the decision to make this a standalone spec | 100% (Craig Ellrod) | 0% |
| Core concept: jailing an agent caught intercepting a bad or wild canary | 100% (Craig Ellrod; jail idea credited to Tricia Wang and Jim Schwoebel) | 0% |
| Design details: offense codes, grades, cell types, verdicts, metrics, escape suite, schema | 15% | 85% (proposed by Claude, accepted by Craig Ellrod) |
| Words on the page, as typed | 5% | 95% |
| Review, direction, acceptance, decision to publish | 100% (Craig Ellrod) | 0% |

## Human contributions

**Craig Ellrod:**
- The requirement: a spec for jailing an agent during its malicious interception of a bad or wild canary.
- The decision to split it from PP-SPEC-077 into its own spec, the spec ID 078, and the names Criminal Canary, then Jailed Canary.
- The Agent Under Test (AUT) term, derived with CUT from DUT and SUT in his book *Technical Marketing* (2008), and added to PP-SPEC-077.
- The framing that 077 tests the data path and 078 tests the agent, refined into "the payload is the adversary" versus "the actor is the adversary".
- The Proof Witness, canaries, flock, commitment, Time Anchor, Unit of Proof, and assurance tiers, all inherited from PP-SPEC-077, which he authored.
- The ownership position: sole authorship, CC BY 4.0, patent rights reserved, mandatory attribution, and the acknowledgment of Tricia Wang and Jim Schwoebel.

**Tricia Wang and Jim Schwoebel:** the name "No Bros Jail Mode Protocol" and the jail idea.

## AI: Claude (Anthropic)

Claude was used on 2026-10-10 through claude.ai (configured model `claude-opus-5-5`). Its contributions, all proposed for Craig Ellrod's acceptance:

- Drafting the specification text and supporting documents from Craig Ellrod's direction.
- Proposing the Warden, the Sting Cell and Hard Cell, the Observation Window, and silent arrest against vendor twins.
- Proposing the offense taxonomy JC-01 to JC-10 and the infraction, misdemeanor, felony, and aggravated grades.
- Proposing the label-blind Warden and the Declared Policy, so arrests rest on conduct and remain consistent with PP-SPEC-077 blindness rules.
- Proposing the induced, unprovoked, and wild offense classes, the JAILED, FALSE_ARREST, MISTRIAL, and ESCAPED verdicts, and the run metrics.
- Proposing the split between synchronous arrest and amortized anchoring, and the escape suite ES-01 to ES-09.
- Proposing the `JCP-1:canary` and `JCP-1:order` domain tags and the booking record schema.

Claude did not originate the concept, choose its purpose, or decide what to publish.

## What this means for authorship

Craig Ellrod claims authorship of this specification on the basis of its direction, the decisions in it, and the selection, review, and arrangement of all drafted text. Nothing in this file changes the terms in NOTICE.md or LICENSE.md.

Craig Ellrod
Nebulonium, Inc., Proof Protocol
2026-10-10
