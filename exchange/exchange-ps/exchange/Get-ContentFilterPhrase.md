---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016
schema: 2.0.0
---

# Get-ContentFilterPhrase

## SYNOPSIS
!!! Exchange Server 2010

Use the Get-ContentFilterPhrase cmdlet to view one or all custom words that the Content Filter agent processes.

!!! Exchange Server 2013, Exchange Server 2016

This cmdlet is available only in on-premises Exchange.

Use the Get-ContentFilterPhrase cmdlet to view one or all custom words that the Content Filter agent processes.

## SYNTAX

### Set1
```
Get-ContentFilterPhrase [[-Identity] <ContentFilterPhraseIdParameter>] [-DomainController <Fqdn>]
 [<CommonParameters>]
```

### Set2
```
Get-ContentFilterPhrase [-DomainController <Fqdn>] [-Phrase <ContentFilterPhraseIdParameter>]
 [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2010

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Anti-spam features" entry in the Transport Permissions topic.

!!! Exchange Server 2013

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Anti-spam features" entry in the Anti-spam and anti-malware permissions topic.

!!! Exchange Server 2016

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Get-ContentFilterPhrase
```

This example returns all custom words stored on the computer where the command is being run.

### Example 1 -------------------------- (Exchange Server 2013)
```
Get-ContentFilterPhrase
```

This example returns all custom words stored on the computer where the command is being run.

### Example 1 -------------------------- (Exchange Server 2016)
```
Get-ContentFilterPhrase
```

This example returns all custom words stored on the computer where the command is being run.

### Example 2 -------------------------- (Exchange Server 2010)
```
Get-ContentFilterPhrase -Phrase "Free credit report"
```

This example returns a specific custom word specified by the Phrase parameter. In this example, the custom word is the phrase Free credit report.

### Example 2 -------------------------- (Exchange Server 2013)
```
Get-ContentFilterPhrase -Phrase "Free credit report"
```

This example returns a specific custom word specified by the Phrase parameter. In this example, the custom word is the phrase Free credit report.

### Example 2 -------------------------- (Exchange Server 2016)
```
Get-ContentFilterPhrase -Phrase "Free credit report"
```

This example returns a specific custom word specified by the Phrase parameter. In this example, the custom word is the phrase Free credit report.

### Example 3 -------------------------- (Exchange Server 2010)
```
Get-ContentFilterPhrase | Where {$_.Phrase -like '*free offer*'}
```

This example returns all custom words and phrases that contain the words free offer.

### Example 3 -------------------------- (Exchange Server 2013)
```
Get-ContentFilterPhrase | Where {$_.Phrase -like '*free offer*'}
```

This example returns all custom words and phrases that contain the words free offer.

### Example 3 -------------------------- (Exchange Server 2016)
```
Get-ContentFilterPhrase | Where {$_.Phrase -like '*free offer*'}
```

This example returns all custom words and phrases that contain the words free offer.

## PARAMETERS

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

### -Identity
The Identity parameter specifies a custom word or phrase to display. You must enclose the value of the Identity parameter in quotation marks (").

The Identity and Phrase parameters are interchangeable.

```yaml
Type: ContentFilterPhraseIdParameter
Parameter Sets: Set1
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016

Required: False
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Phrase
The Phrase parameter specifies a custom word or phrase to display. You must enclose the value of the Phrase parameter in quotation marks (").

The Phrase and Identity parameters are interchangeable.

```yaml
Type: ContentFilterPhraseIdParameter
Parameter Sets: Set2
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

[Online Version](https://technet.microsoft.com/library/22af0f6c-00f7-4fe5-9ff8-c63305adb9bc.aspx)

