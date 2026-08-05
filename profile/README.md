<p align="center">
  <img src="https://raw.githubusercontent.com/product-definition-as-code/.github/main/profile/pdac-social-banner.png" alt="PDaC: Product Definition as Code" width="720" />
</p>

# Product Definition as Code (PDaC)

**Your product, defined like code.**

PDaC is an open methodology for the upstream layer of the AI-SDLC. It models product knowledge as a versioned, validated graph of small, related Markdown artifacts: actors, journeys, use cases, business rules, domain language and requirements. Humans and AI agents consume the same canonical model, and every implementation increment traces back to the product knowledge it serves.

While Spec-Driven Development tools like OpenSpec, Spec Kit and Kiro define how a single change gets built, PDaC defines what the product **is**: the graph that outlives every spec. The citation contract at its boundary is delivery-neutral: the same citations brief an SDD framework, an AI coding agent, or a human team working from the backlog.

## The core principles

1. Product knowledge lives close to the software, inside the repository.
2. Markdown is the canonical representation; the graph is compiled from it, never authored by hand.
3. Every artifact has a stable, immutable identity. Relationships are explicit and machine-readable.
4. Nothing changes the product model silently: the definition changes through exactly one mechanism, an explicit Product Change, approved by a human and accepted through review.
5. Backlog items are projections of accepted product intent, not the source of truth.
6. Delivery consumes canonical product knowledge through citations and reports reality back as proposed Product Changes; it never owns the product definition.

## Repositories

| Repository | What it is |
| --- | --- |
| [`spec`](https://github.com/product-definition-as-code/spec) | The PDaC specification (v0.1 RFC): nine normative chapters, the manifesto, governance and the conformance corpus. |
| [`pdac-lint`](https://github.com/product-definition-as-code/pdac-lint) | Planned: an independent conformance runner (CLI, GitHub Action and badge). Not usable yet; the conformance corpus comes first. |

**Reference implementation:** [ProductShape](https://github.com/juangcarmona/productshape) ([`@prodshape/cli`](https://www.npmjs.com/package/@prodshape/cli) on npm). ProductShape is to PDaC what OpenSpec is to Spec-Driven Development. The spec welcomes further implementations; if you are building one, open an issue in `spec`.

## Start here

- [The founding article](https://jgcarmona.com/en/product-definition-as-code/): why the bottleneck moved left, and what to do about it.
- [The manifesto](https://github.com/product-definition-as-code/spec/blob/main/MANIFESTO.md): four values, ten principles, the position in full. You can [sign it](https://github.com/product-definition-as-code/spec/blob/main/SIGNATORIES.md).
- Start with the manifesto and the spec; the reference implementation is being updated to the citation contract.

## Status

The specification skeleton is live in [`spec`](https://github.com/product-definition-as-code/spec) as **v0.1 (request for comments)**: nine chapters extracted from the reference implementation, governance and RFC process in place, conformance corpus in progress. The version number says what it is: an early draft, weeks old, not a near-final standard.

The honest picture of where every surface stands, and the gates required before v1 may call itself a standard, is in the [maturity matrix](https://github.com/product-definition-as-code/spec/blob/main/MATURITY.md). What the methodology cannot claim yet is named in [known limits](https://pdac.dev/known-limits/).
