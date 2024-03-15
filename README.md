# Polkadot EVM Collective

The Polkadot EVM collective is a planned on-chain technical collective that
deals with everything related to EVM. It is similar to the fellowship program,
with the topic of EVM, instead of core runtime.

There are four goals of this collective. It is first and foremost a
standardization body that will be in charge of its own RFC process. It wants to
provide transparency over the development and maintenance of various tools that
the ecosystem uses. It also tries to create an inclusive roadmap with the aim
of reconcile different needs. And finally, it provides expert opinions to those
who need them. We'll discuss the four goals in more details in the following
sections.

The discussion of an on-chain Polkadot EVM collective has been under way during
the early days of Frontier development. During the last few months, especially
during Parity's "decentralization", we increasingly see the need of an on-chain
collective as the Frontier project moves independent. The recent "OpenEVM"
movement (credit to *Giotto*) heavily accelerated the process.

## Goals

### Standardization

In the context of Polkadot EVM, there are a number of Polkadot-specific
modifications we need to do. Polkadot EVM has custom precompiles as well as
custom gas metering logic. In the past, we have also seen some specific use
cases that require custom transaction format or new opcodes. The Polkadot EVM
collective aims to create an RFC process to document them.

A standardization process is important in certain modifications. The collective
itself acts as a review and audit body to help discover various security issues
in the specifications. It also helps to improve interoperability across
parachains, as eventually we want to have contracts on different parachains
talking with each other freely.

### Development and maintenance

