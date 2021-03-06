# aad oauth2grant remove

Remove specified service principal OAuth2 permissions

## Usage

```sh
aad oauth2grant remove [options]
```

## Options

Option|Description
------|-----------
`--help`|output usage information
`-i, --grantId <grantId>`|`objectId` of OAuth2 permission grant to remove
`-o, --output [output]`|Output type. `json|text`. Default `text`
`--verbose`|Runs command with verbose logging
`--debug`|Runs command with debug logging

!!! important
    Before using this command, connect to Azure Active Directory Graph, using the [aad connect](../connect.md) command.

## Remarks

To remove service principal's OAuth2 permissions, you have to first connect to Azure Active Directory Graph using the [aad connect](../connect.md) command, eg. `aad connect`.

Before you can remove service principal's OAuth2 permissions, you need to get the `objectId` of the permissions grant to remove. You can retrieve it using the [aad oauth2grant list](./oauth2grant-list.md) command.

## Examples

Remove the OAuth2 permission grant with ID _YgA60KYa4UOPSdc-lpxYEnQkr8KVLDpCsOXkiV8i-ek_

```sh
aad oauth2grant remove --grantId YgA60KYa4UOPSdc-lpxYEnQkr8KVLDpCsOXkiV8i-ek
```

## More information

- Application and service principal objects in Azure Active Directory (Azure AD): [https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-application-objects](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-application-objects)