---
author: brianlic-msft
description: 
external help file: NetLldpAgent.cdxml-help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: powershell
ms.technology: powershell
ms.topic: reference
online version: 
schema: 2.0.0
title: Get-NetLldpAgent
ms.assetid: 0CE124BA-BEBA-4676-AD3C-6FD3F0F30939
---

# Get-NetLldpAgent

## SYNOPSIS
Gets the settings of the LLDP agent on a network interface on a host computer.

## SYNTAX

### ByName (Default)
```
Get-NetLldpAgent [[-NetAdapterName] <String[]>] [[-AddressScope] <AddressScope[]>] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

### ByIfIndex
```
Get-NetLldpAgent [[-AddressScope] <AddressScope[]>] [[-InterfaceIndex] <UInt32[]>] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

## DESCRIPTION
The **Get-NetLldpAgent** cmdlet gets the settings of the Logical Link Discovery Protocol (LLDP) agent on a network interface on a host computer.

## EXAMPLES

### Example 1: Get LLDP agent settings on the local computer
```
PS C:\>Get-NetLldpAgent -NetAdapterName "Ethernet1"
```

This command gets LLDP agent settings on a network interface named Ethernet1 on the local computer.

## PARAMETERS

### -AddressScope
Specifies an array of neighbor scopes of the adapter for which this cmdlet gets the LLDP agent settings.
The acceptable values for this parameter are:

- NearestNeighbor 
- NearestNonTpmrBridge 
- NearestCustomerBridge

```yaml
Type: AddressScope[]
Parameter Sets: (All)
Aliases: 
Accepted values: NearestBridge, NearestNonTpmrBridge, NearestCustomerBridge

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InterfaceIndex
Specifies an array of indexes for which this cmdlet gets LLDP agent settings.

```yaml
Type: UInt32[]
Parameter Sets: ByIfIndex
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetAdapterName
Specifies an array of names of the interfaces for which this cmdlet gets LLDP agent settings.

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShell® calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Management.Infrastructure.CimInstance#root/StandardCimv2/MSFT_NetSettingData/MSFT_NetLldpMsap/MSFT_NetLldpAgent
This cmdlet retrieves the following settings: 

- Interface Alias
- Interface Index
- Scope
- MAC address

## NOTES

## RELATED LINKS

[Disable-NetLldpAgent](./Disable-NetLldpAgent.md)

[Enable-NetLldpAgent](./Enable-NetLldpAgent.md)
