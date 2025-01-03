---
title: "RTCTrackEvent: receiver property"
short-title: receiver
slug: Web/API/RTCTrackEvent/receiver
page-type: web-api-instance-property
browser-compat: api.RTCTrackEvent.receiver
---

{{APIRef("WebRTC")}}

The read-only **`receiver`** property
of the {{domxref("RTCTrackEvent")}} interface indicates the
{{domxref("RTCRtpReceiver")}} which is used to receive data containing media for the
{{domxref("RTCTrackEvent.track", "track")}} to which the event refers.

## Value

The {{domxref("RTCRtpReceiver")}} which pairs the `receiver` with a
sender and other properties which establish a single bidirectional {{Glossary("RTP", "SRTP")}}
stream for use by the {{domxref("RTCTrackEvent.track", "track")}} associated with the
`RTCTrackEvent`.

> [!NOTE]
> The {{domxref("RTCTrackEvent.transceiver", "transceiver")}}
> includes its own {{domxref("RTCRtpTransceiver.receiver", "receiver")}} property, which
> will always be the same {{domxref("RTCRtpReceiver")}} as this one.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
