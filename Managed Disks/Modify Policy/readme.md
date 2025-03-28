# Configure Managed disks to disable public and private network access
Disable public and private network access for your managed disk resource so that it's not accessible over public internet or private endpoints. This can reduce data leakage risks.

# Guide
1. Deploy the Policy to the required scope (Management Group, Subscription etc). Any new virtual machines and their respective managed disks will immediately get modified to the correct configuration.
2. Create a new virtual machine to validate that the managed disk gets modified correctly in a test environment (within scope of policy).
3. Run remediation tasks (within the scope of the policy) after Azure Policy compliance updates (usually within 24 hours) for machines already in place. 

## Try with Azure portal
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/?#blade/Microsoft_Azure_Policy/CreatePolicyDefinitionBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fchrislittle%2Fazurepolicy%2Frefs%2Fheads%2Fmain%2FManaged%2520Disks%2FModify%2520Policy%2Fazurepolicy.json)
