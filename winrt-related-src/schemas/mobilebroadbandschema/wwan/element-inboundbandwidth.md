---
Description: Defines a value representing the effective link speed of the subscriber’s inbound connection.
Search.Product: eADQiWindows 10XVcnh
title: InboundBandwidth
ms.assetid: a754547a-eeb5-4397-b3a9-7640886394d4
author: mcleblanc
ms.author: markl
keywords: windows 10, uwp, schema, mobile broadband schema


ms.topic: reference
ms.date: 04/05/2017
---

# InboundBandwidth


Defines a value representing the effective link speed of the subscriber’s inbound connection.

## Element hierarchy

<dl>
<dt><a href="element-messages.md">&lt;Messages&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-message.md">&lt;Message&gt;</a></dt>
<dd>
<dl>
<dt><a href="element-fields.md">&lt;Fields&gt;</a></dt>
<dd><b>&lt;InboundBandwidth&gt;</b></dd>
</dl>
</dd>
</dl>
</dd>
</dl>

## Syntax

``` syntax
<InboundBandwidth Group        = positiveInteger
                  UnitGroup?   = positiveInteger
                  DefaultUnit? = "None" | "K" | "M" | "G" | "T" | ... />
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
<td><strong>DefaultUnit</strong></td>
<td><p>Defines the default unit multiplier of <strong>Group</strong> if <strong>UnitGroup</strong> is not present or no token matches. Units are powers of:</p>
<ul>
<li>None</li>
<li>K - 1,000</li>
<li>M - 1,000,000</li>
<li>G - 1,000,000,000</li>
<li>T - 1,000,000,000,000</li>
<li>Ki - 1,024</li>
<li>Mi - 1,048,576</li>
<li>Gi - 1,073,741,824</li>
<li>Ti - 1,099,511,627,776</li>
</ul></td>
<td><p>This attribute can have one of the following values:</p>
<ul>
<li>None</li>
<li>K</li>
<li>M</li>
<li>G</li>
<li>T</li>
<li>Ki</li>
<li>Mi</li>
<li>Gi</li>
<li>Ti</li>
</ul></td>
<td>No</td>
<td></td>
</tr>
<tr class="even">
<td><strong>Group</strong></td>
<td><p>Defines the group that contains the data limit. This must be a number formatted per the specified <a href="https://msdn.microsoft.com/library/windows/apps/hh868459"><strong>Locale</strong></a> .</p></td>
<td>positiveInteger</td>
<td>Yes</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>UnitGroup</strong></td>
<td><p>Defines the group that specifies units for the data limit. The contents of this group are compared to tokens in <a href="https://msdn.microsoft.com/library/windows/apps/hh868476"><strong>Units</strong></a> . If no match is found, the value of <strong>DefaultUnit</strong> will be used instead. The content of <strong>Group</strong> will be multiplied by this value before being used.</p></td>
<td>positiveInteger</td>
<td>No</td>
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
<td><a href="element-fields.md">Fields</a> </td>
<td><p>Defines values that describe the subscriber's plan and data usage.</p></td>
</tr>
</tbody>
</table>

 

## Remarks

If absent, **InboundBandwidth** is not inferred.

## Requirements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>http://www.microsoft.com/networking/CarrierControl/WWAN/v1</p></td>
</tr>
</tbody>
</table>

 

 



