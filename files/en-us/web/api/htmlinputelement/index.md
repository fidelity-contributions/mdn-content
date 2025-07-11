---
title: HTMLInputElement
slug: Web/API/HTMLInputElement
page-type: web-api-interface
browser-compat: api.HTMLInputElement
---

{{APIRef("HTML DOM")}}

The **`HTMLInputElement`** interface provides special properties and methods for manipulating the options, layout, and presentation of {{HTMLElement("input")}} elements.

{{InheritanceDiagram}}

## Instance properties

_Also inherits properties from its parent interface, {{domxref("HTMLElement")}}._

Some properties only apply to input element types that support the corresponding attributes.

- {{domxref("HTMLInputElement.align", "align")}} {{Deprecated_Inline}}
  - : A string that represents the alignment of the element. _Use CSS instead._

- {{domxref("HTMLInputElement.defaultValue", "defaultValue")}}
  - : A string that represents the default value as originally specified in the HTML that created this object.

- {{domxref("HTMLInputElement.dirName", "dirName")}}
  - : A string that represents the directionality of the element.

- {{domxref("HTMLInputElement.incremental", "incremental")}} {{Non-standard_Inline}}
  - : A boolean that represents the search event fire mode, if `true`, fires on every keypress, or on clicking the cancel button; otherwise fires when pressing <kbd>Enter</kbd>.

- {{domxref("HTMLInputElement.labels", "labels")}} {{ReadOnlyInline}}
  - : Returns a list of {{ HTMLElement("label") }} elements that are labels for this element.

