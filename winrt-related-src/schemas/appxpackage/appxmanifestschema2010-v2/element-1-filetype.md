---
Description: A file type specified as its file type extension.
Search.Product: eADQiWindows 10XVcnh
title: 'FileType (type: ST_FileType)'
ms.assetid: f04c9bf7-2523-4d48-bdd0-f6b227af0a2d
author: laurenhughes
ms.author: lahugh
keywords: windows 10, uwp, schema, package manifest


ms.topic: reference
ms.date: 04/05/2017
---

# FileType (type: ST_FileType)




A file type specified as its file type extension. It is unique per application in the package and is case sensitive.

## Element hierarchy

<dl>
<dt><a href="element-extension.md">&lt;Extension&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-sharetarget.md">&lt;ShareTarget&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-1-supportedfiletypes.md">&lt;SupportedFileTypes&gt;</a></dt>
<dd><b>&lt;FileType&gt;</b></dd>
</dl>
</dd>
</dl>
<dl>
<dt><a href="element-fileopenpicker.md">&lt;FileOpenPicker&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-2-supportedfiletypes.md">&lt;SupportedFileTypes&gt;</a></dt>
<dd><b>&lt;FileType&gt;</b></dd>
</dl>
</dd>
</dl>
<dl>
<dt><a href="element-filesavepicker.md">&lt;FileSavePicker&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-3-supportedfiletypes.md">&lt;SupportedFileTypes&gt;</a></dt>
<dd><b>&lt;FileType&gt;</b></dd>
</dl>
</dd>
</dl>
</dd>
</dl>

## Syntax

``` syntax
<FileType>

  A string between 1 and 64 characters in length that must begin with a period ("."), cannot have additional periods, and cannot contain these characters: <, >, :, ", /, \, |, ?, or *.

</FileType>
```

## Attributes and Elements


### Attributes

None.

### Child Elements

None.

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
<td><a href="element-1-supportedfiletypes.md">SupportedFileTypes (type: CT_CharmsSupportedFileTypes)</a> </td>
<td><p>Defines the file types that the app can share.</p></td>
</tr>
</tbody>
</table>

 

## Related elements


The following elements have the same name as this one, but different content or attributes:

-   **[FileType (in type: CT_FTASupportedFileTypes)](element-filetype.md)**

## Examples

```XAML
<ShareTarget>
  <SupportedFileTypes>
    <FileType>.txt</FileType>
    <FileType>.html</FileType>
  </SupportedFileTypes>
  <DataFormat>Text</DataFormat>
  <DataFormat>Uri</DataFormat>
</ShareTarget>
```

## Requirements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>http://schemas.microsoft.com/appx/2010/manifest</p></td>
</tr>
</tbody>
</table>

 

 



