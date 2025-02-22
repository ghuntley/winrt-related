---
Description: Declares an app extensibility point of type windows.autoPlayDevice.
Search.Product: eADQiWindows 10XVcnh
title: uap:AutoPlayDevice (Windows 10)
ms.assetid: ae471158-7ec0-4f6c-b681-76323317ac0d
author: laurenhughes
ms.author: lahugh
keywords: windows 10, uwp, schema, package manifest


ms.topic: reference
ms.date: 04/05/2017
---

# uap:AutoPlayDevice (Windows 10)


Declares an app extensibility point of type **windows.autoPlayDevice**. The app provides the specified AutoPlay device actions.

## Element hierarchy

<dl>
<dt><a href="element-package.md">&lt;Package&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-applications.md">&lt;Applications&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-application.md">&lt;Application&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-1-extensions.md">&lt;Extensions&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-uap-extension.md">&lt;uap:Extension&gt;</a></dt>
<dd><b>&lt;uap:AutoPlayDevice&gt;</b></dd>
</dl>
</dd>
</dl>
</dd>
</dl>
</dd>
</dl>
</dd>
</dl>

## Syntax

``` syntax
<AutoPlayDevice>

  <!-- Child elements -->
  uap:LaunchAction{1,1000}

</uap:AutoPlayDevice>
```

### Key

`{}`   specific range of occurrences
## Attributes and Elements


### Attributes

None.

### Child Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Child Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-1-uap-launchaction.md">uap:LaunchAction (in type: CT_AutoPlayDevice)</a> </td>
<td><p>Describes an AutoPlay device action.</p></td>
</tr>
</tbody>
</table>

 

### Parent Elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parent Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-uap-extension.md">uap:Extension</a> </td>
<td><p>Declares an extensibility point for the app.</p></td>
</tr>
</tbody>
</table>

 

## Remarks

When a device that is not volume-based is connected to a computer, the system raises an AutoPlay device event. This extensibility point enables your app to be listed as an AutoPlay choice for one or more AutoPlay device events. Because these devices are not volume-based, the system provides the app with device information rather than a file folder.

## Examples

```XML
<uap:Extension Category="windows.autoPlayDevice">
  <uap:AutoPlayDevice>
    <uap:LaunchAction Verb="startDeviceApp" ActionDisplayName="Start my device app" DeviceEvent="CustomDeviceEvent"/>
  </uap:AutoPlayDevice>
</uap:Extension>
```

## See also


**Tasks**
[Auto-launching with AutoPlay](https://msdn.microsoft.com/library/windows/apps/hh452731)

**Concepts**
[App contracts and extensions](https://msdn.microsoft.com/library/windows/apps/hh464906)

## Requirements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>http://schemas.microsoft.com/appx/manifest/uap/windows10</p></td>
</tr>
</tbody>
</table>

 

 



