# spectral-org-scan

### About
This repo contains a github action workflow that will scan a predefined GitHub Org with [SpectralOps](https://get.spectralops.io) scanning tool.

### How to use

#### Pre-Requirements:
Stored in [GitHub Secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets).
- SPECTRAL_DSN - obtained from SpectralOps portal.
- MY_GITHUB_TOKEN - github token with permissions to read public and desired private repos.

Defined in workflow yaml file (/workflow/spectral-org-scan.yml)
- ORG_NAME - name of GitHub Organization that you wish to scan.

#### Setup

Place /workflow/spectral-org-scan.yaml in your own repo with same path.

Customize the trigger section to your desired cron schedule:

        on:
          schedule:
            - cron:  '30 5,17 * * *'

You can [manually](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow) run a workflow or wait for the cron schedule you defined.
