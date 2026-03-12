# .claude/skills/deploy-check/SKILL.md
## Pre-Deploy Validation
1. Run `terraform validate` and `terraform plan` — report any errors.
2. Check all ExternalSecret resources use the correct API version (external-secrets.io/v1beta1 vs v1).
3. Verify secret name consistency between Terraform outputs and K8s manifests.
4. Check Helm chart values match expected variable names.
5. Report a summary of findings.
