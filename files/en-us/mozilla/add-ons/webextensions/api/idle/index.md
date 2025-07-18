---
title: idle
slug: Mozilla/Add-ons/WebExtensions/API/idle
page-type: webextension-api
browser-compat: webextensions.api.idle
sidebar: addonsidebar
---

Find out when the user's system is idle, locked, or active.

To use this API you need to have the "idle" [permission](/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions).

## Types

- {{WebExtAPIRef("idle.IdleState")}}
  - : String describing the device's idle state.

## Functions

- {{WebExtAPIRef("idle.queryState()")}}
  - : Returns `"locked"` if the system is locked, `"idle"` if the user has not generated any input for a specified number of seconds, or `"active"` otherwise.
- {{WebExtAPIRef("idle.setDetectionInterval()")}}
  - : Sets the interval used to determine when the system is in an idle state for {{WebExtAPIRef("idle.onStateChanged")}} events.

## Events

- {{WebExtAPIRef("idle.onStateChanged")}}
  - : Fired when the system changes state.

{{WebExtExamples("h2")}}

## Browser compatibility

{{Compat}}

> [!NOTE]
> This API is based on Chromium's [`chrome.idle`](https://developer.chrome.com/docs/extensions/reference/api/idle) API. This documentation is derived from [`idle.json`](https://chromium.googlesource.com/chromium/src/+/master/extensions/common/api/idle.json) in the Chromium code.

<!--
// Copyright 2015 The Chromium Authors. All rights reserved.
//
// Redistribution and use in source and binary forms, with or without
// modification, are permitted provided that the following conditions are
// met:
//
//    * Redistributions of source code must retain the above copyright
// notice, this list of conditions and the following disclaimer.
//    * Redistributions in binary form must reproduce the above
// copyright notice, this list of conditions and the following disclaimer
// in the documentation and/or other materials provided with the
// distribution.
//    * Neither the name of Google Inc. nor the names of its
// contributors may be used to endorse or promote products derived from
// this software without specific prior written permission.
//
// THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
// "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
// LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
// A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
// OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
// SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
// LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
// DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
// THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
// (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
// OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
-->
