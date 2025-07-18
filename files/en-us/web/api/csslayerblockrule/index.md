---
title: CSSLayerBlockRule
slug: Web/API/CSSLayerBlockRule
page-type: web-api-interface
browser-compat: api.CSSLayerBlockRule
---

{{APIRef("CSSOM")}}

The **`CSSLayerBlockRule`** represents a {{cssxref("@layer")}} block rule.

{{InheritanceDiagram}}

## Instance properties

_Inherits properties from its ancestors {{domxref("CSSGroupingRule")}} and {{domxref("CSSRule")}}._

- {{DOMxRef("CSSLayerBlockRule.name")}} {{ReadOnlyInline}}
  - : A string containing the name of the associated cascade layer.

## Instance methods

_Inherits methods from its ancestors {{domxref("CSSGroupingRule")}} and {{domxref("CSSRule")}}._

## Examples

### HTML

```html
<p>I am displayed in <code>color: rebeccapurple</code>.</p>
```

### CSS

```css
@layer special {
  p {
    color: rebeccapurple;
  }
}
```

### JavaScript

```js
const item = document.getElementsByTagName("p")[0];
const rules = document.styleSheets[1].cssRules;
// Note that stylesheet #1 is the stylesheet associated with this embedded example,
// while stylesheet #0 is the stylesheet associated with the whole MDN page

const layer = rules[0]; // A CSSLayerBlockRule

item.textContent = `The CSSLayerBlockRule is for the "${layer.name}" layer`;
```

### Result

{{EmbedLiveSample("Examples")}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{cssxref("@layer")}}
- {{DOMxRef("CSSLayerStatementRule")}}
- [Learn CSS cascade layers](/en-US/docs/Learn_web_development/Core/Styling_basics/Cascade_layers)
