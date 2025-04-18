---
title: RTCPeerConnection
slug: Web/API/RTCPeerConnection
page-type: web-api-interface
browser-compat: api.RTCPeerConnection
---

{{APIRef('WebRTC')}}

The **`RTCPeerConnection`** interface represents a WebRTC connection between the local computer and a remote peer.
It provides methods to connect to a remote peer, maintain and monitor the connection, and close the connection once it's no longer needed.

{{InheritanceDiagram}}

## Constructor

- {{DOMxRef("RTCPeerConnection.RTCPeerConnection", "RTCPeerConnection()")}}
  - : Returns a new `RTCPeerConnection`, representing a connection between the local device and a remote peer.

## Instance properties

_Also inherits properties from {{DOMxRef("EventTarget")}}._

- {{DOMxRef("RTCPeerConnection.canTrickleIceCandidates", "canTrickleIceCandidates")}} {{ReadOnlyInline}}
  - : Returns a boolean value which indicates whether or not the remote peer can accept [trickled ICE candidates](https://datatracker.ietf.org/doc/html/draft-ietf-mmusic-trickle-ice).
- {{DOMxRef("RTCPeerConnection.connectionState", "connectionState")}} {{ReadOnlyInline}}
  - : Indicates the current state of the peer connection by returning one of the strings: `new`, `connecting`, `connected`, `disconnected`, `failed`, or `closed`.
- {{DOMxRef("RTCPeerConnection.currentLocalDescription", "currentLocalDescription")}} {{ReadOnlyInline}}
  - : Returns an {{DOMxRef("RTCSessionDescription")}} object describing the local end of the connection as it was most recently successfully negotiated since the last time this `RTCPeerConnection` finished negotiating and connecting to a remote peer.
    Also included is a list of any ICE candidates that may already have been generated by the ICE agent since the offer or answer represented by the description was first instantiated.
- {{DOMxRef("RTCPeerConnection.currentRemoteDescription", "currentRemoteDescription")}} {{ReadOnlyInline}}
  - : Returns an {{DOMxRef("RTCSessionDescription")}} object describing the remote end of the connection as it was most recently successfully negotiated since the last time this `RTCPeerConnection` finished negotiating and connecting to a remote peer.
    Also included is a list of any ICE candidates that may already have been generated by the ICE agent since the offer or answer represented by the description was first instantiated.
- {{DOMxRef("RTCPeerConnection.iceConnectionState", "iceConnectionState")}} {{ReadOnlyInline}}
  - : Returns a string which state of the ICE agent associated with this RTCPeerConnection.
    It can be one of the following values: `new`, `checking`, `connected`, `completed`, `failed`, `disconnected`, or `closed`.
- {{DOMxRef("RTCPeerConnection.iceGatheringState", "iceGatheringState")}} {{ReadOnlyInline}}
  - : Returns a string that describes connection's ICE gathering state.
    This lets you detect, for example, when collection of ICE candidates has finished.
    Possible values are: `new`, `gathering`, or `complete`.
- {{DOMxRef("RTCPeerConnection.localDescription", "localDescription")}} {{ReadOnlyInline}}
  - : Returns an {{DOMxRef("RTCSessionDescription")}}
    describing the session for the local end of the connection.
    If it has not yet been set, returns `null`.
- {{DOMxRef("RTCPeerConnection.peerIdentity", "peerIdentity")}} {{ReadOnlyInline}}
  - : Returns a {{jsxref("Promise")}} that resolves to an {{DOMxRef("RTCIdentityAssertion")}} which contains a string identifying the remote peer.
    Once this promise resolves successfully, the resulting identity is the target peer identity and will not change for the duration of the connection.
- {{DOMxRef("RTCPeerConnection.pendingLocalDescription", "pendingLocalDescription")}} {{ReadOnlyInline}}
  - : Returns an {{DOMxRef("RTCSessionDescription")}} object describing a pending configuration change for the local end of the connection.
    This does not describe the connection as it currently stands, but as it may exist in the near future.
- {{DOMxRef("RTCPeerConnection.pendingRemoteDescription", "pendingRemoteDescription")}} {{ReadOnlyInline}}
  - : Returns an {{DOMxRef("RTCSessionDescription")}} object
    describing a pending configuration change for the remote end of the connection.
    This does not describe the connection as it currently stands, but as it may exist in the near future.
- {{DOMxRef("RTCPeerConnection.remoteDescription", "remoteDescription")}} {{ReadOnlyInline}}
  - : Returns an {{DOMxRef("RTCSessionDescription")}} object describing the session, including configuration and media information, for the remote end of the connection.
    If this hasn't been set yet, this returns `null`.
- {{DOMxRef("RTCPeerConnection.sctp", "sctp")}} {{ReadOnlyInline}}
  - : Returns an {{DOMxRef("RTCSctpTransport")}} object describing the {{Glossary("SCTP")}} transport layer over which SCTP data is being sent and received.
    If SCTP hasn't been negotiated, this value is `null`.
- {{DOMxRef("RTCPeerConnection.signalingState", "signalingState")}} {{ReadOnlyInline}}
  - : Returns a string describing the state of the signaling process on the local end of the connection while connecting or reconnecting to another peer.
    It is one of the following values: `stable`, `have-local-offer`, `have-remote-offer`, `have-local-pranswer`, `have-remote-pranswer`, or `closed`.

## Static methods

- {{DOMxRef("RTCPeerConnection.generateCertificate_static", "RTCPeerConnection.generateCertificate()")}}
  - : Creates an X.509 certificate and its corresponding private key, returning a {{jsxref("Promise")}} that resolves with the new {{DOMxRef("RTCCertificate")}} once it is generated.

## Instance methods

_Also inherits methods from {{DOMxRef("EventTarget")}}._

- {{DOMxRef("RTCPeerConnection.addIceCandidate", "addIceCandidate()")}}
  - : Adds a new remote candidate to the `RTCPeerConnection`'s remote description, which describes the state of the remote end of the connection.
- {{DOMxRef("RTCPeerConnection.addTrack", "addTrack()")}}
  - : Adds a new {{DOMxRef("MediaStreamTrack")}} to the set of tracks which will be transmitted to the other peer.
- {{DOMxRef("RTCPeerConnection.addTransceiver", "addTransceiver()")}}
  - : Creates a new {{DOMxRef("RTCRtpTransceiver")}} and adds it to the set of transceivers associated with the connection.
    Each transceiver represents a bidirectional stream, with both an {{DOMxRef("RTCRtpSender")}} and an {{DOMxRef("RTCRtpReceiver")}} associated with it.
- {{DOMxRef("RTCPeerConnection.close", "close()")}}
  - : Closes the current peer connection.
- {{DOMxRef("RTCPeerConnection.createAnswer", "createAnswer()")}}
  - : Initiates the creation of an {{Glossary("SDP")}} answer to an offer received from a remote peer during the offer/answer negotiation of a WebRTC connection.
    The answer contains information about any media already attached to the session, codecs and options supported by the browser, and any {{Glossary("ICE")}} candidates already gathered.
- {{DOMxRef("RTCPeerConnection.createDataChannel", "createDataChannel()")}}
  - : Initiates the creation a new channel linked with the remote peer, over which any kind of data may be transmitted.
    This can be useful for back-channel content, such as images, file transfer, text chat, game update packets, and so forth.
- {{DOMxRef("RTCPeerConnection.createOffer", "createOffer()")}}
  - : Initiates the creation of an {{Glossary("SDP")}} offer for the purpose of starting a new WebRTC connection to a remote peer.
    The SDP offer includes information about any {{DOMxRef("MediaStreamTrack")}} objects already attached to the WebRTC session, codec, and options supported by the browser, as well as any candidates already gathered by the {{Glossary("ICE")}} agent, for the purpose of being sent over the signaling channel to a potential peer to request a connection or to update the configuration of an existing connection.
- {{DOMxRef("RTCPeerConnection.getConfiguration", "getConfiguration()")}}
  - : Returns an object which indicates the current configuration of the connection.
- {{DOMxRef("RTCPeerConnection.getIdentityAssertion", "getIdentityAssertion()")}}
  - : Initiates the gathering of an identity assertion and returns a {{jsxref("Promise")}} which resolves to an identity assertion encoded as a string.
    This has an effect only if {{DOMxRef("RTCPeerConnection.signalingState", "signalingState")}} is not `closed`.
- {{DOMxRef("RTCPeerConnection.getReceivers", "getReceivers()")}}
  - : Returns an array of {{DOMxRef("RTCRtpReceiver")}} objects, each of which represents one {{Glossary("RTP")}} receiver.
- {{DOMxRef("RTCPeerConnection.getSenders", "getSenders()")}}
  - : Returns an array of {{DOMxRef("RTCRtpSender")}} objects, each of which represents the {{Glossary("RTP")}} sender responsible for transmitting one track's data.
- {{DOMxRef("RTCPeerConnection.getStats", "getStats()")}}
  - : Returns a {{jsxref("Promise")}} which resolves with data providing statistics about either the overall connection or about the specified {{DOMxRef("MediaStreamTrack")}}.
- {{DOMxRef("RTCPeerConnection.getTransceivers", "getTransceivers()")}}
  - : Returns a list of all the {{DOMxRef("RTCRtpTransceiver")}} objects being used to send and receive data on the connection.
- {{DOMxRef("RTCPeerConnection.removeTrack", "removeTrack()")}}
  - : Tells the local end of the connection to stop sending media from the specified track, without actually removing the corresponding {{DOMxRef("RTCRtpSender")}} from the list of senders
    as reported by {{DOMxRef("RTCPeerConnection.getSenders", "getSenders()")}}.
    If the track is already stopped, or is not in the connection's senders list, this method has no effect.
- {{DOMxRef("RTCPeerConnection.restartIce", "restartIce()")}}
  - : Allows to easily request that ICE candidate gathering be redone on both ends of the connection.
    This simplifies the process by allowing the same method to be used by either the caller or the receiver to trigger an {{Glossary("ICE")}} restart.
- {{DOMxRef("RTCPeerConnection.setConfiguration", "setConfiguration()")}}
  - : Sets the current configuration of the connection based on the values included in the specified object.
    This lets you change the {{Glossary("ICE")}} servers used by the connection and which transport policies to use.
- {{DOMxRef("RTCPeerConnection.setIdentityProvider", "setIdentityProvider()")}}
  - : Sets the Identity Provider (IdP) to the triplet given in parameter: its name, the protocol used to communicate with it and an username.
    The protocol and the username are optional.
- {{DOMxRef("RTCPeerConnection.setLocalDescription", "setLocalDescription()")}}
  - : Changes the local description associated with the connection.
    This description specifies the properties of the local end of the connection, including the media format.
    It returns a {{jsxref("Promise")}} which is fulfilled once the description has been changed, asynchronously.
- {{DOMxRef("RTCPeerConnection.setRemoteDescription", "setRemoteDescription()")}}
  - : Sets the specified session description as the remote peer's current offer or answer.
    The description specifies the properties of the remote end of the connection, including the media format.
    It returns a {{jsxref("Promise")}} which is fulfilled once the description has been changed, asynchronously.

### Obsolete methods

- {{DOMxRef("RTCPeerConnection.addStream", "addStream()")}} {{Deprecated_Inline}} {{Non-standard_Inline}}
  - : Adds a {{DOMxRef("MediaStream")}} as a local source of audio or video.
    Instead of using this obsolete method, you should instead use {{DOMxRef("RTCPeerConnection.addTrack", "addTrack()")}} once for each track you wish to send to the remote peer.
- {{DOMxRef("RTCPeerConnection.createDTMFSender", "createDTMFSender()")}} {{Deprecated_Inline}} {{non-standard_inline}}
  - : Creates a new {{DOMxRef("RTCDTMFSender")}}, associated to a specific {{DOMxRef("MediaStreamTrack")}}, that will be able to send {{Glossary("DTMF")}} phone signaling over the connection.
- {{DOMxRef("RTCPeerConnection.removeStream", "removeStream()")}} {{Deprecated_Inline}} {{Non-standard_Inline}}
  - : Removes a {{DOMxRef("MediaStream")}} as a local source of audio or video.
    Because this method is obsolete, you should instead use {{DOMxRef("RTCPeerConnection.removeTrack", "removeTrack()")}}.

## Events

Listen to these events using {{domxref("EventTarget.addEventListener", "addEventListener()")}} or by assigning an event listener to the `oneventname` property of this interface.

- {{domxref("RTCPeerConnection.connectionstatechange_event", "connectionstatechange")}}
  - : Sent when the overall connectivity status of the `RTCPeerConnection` changes.
- {{domxref("RTCPeerConnection.datachannel_event", "datachannel")}}
  - : Sent when the remote peer adds an {{domxref("RTCDataChannel")}} to the connection.
- {{domxref("RTCPeerConnection.icecandidate_event", "icecandidate")}}
  - : Sent to request that the specified candidate be transmitted to the remote peer.
- {{domxref("RTCPeerConnection.icecandidateerror_event", "icecandidateerror")}}
  - : Sent to the connection if an error occurred during {{Glossary("ICE")}} candidate gathering. The event describes the error.
- {{domxref("RTCPeerConnection.iceconnectionstatechange_event", "iceconnectionstatechange")}}
  - : Sent when the state of the {{Glossary("ICE")}} connection changes, such as when it disconnects.
- {{domxref("RTCPeerConnection.icegatheringstatechange_event", "icegatheringstatechange")}}
  - : Sent when the {{Glossary("ICE")}} layer's gathering state, reflected by {{domxref("RTCPeerConnection.iceGatheringState", "iceGatheringState")}}, changes.
    This indicates whether ICE negotiation has not yet begun (`new`), has begun gathering candidates (`gathering`), or has completed (`complete`).
- {{domxref("RTCPeerConnection.negotiationneeded_event", "negotiationneeded")}}
  - : Sent when negotiation or renegotiation of the {{Glossary("ICE")}} connection needs to be performed;
    this can happen both when first opening a connection as well as when it is necessary to adapt to changing network conditions.
    The receiver should respond by creating an offer and sending it to the other peer.
- {{domxref("RTCPeerConnection.signalingstatechange_event", "signalingstatechange")}}
  - : Sent when the connection's {{Glossary("ICE")}} signaling state changes.
- {{domxref("RTCPeerConnection.track_event", "track")}}
  - : Sent after a new track has been added to one of the {{domxref("RTCRtpReceiver")}} instances which comprise the connection.

### Obsolete events

- {{domxref("RTCPeerConnection.addstream_event", "addstream")}} {{Deprecated_Inline}} {{Non-standard_Inline}}
  - : Sent when a new {{domxref("MediaStream")}} has been added to the connection.
    Instead of listening for this obsolete event, you should listen for {{domxref("RTCPeerConnection.track_event", "track")}} events;
    one is sent for each {{domxref("MediaStreamTrack")}} added to the connection.
- {{domxref("RTCPeerConnection.removestream_event", "removestream")}} {{Deprecated_Inline}} {{Non-standard_Inline}}
  - : Sent when a {{domxref("MediaStream")}} is removed from the connection.
    Instead of listening for this obsolete event, you should listen for {{domxref("MediaStream.removetrack_event", "removetrack")}} events on each stream.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- <https://github.com/jesup/nightly-gupshup/blob/master/static/js/chat.js>
- [Get started with WebRTC](https://web.dev/articles/webrtc-basics)
- [TutorRoom](https://github.com/chrisjohndigital/TutorRoom): Node.js HTML video capture, peer-to-peer video and file sharing application ([source on GitHub](https://github.com/chrisjohndigital/TutorRoom))