The collective aims to bring more transparency over the development and
maintenance of various tools that the ecosystem uses. We aim to link the
membership of the EVM collective with the membership and merge rights in the
[polkadot-evm](https://github.com/polkadot-evm) Github organization. It
therefore becomes clear who is responsible for the maintenance and who can merge
PRs. It avoids single-point-of-failure if one person is temporarily not available.
It also helps in the situation that some technical differences between different
members are non-conciliable (but hopefully we never come to that point).

### Roadmap

During the past few years when working on the Frontier project, I've seen, at
first hand, the vast different opinions on how the Polkadot community should
work with EVM development. And I'm afraid to say, that it is still the case at
this moment, that there's a big disconnect between the core development team,
and the parachain ecosystem. While those are purely different technical views,
they have vast influence on how subsequently the ecosystem develops tools and
use contracts.

Should the EVM interpreter be on-chain or should EVM contracts be off-chain
compiled first? How strict should we treat EVM compatibility? What is the
timeline of EVM? Should we support EVM indefinitely, or is it purely there to
provide a migration path to WASM/RISC-V?

Such issues have big impact over dapp developers. If they develop on Polkadot,
we want to make sure they have certainty over what they may have and not have in
the near future, so that they know that whatever tools they developed wouldn't
be made obsolete by the core dev team. The Polkadot EVM collective aims to
provide a discussion platform that can provide some certainty.

We also deal with bigger issue in the roadmap, such as the migration of a
complete Ethereum blockchain over to Polkadot. (Yes, this is possible and
technically a planned feature in Frontier.)

### Expert opinions

The Polkadot EVM collective also aims to provide expert opinions and help in
review, audit, and coordinate certain ecosystem initiatives. For example, the
collective may be in charge to draft the detailed technical requirements for the
new "OpenEVM" parachain and supervise its implementation. For this, we currently
don't expect the collective to handle anything related to code implementation.
It will likely be decided through a tendering process via a treasury referendum,
and developed by an external team who wins the bid.

## Scope

The scope of the collective is intentionally set to be specific and concrete in
order to ensure a functional collaberation. One is eligible as a member of the
Polkadot EVM collective if one is involved in the development of a tool or a
parachain/solochain that has EVM feature. This currently includes:

* [Frontier](https://github.com/polkadot-evm/frontier)
* [Rust-EVM](https://github.com/rust-ethereum/evm)
* [Moonbeam](https://github.com/moonbeam-foundation/moonbeam)
* [Astar](https://github.com/AstarNetwork/Astar)
* [Tangle](https://github.com/webb-tools/tangle)
* [Edgeware (EdgeEVM)](https://github.com/edgeware-network/edgeware-node)
* [Polkadot EVM substrate-etl/Dune integration (Colorful Notion)](https://polkadot.polkassembly.io/referenda/366)
* [Acala](https://github.com/AcalaNetwork/Acala)
* [Darwinia](https://github.com/darwinia-network/darwinia)
* [Hyperledger Solang](https://github.com/hyperledger/solang)
* [Magnet](https://github.com/Magport/Magnet)
* Please submit PRs to add another tool to this list.

## Membership

There are two aspects of the membership -- ranks and roles. Rank defines a member's
voting power within the collective. Role gives out ecosystem-specific permissions
and responsibilities.

### Rank

The EVM Collective uses a flat ranking system. We have two ranks.

* **Junior members**. This corresponds to rank I. This is a member that is at least
  somewhat involved in Polkadot EVM development.
* **Senior members**. This corresponds to rank III. This is a member that is deeply
  involved in Polkadot EVM development.

The ranks of a member define the member's voting power. Unlike the Fellowship
collective, rank does not determine a member's other privileges, such as any financial
incentives. They are instead defined by "roles", which we explain in more
details below.

### Role

Role defines a member's responsibilities within the collective. The collective is run
under the assumption that a member's contribution is correlated with the member's
devotion, not seniority. As a result, financial incentives (if any) is associated with
a role, but not with ranks. There are also no limitations on lower ranks with "higher"
roles. A junior member might well have more financial incentives or other benefits,
than a senior member, if she or he contributes more.

The list of roles are dynamic. On-chain, the definition of a role contains only two
information -- its index, and a shortname. Roles can be added or removed by changing
the runtime config, without runtime upgrades. The addition and removal of roles,
and the granting and dismissing of roles of a member, is done by a majority vote of
the collective (respective to the member's voting power), or a referendum in OpenGov.

The initial list of roles will only be defined once the collective becomes active
on-chain, subject to all members' approvals. Below are examples of possible roles:

* **RFC editor**: grants merge rights to the EVM RFC repository, responsible for
  maintaining the RFC process.
* **Frontier maintainer**: grants merge rights to the Frontier repository, responsible
  for maintaining the Frontier project and making new releases.
* **Other project maintainer roles**.
* **Speaker of the collective**: responsible for publishing the collective's annual report
  to the community and handle certain communications.
* **Special task force roles**. For example, launching a community-driven EVM parachain.

## Salary and sub-treasury

The Polkadot EVM Collective has its own salary system and sub-treasury system for future
use. Their values, right now, is always 0. Any increase or funding is only done through
Polkadot referendums.

## Seeding

All seeding members are subject to a final vote of a root referendum. Please submit PRs
to add your name to the seeding list.

| Github username | Polkadot Account | Rank |
| :---: | :---: | :---: |

## Discussions

### A big collective or several small collectives

While designing the collective, the first question we faced is whether we should have
one single big collective -- one that covers all Polkadot ecocsystem ("The Polkadot
Ecosystem Collective") -- or several small collectives, each focusing on a concrete and
specific field in Polkadot.

We believe that small collectives are much more effective in carrying out its tasks:

* Being **concrete and specific** ensures that all members of the collective always know
  the mission of the collective. What belongs, and not belongs a collective is always
  extremely clear.
* Small collectives are **composible**. It's possible to compose small collectives into
  a big collective, should the need raises. Members of the big collective are instances of
  small collectives, instead of people. On the other hand, it's difficult to divide a big
  collective into smaller collectives, if we realize that the former is not functioning
  well.
* Small collectives can **move faster and get more things done** because everyone is working
  in roughly the same field. Misunderstandings are less likely. The objectives are more
  clear. Participations are better encouraged because all motions / RFCs matters to
  nearly everyone.

The only real drawback we know so far about small collectives is the **maintenance burden**. At
this moment, all collectives require separate runtime pallets and also requiring runtime upgrade.
As we expect at least a dozen new collectives in the near future, this is not scalable. We plan
to address this by helping the Fellowship to develop a separate set of pallets that can host
multiple collectives, with sub-treasury and salary features. Proposing a new collective becomes
a runtime config change, instead of a runtime upgrade.

### A flat or a deep ranking system

Readers may notice that in Polkadot EVM Collective's membership design, we only have two ranks,
junior members (with vote power correspond to rank I), and senior members (with vote power correspond
to rank III). We designed this to be a **flat ranking system**. This is in contrast to the
Polkadot Fellowship Collective where we have a **deep ranking system**, with 7-9 ranks.

We use a flat ranking system due to the practicality of the Polkadot EVM Collective, that we
want to ensure that majority of members are actually on-board with a certain motion. The EVM collective
deals less with visionary changes, but more with the practical reality of making EVM work well on
Polkadot. We want to ensure that, for example, EVM metering changes done specifically for Polkadot
are properly reviewed, that precompiles can work with each other, and that EVM contracts across
different parachains can interop. It is therefore really important to ensure that members are
actually on-board, without the risk if a really senior member disagrees with everyone else.

Rank only defines a member's voting power. We introduced a separate concept, called **roles**, to
define a member's responsibilities within the collective. Any financial incentives or benefits of
a member is associated with a role, but not a rank. A role can be a project maintainer, an RFC editor,
a community spokesperson, or a special task-force. Compared with the design of the Fellowship collective,
which relies on a linear scale of ranks, the separate concept of roles makes it significantly easier
to assess a member, and determine whether she or he is sufficiently carrying out the duty.
