# Update VNET Custom DNS Servers Based on Location

## Create Policy Definition via Azure Powershell
```
$definition = New-AzPolicyDefinition -Name "Update VNET Custom DNS Servers Based on Location" -DisplayName "Update VNET Custom DNS Servers Based on Location" -description "Update virtual network custom DNS servers based on a defined list of locations" -Policy 'https://raw.githubusercontent.com/chrislittle/azurepolicy/refs/heads/main/AppendDNSServersVNET/azurepolicy.rules.json' -Parameter 'https://raw.githubusercontent.com/chrislittle/azurepolicy/refs/heads/main/AppendDNSServersVNET/azurepolicy.parameters.json' -Mode All
```
