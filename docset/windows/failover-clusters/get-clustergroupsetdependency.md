---
author: brianlic-msft
description: 
external help file: ClusterCollection.cdxml-help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: powershell
ms.technology: powershell
ms.topic: reference
online version: 
schema: 2.0.0
title: Get-ClusterGroupSetDependency
ms.assetid: FE91D170-66FA-483E-B0E9-3EBDAC60CFC0
---

# Get-ClusterGroupSetDependency

## SYNOPSIS
Gets the cluster group sets based on dependency relationships.

## SYNTAX

```
Get-ClusterGroupSetDependency [-ContainedGroup <String>] [-Name <String>] [-Provider <String>]
 [-DependentGroup <String>] [-CimSession <CimSession[]>] [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

## DESCRIPTION
The **Get-ClusterGroupSetDependency** cmdlet gets the cluster group sets based on dependency relationships.
You can get all sets that are dependent on a specific set.

## EXAMPLES

### Example 1: Get all the group sets that are provided by the specified set
```
PS C:\>Get-ClusterGroupSetDependency -Provider "Set2"

Name                : Set1
GroupNames          : {g1}
ProviderNames       : {Set2}
StartupDelayTrigger : Delay
StartupCount        : 4294967295
IsGlobal            : False
StartupDelay        : 20
```

This command gets all the group sets that are provided by set named Set2.

## PARAMETERS

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

### -ContainedGroup
Specifies the name of the group to get sets.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DependentGroup
Specifies the name of the group to get sets that are dependent on that group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the group set to get.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Provider
Specifies the name of the set that provides for the sets to get.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## NOTES

## RELATED LINKS

[Add-ClusterGroupSetDependency](./Add-ClusterGroupSetDependency.md)

[Remove-ClusterGroupSetDependency](./Remove-ClusterGroupSetDependency.md)
