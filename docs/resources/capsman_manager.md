# routeros_capsman_manager (Resource)


## Example Usage
```terraform
resource "routeros_capsman_manager" "test_manager" {
	enabled        = true
	upgrade_policy = "require-same-version"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `ca_certificate` (String) Device CA certificate.
- `certificate` (String) Device certificate.
- `enabled` (Boolean) Disable or enable CAPsMAN functionality.
- `package_path` (String) Folder location for the RouterOS packages. For example, use '/upgrade' to specify the upgrade folder from the files section. If empty string is set, CAPsMAN can use built-in RouterOS packages, note that in this case only CAPs with the same architecture as CAPsMAN will be upgraded.
- `require_peer_certificate` (Boolean) Require all connecting CAPs to have a valid certificate.
- `upgrade_policy` (String) Upgrade policy options.

### Read-Only

- `id` (String) The ID of this resource.

## Import
Import is supported using the following syntax:
```shell
terraform import routeros_capsman_manager.test_manager .
```
