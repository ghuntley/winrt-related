﻿---
Description: Indicates whether...
title: desktop6:RegistryWriteVirtualization
author: mcleanbyron
ms.author: mcleans
keywords: windows 10, uwp, schema, package manifest


ms.topic: reference
ms.date: 04/19/2019
ms.custom: 19H1
---

# desktop6:RegistryWriteVirtualization

Indicates whether virtualization for the registry is enabled for your desktop application. If disabled, other apps can read or write the same registry entries as your application. This element is currently intended to be used only by certain types of desktop PC games that are published by Microsoft and our partners.

## Element hierarchy

<dl>
<dt><a href="element-package.md">&lt;Package&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-properties.md">&lt;Properties&gt;</a></dt>
<dd><b>&lt;desktop6:RegistryWriteVirtualization&gt;</b></dd>
</dl>
</dd>
</dl>

## Syntax

``` xml
<desktop6:RegistryWriteVirtualization>disabled</desktop6:RegistryWriteVirtualization>
```

## Value

This element can have the value **enabled** or **disabled**. The default is **enabled**. 

## Attributes and Elements


### Attributes

None.

### Child Elements

None.

### Parent Elements

| Parent Element | Description |
|---------------|-------------|
| [Properties](element-properties.md) | Defines additional metadata about the package including attributes that describe how the package appears to users.  |

## Remarks

This element requires the **unvirtualizedResources** [restricted capability](https://docs.microsoft.com/windows/uwp/packaging/app-capability-declarations#restricted-capabilities).

## Requirements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>http://schemas.microsoft.com/appx/manifest/desktop/windows10/6</p></td>
</tr>
</tbody>
</table>

 

 



