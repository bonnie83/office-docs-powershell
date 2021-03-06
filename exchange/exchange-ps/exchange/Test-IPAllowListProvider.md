---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016
schema: 2.0.0
---

# Test-IPAllowListProvider

## SYNOPSIS
!!! Exchange Server 2010

Use the Test-IPAllowListProvider cmdlet to test the configuration for a specific IP Allow list provider on a computer that has the Hub Transport server role or Edge Transport server role installed. This configuration is used by the Connection Filter agent.

!!! Exchange Server 2013

This cmdlet is available or effective only on Edge Transport servers in on-premises Exchange Server 2013.

Use the Test-IPAllowListProvider cmdlet to test IP Allow list providers on Edge Transport servers.

!!! Exchange Server 2016

This cmdlet is available or effective only on Edge Transport servers in on-premises Exchange.

Use the Test-IPAllowListProvider cmdlet to test IP Allow list providers on Edge Transport servers.

## SYNTAX

```
Test-IPAllowListProvider [-Identity] <IPAllowListProviderIdParameter> -IPAddress <IPAddress> [-Confirm]
 [-DomainController <Fqdn>] [-Server <ServerIdParameter>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2010

The Test-IPAllowListProvider cmdlet checks connectivity to the specified IP Allow list provider and then issues a lookup request to the IP Allow list provider. When you test the connection and functionality of the IP Allow list provider, you must enter a known allowed IP address in the IPAddress parameter.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Anti-spam features" entry in the Transport Permissions topic.

!!! Exchange Server 2013

On Edge Transport servers, the Test-IPAllowListProvider cmdlet checks connectivity to the specified allow list provider and then issues a lookup request to the allow list provider.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Anti-spam features - Edge Transport" entry in the Anti-spam and anti-malware permissions topic.

!!! Exchange Server 2016

On Edge Transport servers, the Test-IPAllowListProvider cmdlet checks connectivity to the specified allow list provider and then issues a lookup request to the allow list provider.

On Edge Transport servers, you need to be a member of the local Administrators group to run this cmdlet.

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Test-IPAllowListProvider -IPAddress 192.168.0.1 -Identity ExampleProviderName
```

This example tests the connectivity to the fictitious IP Allow list provider ExampleProviderName, and then issues a lookup request to that provider using the IP address 192.168.0.1.

### Example 1 -------------------------- (Exchange Server 2013)
```
Test-IPAllowListProvider Contoso.com -IPAddress 192.168.0.1
```

This example tests the existing IP Allow list provider named Contoso,com by sending a lookup request to that provider for the IP address 192.168.0.1.

### Example 1 -------------------------- (Exchange Server 2016)
```
Test-IPAllowListProvider Contoso.com -IPAddress 192.168.0.1
```

This example tests the existing IP Allow list provider named Contoso,com by sending a lookup request to that provider for the IP address 192.168.0.1.

## PARAMETERS

### -Identity
!!! Exchange Server 2010

The Identity parameter specifies the IP Allow list provider name. The Identity parameter must match either the name or GUID of the IP Allow list provider that you want to test.



!!! Exchange Server 2013, Exchange Server 2016

The Identity parameter specifies the IP Allow list provider that you want to test. You can use any value that uniquely identifies the IP Allow list provider. For example:

- Name

- Distinguished name (DN)

- GUID



```yaml
Type: IPAllowListProviderIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: True
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -IPAddress
!!! Exchange Server 2010

The IPAddress parameter specifies an IP address to be used in testing the IP Allow list provider. The IPAddress parameter is used to verify and test the IP Allow list providers that you've configured.



!!! Exchange Server 2013, Exchange Server 2016

The IPAddress parameter specifies an IP address to be used in testing the IP Allow list provider. You need to use a known allowed IP address.



```yaml
Type: IPAddress
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: -Confirm:$false.

- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

The DomainController parameter isn't supported on Edge Transport servers. An Edge Transport server uses the local instance of Active Directory Lightweight Directory Services (AD LDS) to read and write data.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
!!! Exchange Server 2010

The Server parameter specifies the server on which you run the command. If you don't use the Server parameter, the command is run on the local server where the task is executed.



!!! Exchange Server 2013

The Server parameter specifies the Exchange server on which you want to run this command. You can use any value that uniquely identifies the server. For example:

- Name

- FQDN

- Distinguished name (DN)

- Exchange Legacy DN

If you don't use the Server parameter, the command is run on the local server.

You can't use this parameter to configure other Edge Transport servers remotely.



!!! Exchange Server 2016

The Server parameter specifies the Exchange server where you want to run this command. You can use any value that uniquely identifies the server. For example:

- Name

- FQDN

- Distinguished name (DN)

- Exchange Legacy DN

If you don't use this parameter, the command is run on the local server.

You can't use this parameter to configure other Edge Transport servers remotely.



```yaml
Type: ServerIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/921b36a2-21a5-48df-aa83-f9ea9c771787.aspx)

