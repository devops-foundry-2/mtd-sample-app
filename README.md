# mtd-sample-app

MuleSoft sample application for the `devops-foundry-2` pilot foundation.

- **Runtime:** Mule 4.6.37 LTS on CloudHub 2.0
- **Regions:** EMEA + AMER (each with Design / Sandbox / Production tiers)
- **Parent POM:** `mule.test.devops:mtd-parent-pom:1.0.0-SNAPSHOT` (GitHub Packages)
- **CI/CD:** `devops-foundry-2/mule-cicd-workflows` reusable workflows

## Branching

- `main` — protected; merge via PR with 1 approval + code-owner review
- `feature/*` · `bugfix/*` · `hotfix/*` — allowed working branches
- `vX.Y.Z` tags — trigger Production deploy (approval-gated per BG)

## Developer flow

1. Create a feature branch: `feature/my-change`
2. Push commits; PR to `main`; validation runs
3. Merge to `main` → build SNAPSHOT → auto-deploy to Design then Sandbox (both BGs)
4. Create a tag `vX.Y.Z` on main → Production deploy, gated per BG
