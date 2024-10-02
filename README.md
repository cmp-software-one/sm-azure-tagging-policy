# About this Automation

Apply a tag policy that applies to all resource built in your environment.


## Fields and Best Practices

| Field         | Best practice and Options      | Limitations |
| ------------- | --------------------------------- |-|
| **Request title**       | A friendly short name to remind you why you created this account         | 256 characters|
| **Request description**        | Add more details on the need for the account          |256 characters |
| **Azure subscription ID** | Select your target Subscription ID | NA |
| **List of Mandatory tags** | Tag Name  | Refer to the **Tagging Limitations** section below |


### Tagging best practies

[Microsoft Tagging best practices](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/naming-and-tagging)

### Tagging limitations

The following limitations apply to tags:

Not all resource types support tags. To determine if you can apply a tag to a resource type, see Tag support for Azure resources.

Each resource, resource group, and subscription can have a maximum of 50 tag name-value pairs. If you need to apply more tags than the maximum allowed number, use a JSON string for the tag value. The JSON string can contain many of the values that you apply to a single tag name. A resource group or subscription can contain many resources that each have 50 tag name-value pairs.

The tag name has a limit of 512 characters and the tag value has a limit of 256 characters. For storage accounts, the tag name has a limit of 128 characters and the tag value has a limit of 256 characters.

Classic resources such as Cloud Services don't support tags.

Azure IP Groups and Azure Firewall Policies don't support PATCH operations. PATCH API method operations, therefore, can't update tags through the portal. Instead, you can use the update commands for those resources. You can update tags for an IP group, for example, with the az network ip-group update command.

Tag names can't contain these characters: <, >, %, &, \, ?, /


