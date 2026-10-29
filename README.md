# 1loc — maintained edition

The 313 JavaScript one-liners of the original [1loc](https://github.com/phuocng/1loc) collection by Nguyen Huu Phuoc and contributors, reviewed and tested, plus a small set of email utilities. Published at **[1loc.dev](https://1loc.dev/)**, where every snippet has a page at its original address and a local lab that runs it on your data.

## Why this fork

- The original site (1loc.dev, later phuoc.ng/collection/1-loc) went offline when its domains expired, and the repository has not changed since December 2023.
- Executing every snippet with its documented examples and edge cases found 29 that return wrong results. They are fixed here and proposed upstream in [phuocng/1loc#559](https://github.com/phuocng/1loc/pull/559); [issue #558](https://github.com/phuocng/1loc/issues/558) lists each case with the failing input.
- This branch is what 1loc.dev publishes. Each page on the site links to its file here, at the pinned commit, and the site's build checks that the two agree.

## What is different from the original

- `contents/`: the original 313 files, with the 29 corrections. The JavaScript and TypeScript versions change together, and the examples of each corrected file cover the input that failed.
- 10 new files in the `Email` category, written by [Oveyon](https://oveyon.com/), the maintainer of 1loc.dev: converting a domain to punycode, extracting and normalizing addresses, masking addresses for logs, reading `Retry-After`, backoff with full jitter, idempotency keys, classifying SMTP replies, and building and parsing DMARC records. Each has a `Notes` section with its limits.
- Everything else is as in the original. The site's own code (the Astro build, the lab, the test suite) is not in this repository.

## Branches

| Branch | Content |
| --- | --- |
| `1loc.dev` (default) | The maintained edition: original files, corrections and the Email category. |
| `fix/reviewed-snippets` | Only the 29 corrections, as sent upstream in PR #559. |
| `master` | Mirrors `phuocng/1loc`. |

## Contributing

Open a pull request against `1loc.dev`: one file per snippet in `contents/`, in the existing format — a **JavaScript version**, a **TypeScript version** and **Examples** whose `// expected` comments hold when the lines are executed. A correction that also applies to the original collection is welcome upstream too; this fork carries it either way. Merged changes reach 1loc.dev on the site's next publish.

## License and attribution

MIT, as the original. Original collection: Copyright (c) 2020 phuoc-ng. Corrections and the Email utilities: Copyright (c) 2026 Oveyon. The original author does not endorse this edition; Oveyon maintains it and discloses that relationship on the site.
