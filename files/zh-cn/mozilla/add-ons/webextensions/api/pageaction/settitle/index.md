---
title: pageAction.setTitle()
slug: Mozilla/Add-ons/WebExtensions/API/pageAction/setTitle
l10n:
  sourceCommit: b8a0743ca8b1e1b1b1a95cc93a4413c020f11262
---

{{AddonSidebar}}

设置页面操作的标题。当用户悬停在页面操作上时，标题会显示在工具提示中。

## 语法

```js-nolint
browser.pageAction.setTitle(
  details // 对象
)
```

### 参数

- `details`
  - : `object`。
    - `tabId`
      - : `integer`。要设置标题的标签页 ID。
    - `title`
      - : `string` 或 `null`。工具提示文本。

        如果传入了 `null`，则标题将重置为在 [`page_action`](/zh-CN/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action) 清单键中指定的标题。

## 浏览器兼容性

{{Compat}}

## 示例

当一个标签页被更新时，在该标签页内显示页面操作，并将页面操作的标题设置为标签页的 ID：

```js
browser.tabs.onUpdated.addListener((tabId, changeInfo, tabInfo) => {
  browser.pageAction.show(tabId);
  browser.pageAction.setTitle({
    tabId,
    title: `标签页 ID：${tabId}`,
  });
});
```

{{WebExtExamples}}

> [!NOTE]
> 此 API 基于 Chromium 的 [`chrome.pageAction`](https://developer.chrome.google.cn/docs/extensions/mv2/reference/pageAction#method-setTitle) API。该文档衍生自 Chromium 代码中的 [`page_action.json`](https://chromium.googlesource.com/chromium/src/+/master/chrome/common/extensions/api/page_action.json)。

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
