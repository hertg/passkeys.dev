---
title: "Known Issues"
description: "A list of known issues with passkey implementations"
date: 2022-09-03T16:09:38.358Z
draft: false
images: []
menu:
  docs:
    parent: "reference"
weight: 1101
toc: false
layout: matrix
---


## User Verification

The following list of passkey providers have not implemented [User Verification](../terms#user-verification-uv) in a spec-compliant manner.

| **Provider** | **Architecture** | **UV Required Behavior**      | **UV Flag**              |
| ------------ | ---------------- | ----------------------------- | ------------------------ |
| 1Password    | Extension        | ❌ Handles request without UV | ❌ Always replies `True` |
| 1Password    | Native           | ✅ Performs UV                | ✅ UV flag accurate      |
| Bitwarden    | Extension        | ✅ Performs UV                | ✅ UV flag accurate      |
| KeepassXC    | Extension        | ❌ Handles request without UV | ❌ Always replies `True` |
| Proton Pass  | Extension        | ❌ Handles request without UV | ❌ Always replies `True` |
| Proton Pass  | Native           | ❌ Handles request without UV | ❌ Always replies `True` |
| Strongbox    | Native           | ❌ Handles request without UV | ❌ Always replies `True` |

> **Architecture**: `Extension` = web browser extension, `Native` = OS native app using provider APIs
