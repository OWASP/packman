# npm

npm is the package manager for JavaScript.


## Tier

The npm package manager is tier 1.

## Contacts

- security - security@npmjs.com
- support - support@npmjs.com
- homepage: https://npmjs.com


## Compliance Table

| Control | Status | Comments |
|---------|--------|--------|
| Strong Authentication | Optional |  |
| MFA To Push Artifacts | Optional |  |
| Security Contacts | Yes | [security.txt](https://www.npmjs.com/.well-known/security.txt) |
| Packages Can Notify of Security Issues | Partial | A [report a vulnerability](https://www.npmjs.com/advisories/report) function is available on every package page for maintainers to get an entry into the npm audit advisory feed |
| Code package tied to source code | No | |
| Update notifications | Partial | Maintainer that published the package is notified |
| Code signing | Partial | npm signs package metadata with internal gpg keys, verification is currently a [manual process](https://blog.npmjs.org/post/172999548390/new-pgp-machinery) |
| Code analysis (static) | No |  |
| Code Dependency Analysis | Yes | [npm audit](https://docs.npmjs.com/cli/audit) |
| Package Manager Does Not Run Code | Optional | The `--ignore-scripts` argument will cause npm to not execute any scripts defined in the package.json |
| Package Manager Does Not Collect Info | No | [npm privacy policy](https://www.npmjs.com/policies/privacy) |
| Project Roles Guide | No |  |
| Project Roles Review | No | |
| Account Level Library Tagging | No |  |
