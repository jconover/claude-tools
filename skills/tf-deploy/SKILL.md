# Terraform Deploy Cycle
1. Run `terraform validate` first — fix any syntax errors
2. Run `terraform plan -out=tfplan` and review the plan
3. Ask user for confirmation before `terraform apply tfplan`
4. If apply fails, read the FULL error output before diagnosing
5. For cloud API errors: check if APIs are enabled, resources exist, and deletion_protection is set correctly
6. For race conditions: add explicit `depends_on` rather than retrying blindly
7. Never use `terraform state rm` unless explicitly asked
