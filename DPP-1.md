# DPP-1: Non-Coin Governance and a Constitutionally Constrained Foundation Treasury

| | |
| :--- | :--- |
| **Description** | How DIN makes decisions, settles disputes, controls upgrades and spends its treasury |
| **Authors** | Abraham Nash (@abrahamnash) |
| **Discussions-To** | [link to the DPP-1 discussion issue] |
| **Status** | Draft |
| **Category** | Meta |
| **Created** | 2026-10-27 |

## Abstract

Today, InfiniteZero's decisions are made in the open by the core team, and on-chain community governance is planned for after mainnet. Before then, the project needs a clear direction for who decides what.

This DPP proposes separating five concerns:

1. **Protocol rules** → social consensus through the DPP process, with no token vote
2. **Network economics** → social consensus, with stake-weighted voting by DIN validators only to settle disputes
3. **Contract upgrades** → carried out by key holders, only for changes social consensus has agreed, with forking as the backstop
4. **Treasury spending** → a future legal Foundation, bound by its charter and founding principles
5. **Fee rate** → set by the community, not the Foundation

The guiding principle: decisions are made by discussion, and voting is a last resort for disputes that can't be settled socially. The aim is a "fast executive, slow constitution" model that is accountable, resistant to capture, and consistent with InfiniteZero's aim of a community-governed AI commons on Ethereum. This is a direction for discussion, not a specific implementation.

## Motivation

InfiniteZero describes itself as built on Ethereum, secured by validators, governed by the community, with models that belong to the commons. Those principles need a governance design behind them before real value is at stake. Without one, power concentrates by default, in whoever holds the keys or the most tokens.

Lessons from Ethereum and other protocols:

- **Ethereum does not use coin-weighted governance for protocol rules.** ETH gives no vote over upgrades. Protocol changes happen through off-chain social consensus (EIPs, client teams, node operators, users). A controversial upgrade can cause a chain split; no central authority can force it.
- **Ethereum does use stake-weighted voting, but only for proof-of-stake consensus.** Validators attest to blocks and finality with staked ETH. That gives them no power over protocol rules or treasury spending.
- **EIP-1559 burns the base fee** rather than routing it to the Ethereum Foundation, to keep Ethereum decentralised, reduce validator manipulation, give ETH intrinsic utility and offset issuance. Ethereum chose "protocol-owned value" over "corporate revenue".
- **Uniswap is a different model.** UNI → voting power → DAO → controls the treasury → can fund Uniswap Labs. ETH → no governance vote → no DAO treasury → no shareholder-like entity.
- **"Non-coin governance" is not "no concentration of power".** It means choosing a different basis for allocating power. Someone still holds the keys; the design question is how to distribute authority so no single group can capture the protocol.
- **A legal foundation can outlast its people.** Founders leave, developers move on, validators rotate, but a foundation's charter can persist. People are the governors; the foundation is the institution whose powers are constrained by rules.

How this proposal maps to InfiniteZero's principles:

| InfiniteZero principle | How this proposal implements it |
| :--- | :--- |
| Built on Ethereum | Inherits Ethereum's social-consensus model for protocol rules |
| Secured by validators | Staked, slashable validators verify the work, and settle disputes over network economics |
| Governed by the community | Decisions by open discussion through DPPs; fee rate set by the community |
| Models belong to the commons | The treasury funds development; models are public goods |
| Applications benefit | Shared models they can use, and possibly a share of fees |
| Foundation | A legally constrained steward, not the protocol's owner |

## Specification

| Layer | Responsibility | How it is decided |
| :--- | :--- | :--- |
| Protocol rules | Upgrades, standards, direction | Social consensus through DPPs |
| Network economics | Economic parameters that affect validators | Social consensus; disputes settled by stake-weighted validator vote |
| Contract upgrades | Carrying out agreed changes on-chain | Key holders (multisig with a time delay), only for agreed changes; forking as the backstop |
| Treasury spending | Deploying accumulated funds | Foundation, within its charter; major spending signed off by two chambers |
| Fee rate | How much users pay | Community, outside the Foundation |

### 1. Discussion first, voting as a last resort

- Every decision starts as open discussion, usually through a DPP.
- A proposal moves forward once no substantive objections remain (rough consensus, not unanimity).
- A vote is held only when there is a dispute, or a question that can't be settled by discussion.
- Who votes depends on what is disputed, as set out below.

### 2. Protocol rules → social consensus

- Anyone can propose a change through a DPP.
- Developers, researchers, validators, node operators, model owners, applications and users discuss it.
- There is no token vote on protocol rules.
- In the long term, multiple independent client implementations (today there is one, `dincli`), so no single team controls the software.

### 3. Network economics → social consensus, validators settle disputes

- DIN runs on Ethereum (today on Optimism), so block consensus is handled there.
- DIN's validators (auditors and aggregators) stake to verify training work and are slashed for misbehaviour, so they are directly exposed to the network's economics.
- Economic changes are agreed through discussion like any other DPP. If a dispute can't be settled, validators vote, weighted by stake.

### 4. Contract upgrades → directed by social consensus

- DIN's contracts are upgradeable, so whoever holds the upgrade keys can change them.
- Upgrades are carried out by a multisig with a time delay, and only for changes that social consensus has agreed through the DPP process.
- The contracts are open source. If key holders refuse an agreed change, or push one the community rejects, anyone can fork and redeploy.

### 5. Treasury spending → two chambers

- **Technical chamber:** recognised developers, researchers and client teams.
- **Network chamber:** validators and node operators, weighted by participation rather than token ownership.
- Major expenditures need sign-off from both chambers before the smart contract releases funds. If a chamber can't agree, it votes, with a two-thirds threshold.

