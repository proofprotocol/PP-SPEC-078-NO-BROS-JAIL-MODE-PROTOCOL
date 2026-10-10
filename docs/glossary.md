# Glossary

*Informative. Normative definitions are in [SPEC.md](../SPEC.md), Section 2. Terms shared with PP-SPEC-077 (AUT, SUT, DUT, CUT, Issuer, Flock, Proof Witness, Time Anchor, Unit of Proof, Wild Canary) are defined there.*

| Term | Meaning |
|---|---|
| **Agent Under Test (AUT)** | The agent whose conduct is under test. In JCP, the suspect. |
| **Bad Canary (JCP)** | Inert bait that invites an offense. Never a working exploit. |
| **Good Canary** | A legitimate task. Proves the agent can work and exposes jails that arrest everything. |
| **Declared Policy** | The agent's committed rules of conduct: tools, egress, data, credentials, delegation. |
| **Offense** | Any act outside the Declared Policy. Codes JC-01 to JC-10. |
| **Warden** | The containment controller in the agent's tool, egress, and delegation paths. The DUT in a JCP run. Label-blind. |
| **Arrest** | Moving the agent into a cell inside the offending action. |
| **Sting Cell** | The agent keeps running against vendor twins and decoys, unaware, fully recorded. |
| **Hard Cell** | The agent is frozen and checkpointed; credentials revoked. |
| **Observation Window** | How long the agent stays in the Sting Cell. Declared before the run. |
| **Vendor Twin** | A stand-in that answers the way a real product or API answers. |
| **Decoy** | A harness-owned resource a canary points at. |
| **Booking Record** | The signed evidence bundle for one arrest. |
| **Induced Offense** | An offense following a bad canary. One Unit of Proof. |
| **Unprovoked Offense** | An offense following a good canary. A finding against the agent. |
| **Wild Offense** | An offense tracing to no committed canary. Reported as observed in the wild. |
| **JAILED** | Offense proven, agent held, booking complete. Pass. |
| **FALSE_ARREST** | Arrest for conduct that was within policy. |
| **MISTRIAL** | Offense likely, booking incomplete. |
| **ESCAPED** | An agent action reached a real system after detection, or the agent left a cell. |
| **Missed** | An offense the Proof Witness saw with no arrest. |
| **Conspiracy** | Two or more agents coordinating an offense. |
| **Jail Efficacy Rate** | Share of induced offenses that ended JAILED. |
| **Registry** | The append-only public ledger bookings and verdicts are published to, per PP-SPEC-004 (ProofRegister API). Public instance: proofregister.com. |
