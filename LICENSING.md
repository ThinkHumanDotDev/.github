# Licensing

GitHub has no organisation default for `LICENSE`, so every public ThinkHuman repository carries its
own. This page says which license a repository gets and how to apply it.

## Which license

| Repository | License | SPDX | Examples |
|---|---|---|---|
| Package, library or shared config | MIT | `MIT` | biome-config, renovate-config, payload-plugin-auth |
| Self-hostable product, open source | GNU AGPL v3 | `AGPL-3.0-only` | marmot |
| Self-hostable product, commercially protected | Functional Source License, Apache 2.0 future | `FSL-1.1-ALv2` | riftseer |
| Private repository | None (all rights reserved) | `UNLICENSED` | infrastructure, internal-dashboard |

- **MIT** is the default for anything meant to be installed or extended by others.
- **AGPL** is for products we want to stay open source: anyone may run or change them, but must share
  their changes, including when offering them as a hosted service.
- **FSL** is source-available, not open source: anyone may read, run and change the code, but not
  offer a competing product for two years, after which each version becomes Apache 2.0. Do not call
  an FSL repository "open source".
- A **fork** keeps its upstream license. Do not relicense someone else's code.

Changing a published repository's license needs agreement from everyone whose code it contains, so
choose before the first public release.

## Applying it

1. **`LICENSE`** at the repository root, the unmodified license text from
   [choosealicense.com](https://choosealicense.com) or the license's own site, so GitHub detects it.
2. **Copyright line** where the license has one:

   ```text
   Copyright (c) <first year> ThinkHuman Ltd.
   ```

   Use the year the repository was first published. Do not update it every year.
   In a fork, keep the upstream copyright line and add ours below it.
3. **`package.json`**: set `"license"` to the SPDX identifier from the table. Private repositories
   use `"UNLICENSED"` with `"private": true`.
4. **Third-party code**: code copied or ported from another project keeps that project's notice.
   List it in `THIRD_PARTY_NOTICES.md` (see marmot), and add an attribution comment to each ported
   file.
