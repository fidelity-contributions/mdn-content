---
title: "HIDDevice: receiveFeatureReport() method"
short-title: receiveFeatureReport()
slug: Web/API/HIDDevice/receiveFeatureReport
page-type: web-api-instance-method
status:
  - experimental
browser-compat: api.HIDDevice.receiveFeatureReport
---

{{securecontext_header}}{{APIRef("WebHID API")}}{{SeeCompatTable}}{{AvailableInWorkers("window_and_worker_except_shared")}}

The **`receiveFeatureReport()`** method of the {{domxref("HIDDevice")}} interface receives a feature report from the HID device. Feature reports are a way for HID devices and applications to exchange non-standardized HID data.

The `reportId` for each of the report formats that this device supports can be retrieved from {{domxref("HIDDevice.collections")}}.

## Syntax

```js-nolint
receiveFeatureReport(reportId)
```

### Parameters

- `reportId`
  - : An 8-bit report ID. If the HID device does not use report IDs, send `0`.

### Return value

A {{jsxref("Promise")}} which resolves with a {{jsxref("DataView")}} object containing the feature report.

### Exceptions

- `NotAllowedError` {{domxref("DOMException")}}
  - : Thrown if receiving the report fails for any reason.

## Examples

In the following example a report is received from a device using a `reportId` of `1`.

```js
const dataView = await device.receiveFeatureReport(1);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
