# CAIPE `.project`

Project metadata and maintainer roster for [CAIPE](https://caipe.io/), a CNCF Sandbox project.

| File | Purpose |
|------|---------|
| [project.yaml](project.yaml) | Project scope, maturity, repositories, and governance and security references |
| [maintainers.yaml](maintainers.yaml) | GitHub handles and teams used for CNCF service provisioning |
| [CODEOWNERS](CODEOWNERS) | Maintainers responsible for metadata review |
| [.github/workflows/](.github/workflows/) | Metadata validation, link checks, and Landscape synchronization |

## Repositories

- [ai-platform-engineering](https://github.com/caipe-io/ai-platform-engineering) — primary platform repository
- [caipe-cli](https://github.com/caipe-io/caipe-cli)
- [governance](https://github.com/caipe-io/governance)
- [agentic-apps](https://github.com/caipe-io/agentic-apps)
- [caipe-sandbox](https://github.com/caipe-io/caipe-sandbox)

## Updating metadata

- Open a pull request for metadata changes. CI validates the schema, new links, and maintainer handles.
- Keep `maintainers.yaml` aligned with the [public maintainer roster](https://github.com/caipe-io/ai-platform-engineering/blob/main/MAINTAINERS.md). Names and affiliations remain in the public project documentation.
- Each maintainer must link their GitHub account and keep their primary email and affiliation current at [openprofile.dev](https://openprofile.dev/). Updating this repository does not update LF profiles.
- The roster is initialized from the project's public `MAINTAINERS.md`; CNCF's foundation CSV does not yet list CAIPE.
- Sign off commits under the [Developer Certificate of Origin](https://developercertificate.org/).

## Automation

- **Validate Project Metadata** runs on pull requests, pushes to `main`, and manual dispatch. LFX profile verification is disabled in the upstream action while the LFX token issue is unresolved; GitHub handle validation remains enabled.
- **Check Links** runs every other Saturday and can be dispatched manually.
- **Update Landscape** runs when project metadata changes and can be dispatched manually. It requires the repository secret `LANDSCAPE_REPO_TOKEN`, authorized to open PRs against `cncf/landscape`. Until CNCF configures that secret, synchronization is skipped and validation still runs.

## References

- [CNCF `.project` setup instructions](https://github.com/cncf/automation/tree/main/utilities/dot-project)
- [Metadata schema](https://github.com/cncf/automation/blob/main/utilities/dot-project/SCHEMA.md)
- [CAIPE Sandbox acceptance](https://github.com/cncf/sandbox/issues/528)
- [CAIPE onboarding](https://github.com/cncf/sandbox/issues/549)
- [Project governance](https://github.com/caipe-io/governance)
- [Code of conduct](https://github.com/caipe-io/ai-platform-engineering/blob/main/CODE_OF_CONDUCT.md)