### 6. The Foundation as legal steward

The Foundation is a future legal entity, still to be set up. Its charter should specify that it:

- exists solely to maintain and develop the protocol and its ecosystem;
- may use treasury assets only for purposes set out in its founding principles;
- cannot alter the protocol's rules on its own;
- cannot sell or compromise the protocol's intellectual property;
- has directors selected and replaced through defined governance;
- needs multiple independent parties to authorise major transactions;
- follows predetermined rules for dissolution and asset transfer;
- has constitutional constraints that are difficult to change.

### 7. Fee rate → community governance

- The fee rate is set outside the Foundation (for example, 0.5%).
- Fee revenue flows automatically to the Foundation's treasury, to be issued for development and ecosystem purposes as its charter sets out.
- The Foundation cannot change the fee rate.
- Applications could also earn a share of fees, although their main benefit is the shared model itself, which they can use in their own products.

### 8. Capture prevention

- Term limits and rotating membership for governance representatives
- Quorum requirements for any vote
- Time delays on large withdrawals and on contract upgrades
- Veto and challenge periods
- Limited emergency powers that expire automatically
- Transparent on-chain accounting
- No single entity receiving a dominant share of funding

## Rationale

- **Discussion before voting.** Votes count preferences; discussion improves proposals. Settling most decisions socially, and voting only on genuine disputes, keeps decisions well reasoned and stops governance from becoming a contest of numbers.
- **Social consensus for rules.** Following Ethereum, rule changes should not be bought. Open discussion through DPPs, with forking as the final check, keeps the protocol accountable to the people who use it.
- **Validators settle economic disputes.** Validators bear the cost of bad economic parameters through their stake, so they should have the deciding say when economics can't be agreed. Limiting their vote to economic disputes stops stake from becoming control over the protocol's rules or treasury.
- **A Foundation bound by founding principles.** Fees routed to the Foundation fund development and the ecosystem. The principles may be subjective, but written founding articles give lasting guidance and guard against the project drifting from a reasonable set of principles because of any one person's interpretation.
- **Separating fee-setting from fee-spending.** If the Foundation could set its own revenue rate, it would have a reason to raise fees. Letting the community set the rate removes that conflict.
- **Fast executive, slow constitution.** A small team can act quickly in emergencies, with limited powers that expire, while changes to the charter stay deliberately hard.

## Backwards Compatibility

Nothing changes for deployed contracts or current participants. Today, the deployer key controls contract upgrades and the core team makes decisions in the open. This DPP sets the direction for moving away from that, starting with putting upgrade keys behind a multisig with a time delay.

Stake-weighted validator voting is limited to disputes over network economics. It does not change the principle that DIN does not use coin voting for protocol decisions.

The on-chain fee router already sends a capped share of fees (at most 20%) to a treasury, alongside the validator pool, storage and public goods. Under this proposal, the Foundation would become the steward of that treasury.

## Security Considerations

- **Upgrade key compromise.** A single deployer key controls every contract today. A multisig with a time delay limits the damage from one stolen key and gives the community time to react.
- **Stake concentration.** A few large validators could dominate a stake-weighted vote. Limiting that vote to economic disputes, and requiring a quorum, reduces the impact.
- **Sybil attacks on the chambers.** Membership of the treasury chambers needs objective criteria, so one party can't fill a chamber with identities it controls.
- **Foundation capture.** A charter that is hard to change, multiple signers on major transactions and transparent accounting limit what any group of directors can do.
- **Abuse of emergency powers.** Emergency powers must be narrow and expire automatically.

## Open Questions

1. Which economic parameters count as "network economics", and what counts as a dispute that triggers a validator vote?
2. How are Foundation directors appointed and replaced?
3. What are the objective criteria for membership of the technical and network chambers?
4. What are the exact thresholds for treasury withdrawals?
5. What emergency powers should the Foundation have, and when do they expire?
6. How can the community trigger the removal of a director without destabilising the Foundation?
7. Should the fee rate be capped, to prevent governance capture?
8. Should the Foundation's operating budget be a share of fees, or set independently with excess fees held in reserve?
9. Who holds the contract upgrade keys before the Foundation exists, and how is that handed over?
10. How are forks and exit rights handled if a controversial change is proposed?
11. In which legal jurisdiction should the Foundation be set up?

## Next Steps

1. Discuss this DPP on its discussion issue.
2. Draft the founding principles and a constitutional charter for the Foundation.
3. Define how disputes are raised and how votes are run, as a follow-up DPP.
4. Move contract upgrade keys to a multisig with a time delay.
5. Implement an on-chain treasury with multisig control, time delays and transparent accounting.
6. Keep fee-setting separate from fee-spending in the protocol's economic design.
7. Publish all governance documents for community review.

## References

**Ethereum**

- EIP-1, the EIP process: https://eips.ethereum.org/EIPS/eip-1
- Proof of stake: https://ethereum.org/developers/docs/consensus-mechanisms/pos/
- Attestations: https://ethereum.org/developers/docs/consensus-mechanisms/pos/attestations/
- Gasper: https://ethereum.org/developers/docs/consensus-mechanisms/pos/gasper/
- EIP-1559: https://eips.ethereum.org/EIPS/eip-1559

**InfiniteZero**

- GitHub organisation: https://github.com/InfiniteZeroFoundation
- DevNet: https://github.com/InfiniteZeroFoundation/DevNet
- White Paper: https://github.com/InfiniteZeroFoundation/White-Paper

**For contrast**

- Uniswap governance: https://uniswap.org/governance
