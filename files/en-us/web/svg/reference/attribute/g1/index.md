---
title: g1
slug: Web/SVG/Reference/Attribute/g1
page-type: svg-attribute
status:
  - deprecated
browser-compat: svg.elements.hkern.g1
sidebar: svgref
---

{{Deprecated_Header}}

The **`g1`** attribute specifies a list of glyph names which identify a set of possible first glyphs in the kerning pair.

All glyphs with the given glyph name are included in the set. The total set of possible first glyphs in the kerning pair is the union of glyphs specified by the {{SVGAttr("u1")}} and `g1` attributes.

You can use this attribute with the following SVG elements:

- {{SVGElement("hkern")}}
- {{SVGElement("vkern")}}

## Context notes

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Value</th>
      <td>
        <code
          >&#x3C;name><a
            href="/en-US/docs/Web/CSS/CSS_Values_and_Units/Value_definition_syntax#hash_mark"
            >#</a
          ></code
        >
      </td>
    </tr>
    <tr>
      <th scope="row">Default value</th>
      <td><em>None</em></td>
    </tr>
    <tr>
      <th scope="row">Animatable</th>
      <td>No</td>
    </tr>
  </tbody>
</table>

- `<name>#`
  - : This value indicates a comma-separated sequence of glyph names (i.e., values that match {{SVGAttr("glyph-name")}} attributes on {{SVGElement("glyph")}} elements) which identify a set of possible first glyphs in the kerning pair.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
