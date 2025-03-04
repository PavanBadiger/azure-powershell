---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version:https://docs.microsoft.com/powershell/module/az.compute/add-azvmgalleryapplication
schema: 2.0.0
---

# Add-AzVmGalleryApplication

## SYNOPSIS
Add a GalleryApplication object to the PSVirtualMachine object.

## SYNTAX

```
Add-AzVmGalleryApplication -VM <PSVirtualMachine> -GalleryApplication <PSVMGalleryApplication> [-Order <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
Adds a GalleryApplication object to the PSVirtualMachine object.

## EXAMPLES

### Example 1
```powershell
PS C:\> $vm = Get-AzVm -ResourceGroupName $rgName -Name $vmName
PS C:\> $vmGal = New-AzVmGalleryApplication -PackageReferenceId $packageRefId -ConfigReferenceId $configRefId
PS C:\> Add-AzVmGalleryApplication -VM $vm -GalleryApplication $vmGal -Order 1
```

This example creates a local VMGalleryApplication object and adds it to a PSVirtualMachine object.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GalleryApplication
PSVMGalleryApplication Object.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVMGalleryApplication
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Order
Order in which the application will be install in.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
The PSVirtualMachine object to add a Gallery Application Reference ID.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTES

## RELATED LINKS
