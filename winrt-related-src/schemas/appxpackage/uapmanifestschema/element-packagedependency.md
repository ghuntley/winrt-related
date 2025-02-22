---
Description: Declares a dependency on another package that is marked as a framework package.
Search.Product: eADQiWindows 10XVcnh
title: PackageDependency (Windows 10)
ms.assetid: 7f0800a1-f1dd-48c2-aba0-3701dd27d383
author: laurenhughes
ms.author: lahugh
keywords: windows 10, uwp, schema, package manifest


ms.topic: reference
ms.date: 04/10/2018
---

# PackageDependency (Windows 10)


Declares a dependency on another package that is marked as a framework package.

## Element hierarchy

<dl>
<dt><a href="element-package.md">&lt;Package&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-dependencies.md">&lt;Dependencies&gt;</a></dt>
<dd><b>&lt;PackageDependency&gt;</b></dd>
</dl>
</dd>
</dl>

## Syntax

``` syntax
<PackageDependency Name                   = A string between 3 and 50 characters in length that consists of alpha-numeric, period, and dash characters.
                   Publisher              = A string between 1 and 8192 characters in length that fits the regular expression  of a distinguished name : "(CN | L | O | OU | E | C | S | STREET | T | G | I | SN | DC | SERIALNUMBER | Description | PostalCode | POBox | Phone | X21Address | dnQualifier | (OID\.(0 | [1-9][0-9]*)(\.(0 | [1-9][0-9]*))+))=(([^,+="<>#;])+ | ".*")(, ((CN | L | O | OU | E | C | S | STREET | T | G | I | SN | DC | SERIALNUMBER | Description | PostalCode | POBox | Phone | X21Address | dnQualifier | (OID\.(0 | [1-9][0-9]*)(\.(0 | [1-9][0-9]*))+))=(([^,+="<>#;])+ | ".*")))*". Further, semantic validation ensures that the string is compliant with CertNameToStr Windows API implementation of X.500 rules.
                   MinVersion             = A version string in quad notation, "Major.Minor.Build.Revision".
                   MaxMajorVersionTested? = unsignedShort
                   uap6:Optional? = Boolean />
```

### Key

`?`   optional (zero or one)

## Attributes and Elements


### Attributes

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribute</th>
<th>Description</th>
<th>Data type</th>
<th>Required</th>
<th>Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MaxMajorVersionTested</strong></td>
<td><p>The maximum version of the dependency package tested against. Used to determine whether frameworks will be staged side-by-side, and what framework gets loaded into the package graph for the package.</p></td>
<td>unsignedShort</td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td><strong>MinVersion</strong></td>
<td><p>The minimum version of the dependency package.</p></td>
<td>A version string in quad notation, &quot;Major.Minor.Build.Revision&quot;.</td>
<td>Yes</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>Name</strong></td>
<td><p>The name as it appears in the <strong>Name</strong> attribute of the <a href="element-identity.md"><strong>Identity</strong></a>  element of the dependency package.</p></td>
<td>A string between 3 and 50 characters in length that consists of alpha-numeric, period, and dash characters.</td>
<td>Yes</td>
<td></td>
</tr>
<tr class="even">
<td><strong>uap6:Optional</strong></td>
<td><p>Indicates that a framework package dependency is optional for the app, meaning the app can be installed even if the optional framework dependencies are not installed.</p></td>
<td>Boolean</td>
<td>No</td>
<td>False</td>
</tr>
<tr class="odd">
<td><strong>Publisher</strong></td>
<td><p>The publisher as it appears in the <strong>Publisher</strong> attribute of the <a href="element-identity.md"><strong>Identity</strong></a>  element of the dependency package.</p></td>
<td>A string between 1 and 8192 characters in length that fits the regular expression of a distinguished name : &quot;(CN | L | O | OU | E | C | S | STREET | T | G | I | SN | DC | SERIALNUMBER | Description | PostalCode | POBox | Phone | X21Address | dnQualifier | (OID\.(0 | [1-9][0-9]*)(\.(0 | [1-9][0-9]*))+))=(([^,+=&quot;&lt;&gt;#;])+ | &quot;.*&quot;)(, ((CN | L | O | OU | E | C | S | STREET | T | G | I | SN | DC | SERIALNUMBER | Description | PostalCode | POBox | Phone | X21Address | dnQualifier | (OID\.(0 | [1-9][0-9]*)(\.(0 | [1-9][0-9]*))+))=(([^,+=&quot;&lt;&gt;#;])+ | &quot;.*&quot;)))*&quot;. Further, semantic validation ensures that the string is compliant with CertNameToStr Windows API implementation of X.500 rules.</td>
<td>Yes</td>
<td></td>
</tr>
</tbody>
</table>

 

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
<td><a href="element-dependencies.md">Dependencies</a> </td>
<td><p>Declares other packages that a package depends on to complete its software.</p></td>
</tr>
</tbody>
</table>

 

## Remarks

When working with package dependencies note the following:

-   A package cannot have multiple dependency declarations that have the same **Name** attribute.
-   If the **Publisher** attribute is not specified, then the dependency package must be unsigned. When a dependency package is unsigned it must also be marked as a framework package. See the [**Framework**](element-framework.md) element.
-   The version of the dependency package must be greater than or equal to the minimum version specified by this attribute.

## Examples

```XML
<Dependencies>
    <PackageDependency Name="Microsoft.WinJS.1.0"
      Publisher="CN=Microsoft Corporation, O=Microsoft Corporation, L=Redmond, S=Washington, C=US"
      MinVersion="1.0.0.0"/>    
</Dependencies>
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
<td><p>http://schemas.microsoft.com/appx/manifest/foundation/windows10</p></td>
</tr>
</tbody>
</table>

 

 



