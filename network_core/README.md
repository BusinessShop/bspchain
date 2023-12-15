# Network Core

## Terraform cloud

- Register: https://app.terraform.io
- Create API token at https://app.terraform.io/app/settings/tokens (User -> Setting -> Tokens)
- Create new Organization. Ex: `BSPChain`
- Create new Workspace with `CLI-driven workflow`. Ex: `testnet-bspchain`

### Terraform local

- Copy `env.tf.dev` to `env.tf` and CORRECT `Org name` and `Workspace name` in `env.tf`
- IF you have multi credentials, you need to set TF_CLI_CONFIG_FILE each deployment:
    + Copy `.terraformrc.dev` to `.terraformrc` and CORRECT API token
    + Run this command: `export TF_CLI_CONFIG_FILE=".terraformrc"`
- ELSE just use global config by `terraform login` -> the config places at `$HOME/.terraform.d/credentials.tfrc.json`
- Initialize: `terraform init`
- Planning: `terraform plan`
- Destroy: `terraform destroy`
