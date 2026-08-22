<p align="center">
  <img src="https://raw.githubusercontent.com/product-definition-as-code/.github/main/profile/pdac-social-banner.png" alt="PDaC: Product Definition as Code" width="720" />
</p>

# Product Definition as Code (PDaC)

Product Definition as Code keeps the agreed product definition as versioned Markdown beside the software, so people and AI agents work from the same source. Product requirements, rules, actors, journeys and domain terms have stable IDs and explicit relationships. Markdown is the source of truth; tools compile the graph from it.

Delivery specifications and other working documents cite the exact product-definition text they rely on. When that text changes, verification identifies the recorded citations that need review. This makes documentation drift visible instead of relying on memory.

```console
$ prodshape citations verify
stale  BR-REFUND-001  openspec/checkout-flow.citations.yaml:1
1 citation(s): 0 current, 1 stale, 0 tampered, 0 unresolved
```

People decide what is true, review Product Changes and accept the product baseline. PDaC tools check structure, relationships and recorded citations. Delivery tools decide how to build it. Only recorded citations are checked.

## Start here

- [See a citation catch drift on pdac.dev](https://pdac.dev/).
- [Try ProductShape](https://github.com/juangcarmona/productshape#quickstart), the reference CLI.
- [Read the PDaC specification](https://github.com/product-definition-as-code/spec) or [the manifesto](https://github.com/product-definition-as-code/spec/blob/main/MANIFESTO.md).
- [Review the current maturity and limits](https://github.com/product-definition-as-code/spec/blob/main/MATURITY.md).

## Repositories

| Repository | Role |
| --- | --- |
| [`spec`](https://github.com/product-definition-as-code/spec) | Defines the PDaC model, relationships, citations, Product Change lifecycle and implementation requirements. It also publishes the specification tests. |
| [ProductShape](https://github.com/juangcarmona/productshape) | The reference CLI for creating, checking, changing, exploring and citing a product definition. |
| [`pdac-lint`](https://github.com/product-definition-as-code/pdac-lint) | Runs the published specification tests against a PDaC implementation. It checks implementations, not product repositories. |
| [`product-definition-as-code.github.io`](https://github.com/product-definition-as-code/product-definition-as-code.github.io) | Publishes [pdac.dev](https://pdac.dev/), the public entry point for the method, diagrams and specification pages. |

## Status

PDaC is a **v0.1 request for comments**, not a final standard. The [maturity matrix](https://github.com/product-definition-as-code/spec/blob/main/MATURITY.md) records what is complete, and [known limits](https://pdac.dev/known-limits/) states what the project cannot claim yet.
