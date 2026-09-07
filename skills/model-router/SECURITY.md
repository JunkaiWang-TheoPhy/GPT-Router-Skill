# Security and permissions

This skill is intended for a public, forkable repository. Public visibility does not imply write access.

Repository administrators should enforce branch protection for the default branch, require pull requests and passing checks, enable secret scanning and push protection where available, and grant write/admin roles only to named maintainers. Forks and redistribution are allowed under the repository license, but forks must not receive credentials, private workspace dumps, or local telemetry by default.

The skill itself is read-only with respect to routing evidence. It may inspect the minimum workspace context needed to choose a model, but must not publish private content or make external mutations solely because a stronger model was selected. Report suspected vulnerabilities through the repository's private security channel rather than opening a public issue with sensitive details.
