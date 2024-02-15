# Polkadot EVM Collective

The Polkadot EVM collective is a planned on-chain technical collective that
deals with everything related to EVM. It is similar to the fellowship program,
and instead of dealing with the runtime, it deals with EVM issues.

There are four goals of this collective. It is first and foremost a
standardization body that will be in charge of its own RFC process. It wants to
provide transparency over the development and maintenance of various tools that
the ecosystem uses. It also tries to create an inclusive roadmap with the aim
of reconcile different needs. And finally, it provides expert opinions when the
need raises. We'll discuss the three goals in more details in the following
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
compiled first? How strict should we treat EVM compatiblity? What is the
timeline of EVM? Should we support EVM indefinitely, or is it purely there to
provide a migration path to WASM/RISC-V?

Such issues have big impact over dapp developers. If they develop on Polkadot,
we want to make sure they have certainty over what they may have and not have in
the near future, so that they know that whatever tools they developed wouldn't
be made obsolete by the core dev team. The Pokladot EVM collective aims to
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

## Membership

### Definition

One is eligible as a member of the Polkadot EVM collective if one is involved in
the development of a tool or a parachain that have EVM feature. This currently
includes:

* [Frontier](https://github.com/polkadot-evm/frontier)
* [Rust-EVM](https://github.com/rust-ethereum/evm)
* [Moonbeam](https://github.com/moonbeam-foundation/moonbeam)
* [Astar](https://github.com/AstarNetwork/Astar)
* Please submit PRs to add another tool to this list.

We currently only define two ranks, rank I and rank III. Rank I means a member
is at least somewhat involved, and rank III means a member is deeply involved.

### Seeding

All seeding members are set to be rank III and is subject to a final vote of a
root referendum.

* Please submit PRs to add your name to the seeding list.
