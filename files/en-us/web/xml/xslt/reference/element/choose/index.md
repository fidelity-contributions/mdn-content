---
title: <xsl:choose>
slug: Web/XML/XSLT/Reference/Element/choose
page-type: xslt-element
sidebar: xmlsidebar
---

The `<xsl:choose>` element defines a choice among a number of alternatives. It behaves like a switch statement in procedural languages.

## Syntax

```xml
<xsl:choose>
  <xsl:when test="[whatever to test1]"></xsl:when>
  <xsl:when test="[whatever to test2]"></xsl:when>
  <xsl:otherwise></xsl:otherwise> [optional]
</xsl:choose>
```

### Required Attributes

None.

### Optional Attributes

None.

### Type

Instruction, appears with a template. It contains one or more `<xsl:when>` elements, and, optionally, a final `<xsl:otherwise>` element.

## Specifications

XSLT, section 9.2.

## Gecko support

Supported.
