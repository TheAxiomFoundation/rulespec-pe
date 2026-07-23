# rulespec-pe Agent Notes

This repo stores Peru RuleSpec source registry materials, oracle references, and encoded policy rules. All encoded law lives under a single `pe/` namespace.

## Scope

- `pe/statutes/`: Peruian laws — the TUO LIR (DS 179-2004-EF) chain, the TUO IGV/ISC (DS 055-99-EF), Ley 26790, and other primary law needed for tax-benefit modeling.
- `pe/regulations/`: executive decrees, reglamentos, and institutional resolutions (pension-system instruments, SUNAT resolutions, UIT decrees) made under the laws.
- `pe/policies/`: social-protection programme rules set administratively (Pensión 65 and Juntos programme rules).
- `programs/`: declarative compose specs (one per jurisdiction/program/period).
- `data/coverage/`, `data/oracles/`: coverage backlog and comparison references. These are never legal authority.

## Do

- Start from the furthest upstream source: Registro Oficial texts and official consolidations (SRI compilations, IESS prints, ministry legal-basis records — record the host in manifest metadata), decrees and institutional resolutions next, agency guidance last.
- Add RuleSpec under `pe/statutes/`, `pe/regulations/`, or `pe/policies/` with companion `.test.yaml` files.
- Cite corpus paths from modules via `module.source_verification.corpus_citation_path` (or `corpus_citation_paths`).
- Use the PERUMOD v2.4 policy window (2019–24) as the validation frame: IGV 16%+2% IPM; EsSalud 9%; pension 10% AFP / 13% ONP; Pensión 65 ~S/250 bimonthly; UIT-banded PIT. Indexed/annual values must be corpus-grounded, never invented.
- Keep exact oracle versions in `data/oracles/oracle-index.json`. The SOUTHMOD bundle is licensed and non-redistributable — never commit bundle bytes, dataset rows, or model XML.
- Sync `axiom-encode` and `.axiom/toolchain.toml` before substantial encoding runs.

## Do Not

- Use SUNAT calculators or third-party tax alerts as the first legal source when a law or instrument governs the rule.
- Invent, round, or interpolate any Peruian monetary amount, rate band, or threshold. Every number must come verbatim from a captured official provision.
- Migrate PERUMOD, EUROMOD/SOUTHMOD, or agency calculator code mechanically as RuleSpec.
- Add generated source payload dumps, formula artifacts, `parameters.yaml`, or standalone YAML fixtures outside allowed RuleSpec roots.
- Hand-copy statute text into RuleSpec without a corpus `citation_path`.
