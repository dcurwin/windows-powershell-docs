---
ms.mktglfcycl: manage
ms.sitesec: library
ms.author: brianlic
author: brianlic-msft
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file: HgsClient-help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 12/20/2016
ms.prod: w10
ms.technology: powershell-windows
ms.topic: reference
online version: 
schema: 2.0.0
title: Set-HgsClientConfiguration
ms.assetid: 0C150F6E-C13B-49D7-8FE5-AE197AB49038
---

# Set-HgsClientConfiguration

## SYNOPSIS
Modifies the configuration of a Host Guardian Service client.

## SYNTAX

### ChangeToLocalMode
```
Set-HgsClientConfiguration [-EnableLocalMode] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SecureHostingServiceMode
```
Set-HgsClientConfiguration -KeyProtectionServerUrl <String> -AttestationServerUrl <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-HgsClientConfiguration** cmdlet modifies the configuration of a Host Guardian Service client.
You can configure the client in either local mode or Host Guardian Service mode.
In local mode, there is no attestation and the client keeps key material.

## EXAMPLES

### Example 1: Set an attestation and key protection servers
```
PS C:\> Set-HgsClientConfiguration -AttestationServerUrl "https://DemoHgs.Contoso.com/Attestation" -KeyProtectionServerUrl "https://DemoHgs.Contoso.com/KeyProtection"
```

This command configures the URLs used by the attestation client and the key protection client.
Use this command to configure the local host to run in Host Guardian Service mode.

### Example 2: Change the mode to Local
```
PS C:\> Set-HgsClientConfiguration -EnableLocalMode
```

This command changes the Host Guardian Service client from Host Guardian Service mode to Local mode.
This command resets the attestation server URL and the key protection server URL.

## PARAMETERS

### -AttestationServerUrl
Specifies the URL of an attestation server.
A Host Guardian Service client in Secure Hosting Service mode uses the server that this parameter specifies.

```yaml
Type: String
Parameter Sets: SecureHostingServiceMode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableLocalMode
Indicates that this cmdlet changes the mode of client from Host Guardian Service to Local mode.
A change in mode to Local resets the attestation server and key protection server URLs.

```yaml
Type: SwitchParameter
Parameter Sets: ChangeToLocalMode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyProtectionServerUrl
Specifies the URL of a key protection server server.
A Host Guardian Service client in Secure Hosting Service mode uses the server that this parameter specifies.

```yaml
Type: String
Parameter Sets: SecureHostingServiceMode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### CimInstance#MSFT_HgsClientConfiguration
The `Microsoft.Management.Infrastructure.CimInstance` object is a wrapper class that displays Windows Management Instrumentation (WMI) objects.
The path after the pound sign (`#`) provides the namespace and class name for the underlying WMI object.

## NOTES

## RELATED LINKS

[Get-HgsClientConfiguration](./Get-HgsClientConfiguration.md)
