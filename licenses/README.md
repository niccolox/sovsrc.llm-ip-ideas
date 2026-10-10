# Sovereign Source Super Intellectual Property Licensing

The proposed **Sovereign Source Super Intellectual Property License (SS-SIP-0.1)** combines source sharing with required attribution and documented influence notices. A separate, opt-in marketplace agreement supplies syndicate representation, commercial orders and **SIP Creator Rewards**. Creators can receive credit, track earnings and receive payouts from agreed services and contribution use while preserving public license freedoms.

## Documents and status

| Document | Purpose |
| --- | --- |
| [SS-SIP license v0.1](SS-SIP-0.1.md) | Reusable license draft with covered-file source sharing, attribution, influence records and correction/enforcement terms |
| [Syndicate marketplace terms v0.1](SYNDICATE-MARKETPLACE-TERMS-0.1.md) | Separate participation and transaction terms covering authority, orders, rewards, payouts, appeals and exit |
| [Attribution example](templates/ATTRIBUTION.example.json) | Synthetic record showing contributors, documented influences, unknowns and source references |
| [Marketplace order example](templates/MARKETPLACE_ORDER.example.json) | Unaccepted synthetic order showing required fields and the $2,000 allocation example |

The license and marketplace terms are **drafts for qualified legal review**. SS-SIP-0.1 is intended to satisfy open-source principles, but no OSI approval, SPDX-list inclusion, compatibility determination or court-tested enforceability is claimed. `LicenseRef-SS-SIP-0.1` is a local custom identifier. These drafts have not been applied wholesale to this repository; an authorized holder must identify the material being licensed. Existing source references and Nemotron retain their applicable terms.

## How the license works

Anyone receiving properly licensed material can use, study, modify, redistribute and commercialize it. Distribution of covered files and their modifications carries a source-sharing requirement. Independent components keep their own licenses. Recipients retain public grants when a listing disappears or a syndicate changes membership.

Distributors must preserve relevant credit records and identify specific influences they know they relied upon in covered modifications. The obligation is bounded by actual knowledge and identifiable evidence; it does not require reconstructing every influence on a person's thinking or every training source behind a model. AI can propose evidence for human review. It cannot invent an origin or award a royalty.

Ordinary attribution files and documentation are sufficient. There is no mandatory advertising, splash screen, online registry, proprietary metadata format, usage telemetry or credit in every generated sentence. Attribution records cannot smuggle in extra restrictions. Source availability, notices and correction behavior must be reviewed together before adoption.

The draft provides a specific notice-and-cure process and termination of the affected grant for uncured material breaches. Actual remedies depend on applicable law and authority to enforce the relevant rights. A syndicate operator or credited influence does not automatically acquire another person's enforcement rights.

## How the marketplace works

A syndicate enrolls selected contributions under accepted mandates, prepares a reviewed listing and agrees to an order with a buyer. The order records what is supplied, applicable permissions, attribution, acceptance criteria, price or revenue formula, beneficiary splits, fees, adjustments and dispute terms. The Rust core verifies the accepted versions before fulfillment or accounting.

```mermaid
flowchart LR
    A[Contribution and authority review] --> B[Syndicate listing]
    B --> C[Versioned offer]
    C --> D[Required party acceptances]
    D --> E[Delivery and attribution receipt]
    E --> F[Qualified use or accepted delivery]
    F --> G[Earnings statements and payouts]
```

The public license does not require joining that flow. Paid offerings can include commissions, curation, support, hosting, distribution convenience and rights not already supplied by a public license. A seller must clearly disclose what a buyer can already obtain or do under open terms. Credits and market participation remain separate from legal ownership.

The proposed creator rewards pool is a contract option, not a mandatory license tax. A $2,000 distributable transaction with no administration fee can assign $1,200, $500 and $300 to agreed idea, implementation and influence beneficiaries. A credit-only influence receives acknowledgment without an amount owed.

## Creator rewards language

Use **SIP Creator Rewards** for the proposed contribution compensation program. An **eligible creator** is a contributor, rights holder or agreed beneficiary who satisfies the applicable agreement. **Qualified use** is an evidenced earning event under that agreement, including an accepted adoption or delivery where specified. The program rewards the participant's identified contribution while preserving upstream credits and permissions.

Present **estimated earnings** as provisional, **earned balances** as posted accounting entries with holds and adjustments visible, and **payouts** as payment events with an explicit status. A calculation is not proof of payment. In the local pilot, payout status must state that it is simulated. Calling compensation a reward does not make an accrued contractual obligation discretionary.

The language takes inspiration from X's focus on creators, originality, eligibility and payouts in its [Original Content Rewards overview](https://help.x.com/en/using-x/original-content-rewards), reviewed October 10, 2026. SIP defines its own contribution and agreement model; it is independent of X. This adaptation does not adopt X's subscription requirements, impression metrics, content rules or payment schedule.

## Applying the drafts

1. Have an authorized holder identify the exact files, works or versions it can license and any excluded upstream components. Complete the application notice in license section 15; do not invent a holder or infer authority from a project name.
2. Supply the license, an accurate Attribution Record and the required Source Form. The JSON example is optional; an equivalent readable format is allowed. Mark missing provenance honestly and keep confidential evidence out of public notices.
3. Review compatibility before combining covered modifications with differently licensed code, data or models. A custom license cannot overwrite an upstream license.
4. For optional commerce, identify the real operator and parties, complete the marketplace schedule and obtain every required acceptance. A template, invitation or AI-generated proposal is not a contract acceptance.
5. Review the custom attribution/influence duties, source-sharing scope, termination provisions, cross-border enforceability and marketplace contracts with qualified counsel before adopting them for a release or real transaction. Consider formal OSI review if seeking that approval.

The unaccepted examples contain null identities, locations and legal choices deliberately. They must fail an execution/adoption gate until completed. They are not grants, invoices, mandates or payment instructions.

## Open source and legal design references

The Open Source Definition protects free redistribution, source access, modification, equal access and independence from a specific product or technology. Requiring marketplace royalties or an additional account agreement to exercise public software rights would conflict with that design. SS-SIP therefore places commercial obligations in separately accepted orders. [Open Source Definition](https://opensource.org/osd).

Formal OSI approval requires public review; a newly written license cannot confer that status on itself. The novel influence clause also needs compatibility and practical-compliance review, even though its intent is open source. [OSI license review process](https://opensource.org/licenses/review-process).

Apache 2.0 provides an established example of preserving attribution notices without using the notice file to change the license. MPL 2.0 provides an established source-sharing approach for covered files within a larger work. Those are comparison points, not claims that SS-SIP is the same license, approved by their stewards or compatible with them. [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0), [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/).

U.S. copyright distinguishes protected expression from underlying ideas, methods and systems. The marketplace therefore uses explicit contribution and compensation agreements for ideas and influences rather than asserting that a registration creates exclusive ownership. [Copyright Office Circular 31](https://www.copyright.gov/circs/circ31.pdf).

An open software license is only part of evaluating an AI system's openness. The OSI AI definition separately addresses the preferred form for modification, including parameters, code and data information. Applying SS-SIP to project code or an adapter does not by itself certify an entire model as open-source AI. [Open Source AI Definition](https://opensource.org/ai/open-source-ai-definition).

Nemotron's own license and notices continue to govern its covered upstream material. Any SS-SIP application to project additions must respect that scope; it cannot claim NVIDIA's weights or upstream data as newly owned SIP material. [NVIDIA Nemotron license](https://www.nvidia.com/en-us/agreements/enterprise-software/nvidia-nemotron-open-model-license/).
