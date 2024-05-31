# Summary

## Google's Workload Identity Federation
`code `
---
[Markdown Guid](https://www.markdownguide.org)

```
1) Enable the IAM Service Account Credentials API in the Google Cloud Console
2) Configure a workload identity pool and provider
- Create Workload Identity Pool
-- Name: github-actions-cloud-run
-- Description: github-actions-cloud-run
-- Provider: OIDC
-- Provider Name: github
-- Issuer: https://token.actions.githubusercontent.com
-- Audience: Default audience
--Configure provider attributes
-- google.subnect = assertion.sub
--atrribute.actor = assertion.actor
--atrribute.repository = assertion.repository
--Atrribute conditions: assertion.repository='MyGitHubAccount/MyRepo'
3) Grant SA access to this pool
-- click the pool
--click grant access to SA
-- service account: the SA that accesses to My Cloud Run resources
-- select principals (identities that can access the SA): All identitites in the pool





```
