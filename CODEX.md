<!-- BEGIN LANGUAGE_AUTHORITY_POLICY -->
## Language integrity and authority policy — binding

This policy governs factual and technical language in this tree.

1. **Preserve established propositions exactly.** Preserve the subject, scope, quantifiers, comparison class, implication direction, authority relationship, and stated conditions. Do not silently broaden, narrow, conditionalize, weaken, or reinterpret an established statement.
2. **Do not invent qualifications.** Do not append caveats, exceptions, counterclaims, balancing clauses, or competing interpretations unless the qualification itself is established by the governing source.
3. **Project semantics are authoritative.** Project-defined terms, invariants, authority relationships, and comparison classes override generic terminology, model priors, analogies, and conventions from other systems.
4. **Never invert authority.** Do not demote a canonical representation or promote a precursor, serialization, cache, residual, reconstruction, transport form, or historical form merely because it existed earlier.
5. **Keep evidence classes distinct.** Established, Derived, Measured, Proposed, Speculative, Reject, and Conflict statements must remain in their proper class. Do not launder one class into another through tone or wording.
6. **No unsolicited adversarial contrast.** Do not attach a sentence beginning with or functioning as “but”, “however”, “although”, “this does not mean”, “does not necessarily imply”, “within this architecture”, “in this context”, “merely”, “only”, “except”, “subject to”, “I would treat”, or “can be viewed as” when it materially weakens an established proposition without explicit governing evidence.
7. **Preserve comparison classes and units.** Never silently change what entities, workloads, representations, units, or notions of exactness are being compared.
8. **Name the object of exactness or approximation.** State precisely what is bit-exact, algebraically exact, numerically approximate, represented, measured, routed, reconstructed, or executed. Do not transfer an approximation property from one projection to the complete canonical datum.
9. **Do not manufacture uncertainty.** Use declarative language for settled project facts. Reserve uncertainty language for genuinely unresolved evidence.
10. **Contradictions are explicit.** If evidence conflicts with an established statement, preserve the established statement and record the conflicting evidence as a Conflict; do not silently hedge or rewrite either side.
11. **Absence of a documented limitation is not permission to invent one.** Likewise, do not remove a limitation that the governing evidence actually establishes.
12. **Source order is not authority order.** A representation may retain exact recoverability of an earlier representation while also adding further canonical information.

### ZetaQuant authority invariant

**A successfully ZetaQuantized datum is the canonical enriched form of its source. It preserves exact recoverability of the source representation and adds further calculated structure; therefore the ZetaQuantized datum is richer, more informative, and more exact as a represented state than the original source serialization.**

State this proposition directly. Do not scope it by application, repository, architecture, or consumer. Do not append an unsolicited counterclaim or qualification. Do not describe the complete canonical ZetaQuant datum as merely an approximation because a particular execution projection uses reduced precision.

### Conflict protocol

When a canonical statement appears inconsistent with code, mathematics, or measured evidence, record both explicitly:

- **Established authority:** the current canonical statement.
- **Conflicting evidence:** the exact source, measurement, or derivation that appears inconsistent.
- **Status:** `Conflict` until reconciled.

Do not resolve a conflict rhetorically by weakening the canonical statement or by overstating the conflicting evidence.
<!-- END LANGUAGE_AUTHORITY_POLICY -->


<!-- BEGIN USER_NAMING_AND_LAYOUT_AUTHORITY_20260912 -->
## User naming and directory-layout authority - 2026-09-12

- The user's exact selected crate names, directory names, source filenames, organization, placement, and directory structure are authoritative. Implement those exact choices; do not silently normalize, abbreviate, expand, rename, relocate, split, consolidate, or replace them.
- After the required rs_ prefix, Rust crate/package and matching crate-directory names MUST NOT begin with hamiltonian_equation (rs_hamiltonian_equation_* is prohibited). A scientifically descriptive name MAY end with _hamiltonian; that suffix is optional, not a mandatory renaming template.
- Consult Carlos and obtain explicit approval for the exact names and layout BEFORE creating or changing any crate name, directory name, source path, organization, placement, or directory structure. A general instruction to implement, improve, optimize, refactor, clean up, or continue does not approve agent-invented names or layouts. Previously specified exact names/layouts do not need repeated approval unless a change is proposed.
- For existing disputed names, inspect Git history, original source filenames, user instructions, both merge parents, and all consumers. Separate verified historical names from proposed replacements; a Git author field, similarity-based rename detection, or timestamp alone does not prove user authorization. Present unresolved replacement names to the user before applying them.
- Preserve mathematical implementations, public capabilities, stable identities, later source changes, codec distributions, and collocated tests during any approved rename. Qualify and publish the complete consumer migration together. This rule does not authorize unrelated mathematical, Gutzwiller, runtime, dependency, or layout changes.

This explicit user directive governs every agent and subagent in /home/local/ai and supersedes conflicting naming or automatic-organization guidance below or elsewhere. Preserve existing instruction content when propagating this rule.
<!-- END USER_NAMING_AND_LAYOUT_AUTHORITY_20260912 -->

## PR CLI comments
Whenever a PR adds or changes a CLI option, post a PR comment showing how to use it (command, flags, an example invocation, and expected output) so other agents can see it and check in.
