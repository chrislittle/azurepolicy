# Update VNET Custom DNS Servers Based on Location
NOTE: This policy is built with just a single DNS server in a String.  Additional parameters (Strings) would need to be added if there are more than 1 DNS server to configure. This process would also include the need to perform multiple operations with Append for subsequent IPs.

## Try with Azure portal
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#blade/Microsoft_Azure_Policy/CreatePolicyDefinitionBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fchrislittle%2Fazurepolicy%2Frefs%2Fheads%2Fmain%2Ftestdns%2Fazurepolicy.json)

## Create Policy Definition via Azure Powershell
```
$definition = New-AzPolicyDefinition -Name "Enforce VNET DNS servers" -DisplayName "Enforce VNET DNS servers" -description "This policy enforces the use of a specific DNS Servers on Virtual Networks based on location." -Policy 'https://raw.githubusercontent.com/chrislittle/azurepolicy/refs/heads/main/testdns/azurepolicy.rules.json' -Parameter 'https://raw.githubusercontent.com/chrislittle/azurepolicy/refs/heads/main/testdns/azurepolicy.parameters.json' -Mode All
```

