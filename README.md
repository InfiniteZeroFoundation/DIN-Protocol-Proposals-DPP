# DIN Protocol Proposals (DPPs)

DIN Protocol Proposals (DPPs) are how changes to the Decentralized Intelligence Network (DIN) are proposed, discussed and agreed. A DPP is a design document: it describes a change, explains why it is needed, and records how the community reached its decision.

The process is modelled on Ethereum's Improvement Proposals ([EIP-1](https://eips.ethereum.org/EIPS/eip-1)).

## How decisions are made

DIN is governed by social consensus, not coin voting.

- **Discussion comes first.** Most proposals are settled in the open: people raise concerns, the author revises, and the proposal moves forward once no substantive objections remain. This is rough consensus, not unanimity.
- **Voting is a last resort.** A vote is held only when there is a dispute, or a question that can't be settled by discussion. How disputes are settled, and who takes part, is being defined in DPP-1.
- **Tokens don't buy control of the rules.** Holding tokens gives no say over protocol rules. Validators, who have stake at risk, may have a stake-weighted say in disputes over network economics, as proposed in DPP-1.
- **Anyone can take part.** You don't need permission, tokens or a title to propose or comment.
- **Exit is always possible.** All DIN code is open source. If the community rejects a direction, anyone can fork.

Editors don't judge whether a proposal is a good idea. They check that it is complete, clearly written and follows this process.

When a discussion needs wider or more structured input, we may use tools such as [Polis](https://pol.is/home), which maps where people agree and disagree, or [gov4git](https://github.com/gov4git/gov4git), which records votes transparently in Git. These are options, not requirements.

## Categories

| Category | Covers |
| :--- | :--- |
| **Core** | Protocol rules: smart contracts, training rounds, scoring, slashing, rewards, and security and privacy mechanisms |
| **Interface** | Standards for working with DIN: CLI and SDK behaviour, APIs, data formats, model packaging and node communication |
| **Economics** | Network economic parameters: fees, emissions, stake requirements, reward splits and penalties |
| **Meta** | How DIN is governed and run: this process, governance, the treasury and the Foundation |
| **Informational** | Guidelines, research and best practice that don't change the protocol |

Core and Interface DPPs need a reference implementation before they can become Final.

## Lifecycle

```
Idea → Draft → Review → Last Call → Final
```

| Status | Meaning |
| :--- | :--- |
| **Idea** | Not yet a DPP. Discuss it first in [DevNet Discussions](https://github.com/InfiniteZeroFoundation/DevNet/discussions) or on [Telegram](https://t.me/+h46VS3AnO384ZGI8) to test interest and find collaborators. |
| **Draft** | Merged into this repository and open for discussion and changes. |
| **Review** | The author considers it ready and asks for wider review. |
| **Last Call** | The final review window, normally 14 days. A substantive objection sends it back to Review. |
| **Final** | Agreed. Only corrections are made after this point. |
| **Living** | Kept up to date indefinitely, such as a process document. |
| **Stagnant** | No activity for 6 months while in Draft or Review. The author, or anyone else, can revive it. |
| **Withdrawn** | Withdrawn by the author. The number is not reused. |
| **Rejected** | The community decided not to proceed. The reasons are recorded in the DPP. |

A Final DPP is an agreement, not a deployment. Changes reach the network through the normal release process in [DevNet](https://github.com/InfiniteZeroFoundation/DevNet).

## How to submit a DPP

1. **Discuss the idea first** in [DevNet Discussions](https://github.com/InfiniteZeroFoundation/DevNet/discussions) or on [Telegram](https://t.me/+h46VS3AnO384ZGI8).
2. **Open a discussion issue** in this repository titled `DPP discussion: <title>`. The conversation about your proposal lives there.
3. **Write your DPP** using the template below, in a file named `DPP-<number>.md`. Use the next free number in the [DPP Index](./DPP-Index.md); an editor confirms it during review.
4. **Open a pull request** that adds your DPP and its row in the DPP Index. If you aren't a maintainer, fork this repository first.
5. **An editor checks it and merges it as Draft.** Discussion continues on the issue.
6. **Move it forward.** When it is ready, open a pull request that updates its status.

## Roles

- **Authors** write the DPP, gather feedback, keep it up to date, and record the objections raised and how they were resolved.
- **Editors** check format and completeness, confirm numbers, and merge status changes. They don't decide on merit. Until community editors are appointed, the core maintainers act as editors.
- **The community** is anyone who reads, comments on, tests or reviews a proposal.

## DPP template

```markdown
# DPP-<number>: <Title>

| | |
| :--- | :--- |
| **Description** | One sentence on what this proposes |
| **Authors** | Name (@github-handle) |
| **Discussions-To** | Link to the discussion issue |
| **Status** | Draft |
| **Category** | Core / Interface / Economics / Meta / Informational |
| **Created** | YYYY-MM-DD |
| **Requires** | (Optional) Numbers of DPPs this depends on |

## Abstract

A short summary of the proposal, in about 200 words.

## Motivation

The problem this solves, and why it matters now.

## Specification

Exactly what changes. For Core and Interface DPPs, enough detail for someone to implement it.

## Rationale

Why this design, which alternatives were considered, and which objections were raised and how they were resolved.

## Backwards Compatibility

What this changes for existing participants, contracts and tools, and how to migrate. Write "None" if nothing changes.

## Security Considerations

The risks this introduces or removes: attacks, failure modes, privacy and economic manipulation. Required for every DPP.

## Reference Implementation

(Optional while in Draft; required before Final for Core and Interface DPPs.) Links to code, pull requests or tests.

## References

(Optional) Related DPPs, research and documents.
```

## Get involved

- [DPP Index](./DPP-Index.md): every proposal and its status
- [DevNet](https://github.com/InfiniteZeroFoundation/DevNet): the protocol's code
- [DevNet Discussions](https://github.com/InfiniteZeroFoundation/DevNet/discussions): ideas and questions
- [White Paper](https://github.com/InfiniteZeroFoundation/White-Paper)
- [Telegram](https://t.me/+h46VS3AnO384ZGI8)

Questions about the process? [Open an issue](https://github.com/InfiniteZeroFoundation/DIN-Protocol-Proposals-DPP/issues).
