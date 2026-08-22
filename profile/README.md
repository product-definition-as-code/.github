<p align="center">
  <img src="https://raw.githubusercontent.com/product-definition-as-code/.github/main/profile/pdac-social-banner.png" alt="PDaC: Product Definition as Code" width="720" />
</p>

# Product Definition as Code (PDaC)

**Your product, defined like code.**

Product Definition as Code keeps the agreed product definition in versioned Markdown that delivery work cites instead of restating.

The definition lives as small, related Markdown files — actors, journeys, use cases, business rules, domain terms, requirements — compiled into a validated product graph that humans and AI agents read alike. It changes only through an explicit Product Change, reviewed and accepted by a human. Consumer documents (SDD specs, tasks, agent prompts) cite the exact product text they rely on by stable ID and content digest, and when cited text changes, tools flag every recorded citation for review: documentation drift is detected instead of silent. Deterministic tools check structure and references, never truth; people decide what is true and what should change.

A delivery spec cites a product rule. Someone changes the rule. The next verification run flags the spec, and nobody had to remember to check:

```console
$ prodshape citations verify
stale	BR-REFUND-001	openspec/checkout-flow.citations.yaml:1
warning PRODUCT061 openspec/checkout-flow.citations.yaml [BR-REFUND-001]: Citation of 'BR-REFUND-001' is stale: canonical content changed since the citation was recorded
1 citation(s): 0 current, 1 stale, 0 tampered, 0 unresolved
```

That is the citation contract, the delivery boundary of PDaC. Delivery tools decide how to build what the definition describes, and only recorded citations are checked. [See it in 30 seconds on pdac.dev](https://pdac.dev/), or run it yourself with `npm install -g @prodshape/cli`.

While Spec-Driven Development tools like OpenSpec, Spec Kit and Kiro define how a single change gets built, PDaC defines what the product **is**: the graph that outlives every spec. The full position is [the manifesto](https://github.com/product-definition-as-code/spec/blob/main/MANIFESTO.md), which you can [sign](https://github.com/product-definition-as-code/spec/blob/main/SIGNATORIES.md).

## Start here

- [See a citation catch drift on pdac.dev](https://pdac.dev/).
- [Try ProductShape](https://github.com/juangcarmona/productshape#quickstart), the reference CLI.
- [Read the PDaC specification](https://github.com/product-definition-as-code/spec) or [the founding article](https://jgcarmona.com/en/product-definition-as-code/).
- [Review the current maturity and limits](https://github.com/product-definition-as-code/spec/blob/main/MATURITY.md).

## Repositories

| Repository | Role |
| --- | --- |
| [`spec`](https://github.com/product-definition-as-code/spec) | Defines the PDaC model, relationships, citations, Product Change lifecycle and implementation requirements. It also publishes the conformance tests. |
| [ProductShape](https://github.com/juangcarmona/productshape) | The reference implementation of Product Definition as Code: a CLI for creating, checking, changing, exploring and citing a product definition. |
| [`pdac-lint`](https://github.com/product-definition-as-code/pdac-lint) | Runs the published conformance tests against a PDaC implementation. It checks implementations, not product repositories. |
| [`product-definition-as-code.github.io`](https://github.com/product-definition-as-code/product-definition-as-code.github.io) | Publishes [pdac.dev](https://pdac.dev/), the public entry point for the method, diagrams and specification pages. |

The spec welcomes further implementations; if you are building one, open an issue in `spec`.

## Status

PDaC is a **v0.1 request for comments**, not a final standard. The conformance tests are runnable — the reference implementation passes every published case — but they are not yet a complete normative set. The [maturity matrix](https://github.com/product-definition-as-code/spec/blob/main/MATURITY.md) records what is complete, and [known limits](https://pdac.dev/known-limits/) states what the project cannot claim yet.
