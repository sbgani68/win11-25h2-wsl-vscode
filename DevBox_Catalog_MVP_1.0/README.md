
# DevCenter Catalog Structure (Dev Box only)

This repository is organized to avoid cross-validation with Azure Deployment Environments (ADE):

- **/ImageDefinitions/** → Microsoft Dev Box image definitions (e.g., `imagedefinition.yaml`).
- **/Tasks/** → (Optional) Dev Box catalog tasks (`task.yaml` per task) if you add custom tasks later.
- **/Environment-Definitions/** → (Optional) ADE environment definitions. If you use ADE, each subfolder **must** contain:
  - An IaC template (e.g., `main.bicep`, `azuredeploy.json`, or Terraform files), and
  - An `environment.yaml` with a non-empty `templatePath` pointing to that template.

## Azure Portal Settings
- **Project → Catalogs → Catalog item permissions:** enable **Image definitions**; disable **Environment definitions** unless you add valid ADE items.
- **Add/Edit Catalog → Folder path:** set to `/ImageDefinitions`.

## References
- Dev Box customizations & image definitions: Microsoft Learn
- Catalogs & sync settings: Microsoft Learn
- ADE environment definition schema (`templatePath`): Microsoft Learn
