---
title: DEVPKEY_DrvPkg_DetailedDescription
description: DEVPKEY_DrvPkg_DetailedDescription
ms.assetid: ee9080d1-8c66-42b3-af48-cb1fbfc332e2
keywords: ["DEVPKEY_DrvPkg_DetailedDescription Device and Driver Installation"]
topic_type:
- apiref
api_name:
- DEVPKEY_DrvPkg_DetailedDescription
api_location:
- Devpkey.h
api_type:
- HeaderDef
---

# DEVPKEY_DrvPkg_DetailedDescription


The DEVPKEY_DrvPkg_DetailedDescription device property represents a detailed description of the capabilities of a device instance.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Property key</strong></p></td>
<td align="left"><p>DEVPKEY_DrvPkg_DetailedDescription</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Property-data-type identifier</strong></p></td>
<td align="left"><p>[<strong>DEVPROP_TYPE_STRING</strong>](devprop-type-string.md)</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Data format</strong></p></td>
<td align="left"><p>Limited set of XML tags</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Property access</strong></p></td>
<td align="left"><p>Read-only access by installation applications and installers</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Localized?</strong></p></td>
<td align="left"><p>Yes</p></td>
</tr>
</tbody>
</table>

 

Remarks
-------

The detailed description string is in XML format. XML format makes it possible for Windows to format the display of the information based on the following subset of supported Hypertext Markup Language (HTML) tags. The operation of these tags resembles the operation of HTML tags.

<a href="" id="heading-level-tags"></a>Heading level tags  
&lt;h1&gt;, &lt;h2&gt;, &lt;h3&gt;

<a href="" id="list-tags"></a>List tags  
&lt;ul&gt;, &lt;ol&gt;, &lt;li&gt;

<a href="" id="paragraph-tag"></a>Paragraph tag  
&lt;p&gt;

You can set the value of DEVPKEY_DrvPkg_DetailedDescription by an [**INF AddProperty directive**](https://msdn.microsoft.com/library/windows/hardware/ff546318) that is included in the [**INF *DDInstall* section**](https://msdn.microsoft.com/library/windows/hardware/ff547344) of the INF file that installs the device. You can retrieve the value of DEVPKEY_DrvPkg_DetailedDescription by calling [**SetupDiGetDeviceProperty**](https://msdn.microsoft.com/library/windows/hardware/ff551963).

The following is an example of how to use an INF **AddProperty** directive to set the value of DEVPKEY_DrvPkg_DetailedDescription for a device instance that is installed by an INF *DDInstall* section "SampleDDInstallSection":

```
[SampleDDinstallSection]
...
AddProperty=SampleAddPropertySection
...

[SampleAddPropertySection] 
DeviceDetailedDescription,,,,"<xml><h1>Microsoft DiscoveryCam 530</h1><h2>Overview<h2>The Microsoft DiscoveryCam is great.<p>Really.<p><h2>Features</h2>The Microsoft DiscoveryCam has three features.<ol><li>Feature 1</li><li>Feature 2</li><li>Feature 3</li></ol></xml>"
...
```

Requirements
------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Version</p></td>
<td align="left"><p>Available in Windows Vista and later versions of Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Header</p></td>
<td align="left">Devpkey.h (include Devpkey.h)</td>
</tr>
</tbody>
</table>

## See also


[**INF AddProperty Directive**](https://msdn.microsoft.com/library/windows/hardware/ff546318)

[**INF *DDInstall* Section**](https://msdn.microsoft.com/library/windows/hardware/ff547344)

[**SetupDiGetDeviceProperty**](https://msdn.microsoft.com/library/windows/hardware/ff551963)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20DEVPKEY_DrvPkg_DetailedDescription%20%20RELEASE:%20%2810/9/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





