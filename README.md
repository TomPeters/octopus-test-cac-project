# Release page reference

Config-as-code content for the "Reference: full" project (P1) in the release page reference set. The seed script in the OctopusDeploy repository (`docs/plans/release-page-reference-set/seed.mts`) connects a project to this repository and adopts the `.octopus` folder as-is.

- `.octopus/` - the project's deployment process, settings and variables.
- `scripts/hello.sh` - the script the "Run script from Git" step points at, so the release has a Git resource.

The repository must be public: the "Run script from Git" step reads it anonymously, because the Octopus GitHub connection id changes every time the reference space is recreated.

Don't edit the `.octopus` folder through Octopus. The seed script expects the project to adopt this content unchanged.
