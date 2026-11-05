# Licensing

GitHub has no organisation default for `LICENSE`, so every public ThinkHuman repository carries its
own. This page says which license a repository gets and how to apply it.

## Which license

| Repository | License | `package.json` `"license"` | Examples |
|---|---|---|---|
| Package, library or shared config | MIT | `MIT` | biome-config, renovate-config, payload-plugin-auth |
| Self-hostable product, open source | GNU AGPL v3 | `AGPL-3.0-only` | marmot |
| Self-hostable product, commercially protected | Functional Source License, Apache 2.0 future | `FSL-1.1-ALv2` | riftseer |
| Private repository | None (all rights reserved) | `UNLICENSED` (npm value, not SPDX) | infrastructure, internal-dashboard |

- **MIT** is the default for anything meant to be installed or extended by others.
- **AGPL** is for products we want to stay open source: anyone may run, change and share them, but
  whoever distributes a modified version, or lets people use one over a network (a hosted service),
  must offer those users its complete source under the AGPL. Private changes nobody else uses carry
  no obligation.
- **FSL** is source-available, not open source: anyone may use, change and redistribute the code for
  any purpose except a *Competing Use*, a commercial product or service that substitutes for it or
  offers substantially similar features. Two years after each version is made available, that
  version is also licensed under Apache 2.0. The [license text](https://fsl.software) is the
  authority. Do not call an FSL repository "open source".
- A **fork** keeps its upstream license. Do not relicense someone else's code.

Changing a published repository's license needs agreement from everyone whose code it contains, so
choose before the first public release.

## Applying it

1. **`LICENSE`** at the repository root: the license text from
   [choosealicense.com](https://choosealicense.com) or the license's own site, changed only to fill
   in its placeholders, so GitHub detects it.
2. **Copyright line**: where the license text has a copyright placeholder (MIT's `[year]` and
   `[fullname]`, FSL's Notice), replace it inside `LICENSE` with:

   ```text
   Copyright (c) <first year> ThinkHuman Ltd.
   ```

   Use the year the repository was first published. Do not update it every year.
   In a fork, keep the upstream copyright line and add ours on the line below it. The AGPL text has
   no placeholder: leave `LICENSE` as it is and put the notice in the README.
3. **`package.json`**: set `"license"` to the value from the table: the SPDX identifier for a
   licensed repository, or npm's `"UNLICENSED"` with `"private": true` for a private one.
4. **Third-party code**: code copied or ported from another project must meet every condition of
   that project's license, which can include keeping its notice, shipping its full license text,
   marking changes or offering source. At a minimum, list it in `THIRD_PARTY_NOTICES.md` with its
   license (see marmot) and add an attribution comment to each ported file. If the license is
   incompatible with the repository's own, do not copy the code.