- {{domxref("HTMLInputElement.list", "list")}} {{ReadOnlyInline}}
  - : Returns the element pointed to by the [`list`](/en-US/docs/Web/HTML/Reference/Elements/input#list) attribute. The property may be `null` if no HTML element is found in the same tree.

- {{domxref("HTMLInputElement.multiple", "multiple")}}
  - : A boolean that represents the element's [`multiple`](/en-US/docs/Web/HTML/Reference/Elements/input#multiple) attribute, indicating whether more than one value is possible (e.g., multiple files).

- {{domxref("HTMLInputElement.name", "name")}}
  - : A string that represents the element's [`name`](/en-US/docs/Web/HTML/Reference/Elements/input#name) attribute, containing a name that identifies the element when submitting the form.

- {{domxref("HTMLInputElement.popoverTargetAction", "popoverTargetAction")}}
  - : Gets and sets the action to be performed (`"hide"`, `"show"`, or `"toggle"`) on a popover element being controlled by an {{HTMLElement("input")}} element of `type="button"`. It reflects the value of the [`popovertargetaction`](/en-US/docs/Web/HTML/Reference/Elements/input#popovertargetaction) HTML attribute.

- {{domxref("HTMLInputElement.popoverTargetElement", "popoverTargetElement")}}
  - : Gets and sets the popover element to control via an {{HTMLElement("input")}} element of `type="button"`. The JavaScript equivalent of the [`popovertarget`](/en-US/docs/Web/HTML/Reference/Elements/input#popovertarget) HTML attribute.

- {{domxref("HTMLInputElement.step", "step")}}
  - : A string that represents the element's [`step`](/en-US/docs/Web/HTML/Reference/Elements/input#step) attribute, which works with [`min`](/en-US/docs/Web/HTML/Reference/Elements/input#min) and [`max`](/en-US/docs/Web/HTML/Reference/Elements/input#max) to limit the increments at which a numeric or date-time value can be set. It can be the string `any` or a positive floating point number. If this is not set to `any`, the control accepts only values at multiples of the step value greater than the minimum.

- {{domxref("HTMLInputElement.type", "type")}}
  - : A string that represents the element's [`type`](/en-US/docs/Web/HTML/Reference/Elements/input#type) attribute, indicating the type of control to display. For possible values, see the documentation for the [`type`](/en-US/docs/Web/HTML/Reference/Elements/input#type) attribute.

- {{domxref("HTMLInputElement.useMap", "useMap")}} {{Deprecated_Inline}}
  - : A string that represents a client-side image map.

- {{domxref("HTMLInputElement.value", "value")}}
  - : A string that represents the current value of the control. If the user enters a value different from the value expected, this may return an empty string.

- {{domxref("HTMLInputElement.valueAsDate", "valueAsDate")}}
  - : A {{jsxref("Date")}} that represents the value of the element, interpreted as a date, or `null` if conversion is not possible.

- {{domxref("HTMLInputElement.valueAsNumber", "valueAsNumber")}}
  - : A number that represents the value of the element, interpreted as one of the following, in order: A time value, a number, or `NaN` if conversion is impossible.

### Instance properties related to the parent form

- {{domxref("HTMLInputElement.form", "form")}} {{ReadOnlyInline}}
  - : Returns a reference to the parent {{HTMLElement("form")}} element.

- {{domxref("HTMLInputElement.formAction", "formAction")}}
  - : A string that represents the element's [`formaction`](/en-US/docs/Web/HTML/Reference/Elements/input#formaction) attribute, containing the URL of a program that processes information submitted by the element. This overrides the [`action`](/en-US/docs/Web/HTML/Reference/Elements/form#action) attribute of the parent form.

- {{domxref("HTMLInputElement.formEnctype", "formEnctype")}}
  - : A string that represents the element's [`formenctype`](/en-US/docs/Web/HTML/Reference/Elements/input#formenctype) attribute, containing the type of content that is used to submit the form to the server. This overrides the [`enctype`](/en-US/docs/Web/HTML/Reference/Elements/form#enctype) attribute of the parent form.

- {{domxref("HTMLInputElement.formMethod", "formMethod")}}
  - : A string that represents the element's [`formmethod`](/en-US/docs/Web/HTML/Reference/Elements/input#formmethod) attribute, containing the HTTP method that the browser uses to submit the form. This overrides the [`method`](/en-US/docs/Web/HTML/Reference/Elements/form#method) attribute of the parent form.

- {{domxref("HTMLInputElement.formNoValidate", "formNoValidate")}}
  - : A boolean that represents the element's [`formnovalidate`](/en-US/docs/Web/HTML/Reference/Elements/input#formnovalidate) attribute, indicating that the form is not to be validated when it is submitted. This overrides the [`novalidate`](/en-US/docs/Web/HTML/Reference/Elements/form#novalidate) attribute of the parent form.

- {{domxref("HTMLInputElement.formTarget", "formTarget")}}
  - : A string that represents the element's [`formtarget`](/en-US/docs/Web/HTML/Reference/Elements/input#formtarget) attribute, containing a name or keyword indicating where to display the response that is received after submitting the form. This overrides the [`target`](/en-US/docs/Web/HTML/Reference/Elements/form#target) attribute of the parent form.

### Instance properties that apply to any type of input element that is not hidden

- {{domxref("HTMLInputElement.disabled", "disabled")}}
  - : A boolean that represents the element's [`disabled`](/en-US/docs/Web/HTML/Reference/Elements/input#disabled) attribute, indicating that the control is not available for interaction. The input values will not be submitted with the form. See also [`readonly`](/en-US/docs/Web/HTML/Reference/Elements/input#readonly).

- {{domxref("HTMLInputElement.required", "required")}}
  - : A boolean that represents the element's [`required`](/en-US/docs/Web/HTML/Reference/Elements/input#required) attribute, indicating that the user must fill in a value before submitting a form.

- {{domxref("HTMLInputElement.validationMessage", "validationMessage")}} {{ReadOnlyInline}}
  - : Returns a localized message that describes the validation constraints that the control does not satisfy (if any). This is the empty string if the control is not a candidate for constraint validation ({{domxref("HTMLInputElement.willValidate", "willValidate")}} is `false`), or it satisfies its constraints. This value can be set by the {{domxref("HTMLInputElement.setCustomValidity()", "setCustomValidity()")}} method.

- {{domxref("HTMLInputElement.validity", "validity")}} {{ReadOnlyInline}}
  - : Returns the element's current validity state.

- {{domxref("HTMLInputElement.willValidate", "willValidate")}} {{ReadOnlyInline}}
  - : Returns whether the element is a candidate for constraint validation. It is `false` if any conditions bar it from constraint validation, including: its `type` is one of `hidden`, `reset` or `button`, it has a {{HTMLElement("datalist")}} ancestor or its `disabled` property is `true`.

### Instance properties that apply only to elements of type checkbox or radio

- {{domxref("HTMLInputElement.checked", "checked")}}
  - : A boolean that represents the current state of the element.

- {{domxref("HTMLInputElement.defaultChecked", "defaultChecked")}}
  - : A boolean that represents the default state of a radio button or checkbox as originally specified in HTML that created this object.

- {{domxref("HTMLInputElement.indeterminate", "indeterminate")}}
  - : A boolean that represents whether the checkbox or radio button is in indeterminate state. For checkboxes, the effect is that the appearance of the checkbox is obscured/greyed in some way as to indicate its state is indeterminate (not checked but not unchecked). Does not affect the value of the `checked` attribute, and clicking the checkbox will set the value to false.

### Instance properties that apply only to elements of type image

- {{domxref("HTMLInputElement.alt", "alt")}}
  - : A string that represents the element's [`alt`](/en-US/docs/Web/HTML/Reference/Elements/input#alt) attribute, containing alternative text to use.

- {{domxref("HTMLInputElement.height", "height")}}
  - : A string that represents the element's [`height`](/en-US/docs/Web/HTML/Reference/Elements/input#height) attribute, which defines the height of the image displayed for the button.

- {{domxref("HTMLInputElement.src", "src")}}
  - : A string that represents the element's [`src`](/en-US/docs/Web/HTML/Reference/Elements/input#src) attribute, which specifies a URI for the location of an image to display on the graphical submit button.

- {{domxref("HTMLInputElement.width", "width")}}
  - : A string that represents the element's [`width`](/en-US/docs/Web/HTML/Reference/Elements/input#width) attribute, which defines the width of the image displayed for the button.

### Instance properties that apply only to elements of type file

- {{domxref("HTMLInputElement.accept", "accept")}}
  - : A string that represents the element's [`accept`](/en-US/docs/Web/HTML/Reference/Elements/input#accept) attribute, containing comma-separated list of file types that can be selected.

- {{domxref("HTMLInputElement.capture", "capture")}}
  - : A string that represents the element's [`capture`](/en-US/docs/Web/HTML/Reference/Elements/input#capture) attribute, indicating the media capture input method in file upload controls.

- {{domxref("HTMLInputElement.files", "files")}}
  - : A {{domxref("FileList")}} that represents the files selected for upload.

- {{domxref("HTMLInputElement.webkitdirectory", "webkitdirectory")}}
  - : A boolean that represents the [`webkitdirectory`](/en-US/docs/Web/HTML/Reference/Elements/input#webkitdirectory) attribute. If `true`, the file-system-picker interface only accepts directories instead of files.

- {{domxref("HTMLInputElement.webkitEntries", "webkitEntries")}} {{ReadOnlyInline}}
  - : Describes the currently selected files or directories.

### Instance properties that apply only to visible elements containing text or numbers

- {{domxref("HTMLInputElement.autocomplete", "autocomplete")}}
  - : A string that represents the element's [`autocomplete`](/en-US/docs/Web/HTML/Reference/Elements/input#autocomplete) attribute, indicating whether the value of the control can be automatically completed by the browser.

- {{domxref("HTMLInputElement.max", "max")}}
  - : A string that represents the element's [`max`](/en-US/docs/Web/HTML/Reference/Elements/input#max) attribute, containing the maximum (numeric or date-time) value for this item, which must not be less than its minimum ([`min`](/en-US/docs/Web/HTML/Reference/Elements/input#min) attribute) value.

- {{domxref("HTMLInputElement.maxLength", "maxLength")}}
  - : A number that represents the element's [`maxlength`](/en-US/docs/Web/HTML/Reference/Elements/input#maxlength) attribute, containing the maximum number of characters (in Unicode code points) that the value can have.

- {{domxref("HTMLInputElement.min", "min")}}
  - : A string that represents the element's [`min`](/en-US/docs/Web/HTML/Reference/Elements/input#min) attribute, containing the minimum (numeric or date-time) value for this item, which must not be greater than its maximum ([`max`](/en-US/docs/Web/HTML/Reference/Elements/input#max) attribute) value.

- {{domxref("HTMLInputElement.minLength", "minLength")}}
  - : A number that represents the element's [`minlength`](/en-US/docs/Web/HTML/Reference/Elements/input#minlength) attribute, containing the minimum number of characters (in Unicode code points) that the value can have.

- {{domxref("HTMLInputElement.pattern", "pattern")}}
  - : A string that represents the element's [`pattern`](/en-US/docs/Web/HTML/Reference/Elements/input#pattern) attribute, containing a regular expression that the control's value is checked against. Use the [`title`](/en-US/docs/Web/HTML/Reference/Elements/input#title) attribute to describe the pattern to help the user. This attribute only applies when the value of the [`type`](/en-US/docs/Web/HTML/Reference/Elements/input#type) attribute is `text`, `search`, `tel`, `url` or `email`.

- {{domxref("HTMLInputElement.placeholder", "placeholder")}}
  - : A string that represents the element's [`placeholder`](/en-US/docs/Web/HTML/Reference/Elements/input#placeholder) attribute, containing a hint to the user of what can be entered in the control. The placeholder text must not contain carriage returns or line-feeds. This attribute only applies when the value of the [`type`](/en-US/docs/Web/HTML/Reference/Elements/input#type) attribute is `text`, `search`, `tel`, `url` or `email`.

- {{domxref("HTMLInputElement.readOnly", "readOnly")}}
  - : A boolean that represents the element's [`readonly`](/en-US/docs/Web/HTML/Reference/Elements/input#readonly) attribute, indicating that the user cannot modify the value of the control. This is ignored if the [`type`](/en-US/docs/Web/HTML/Reference/Elements/input#type) is `hidden`, `range`, `color`, `checkbox`, `radio`, `file`, or a button type.

- {{domxref("HTMLInputElement.selectionDirection", "selectionDirection")}}
  - : A string that represents the direction in which selection occurred. Possible values are: `forward` (the selection was performed in the start-to-end direction of the current locale), `backward` (the opposite direction) or `none` (the direction is unknown).

- {{domxref("HTMLInputElement.selectionEnd", "selectionEnd")}}
  - : A number that represents the end index of the selected text. When there's no selection, this returns the offset of the character immediately following the current text input cursor position.

- {{domxref("HTMLInputElement.selectionStart", "selectionStart")}}
  - : A number that represents the beginning index of the selected text. When nothing is selected, this returns the position of the text input cursor (caret) inside of the {{HTMLElement("input")}} element.

- {{domxref("HTMLInputElement.size", "size")}}
  - : A number that represents the element's [`size`](/en-US/docs/Web/HTML/Reference/Elements/input#size) attribute, containing visual size of the control. This value is in pixels unless the value of [`type`](/en-US/docs/Web/HTML/Reference/Elements/input#type) is `text` or `password`, in which case, it is an integer number of characters. Applies only when [`type`](/en-US/docs/Web/HTML/Reference/Elements/input#type) is set to `text`, `search`, `tel`, `url`, `email`, or `password`.

## Instance methods

_Also inherits methods from its parent interface, {{domxref("HTMLElement")}}._

- {{domxref("HTMLInputElement.checkValidity()", "checkValidity()")}}
  - : Returns a boolean value that is `false` if the element is a candidate for constraint validation, and it does not satisfy its constraints. In this case, it also fires an {{domxref("HTMLInputElement/invalid_event", "invalid")}} event at the element. It returns `true` if the element is not a candidate for constraint validation, or if it satisfies its constraints.

- {{domxref("HTMLInputElement.reportValidity()", "reportValidity()")}}
  - : Runs the `checkValidity()` method, and if it returns false (for an invalid input or no pattern attribute provided), then it reports to the user that the input is invalid in the same manner as if you submitted a form.

- {{domxref("HTMLInputElement.select()", "select()")}}
  - : Selects all the text in the input element, and focuses it so the user can subsequently replace all of its content.

- {{domxref("HTMLInputElement.setCustomValidity()", "setCustomValidity()")}}
  - : Sets a custom validity message for the element. If this message is not the empty string, then the element is suffering from a custom validity error, and does not validate.

- {{domxref("HTMLInputElement.setRangeText()", "setRangeText()")}}
  - : Replaces a range of text in the input element with new text.

- {{domxref("HTMLInputElement.setSelectionRange()", "setSelectionRange()")}}
  - : Selects a range of text in the input element (but does not focus it).

- {{domxref("HTMLInputElement.showPicker()", "showPicker()")}}
  - : Shows a browser picker for date, time, color, and files.

- {{domxref("HTMLInputElement.stepDown()", "stepDown()")}}
  - : Decrements the [`value`](/en-US/docs/Web/HTML/Reference/Elements/input#value) by ([`step`](/en-US/docs/Web/HTML/Reference/Elements/input#step) \* n), where n defaults to 1 if not specified.

- {{domxref("HTMLInputElement.stepUp()", "stepUp()")}}
  - : Increments the [`value`](/en-US/docs/Web/HTML/Reference/Elements/input#value) by ([`step`](/en-US/docs/Web/HTML/Reference/Elements/input#step) \* n), where n defaults to 1 if not specified.

## Events

_Also inherits events from its parent interface, {{domxref("HTMLElement")}}._

Listen to these events using {{domxref("EventTarget.addEventListener", "addEventListener()")}} or by assigning an event listener to the `oneventname` property of this interface:

- {{domxref("HTMLInputElement/cancel_event", "cancel")}} event
  - : Fired when the user cancels the file picker dialog via the <kbd>Esc</kbd> key or the cancel button and when the user re-selects the same files that were previously selected.
- {{domxref("HTMLInputElement/invalid_event", "invalid")}} event
  - : Fired when an element does not satisfy its constraints during constraint validation.
- {{domxref("HTMLInputElement/search_event", "search")}} event {{Non-standard_Inline}}
  - : Fired when a search is initiated on an {{HTMLElement("input")}} of `type="search"`.
- {{domxref("HTMLInputElement/select_event", "select")}} event
  - : Fired when some text has been selected.
- {{domxref("HTMLInputElement/selectionchange_event", "selectionchange")}} event
  - : Fires when the text selection in an {{HTMLElement("input")}} element has been changed.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- HTML element implementing this interface: {{HTMLElement("input")}}
