---
layout: default
menu_item: api
title: ConvenientPatch
description: Version 0.4.0
menu_item: api
return_to:
  "API Documentation Index": /api/
sections:
  "#hunks": "#hunks"
  "#isAdded": "#isAdded"
  "#isCopied": "#isCopied"
  "#isDeleted": "#isDeleted"
  "#isIgnored": "#isIgnored"
  "#isModified": "#isModified"
  "#isRenamed": "#isRenamed"
  "#isTypeChange": "#isTypeChange"
  "#isUnmodified": "#isUnmodified"
  "#isUntracked": "#isUntracked"
  "#newFile": "#newFile"
  "#oldFile": "#oldFile"
  "#size": "#size"
  "#status": "#status"
---

## <a name="hunks"></a><span>ConvenientPatch#</span>hunks <span class="tags"><span class="sync">Sync</span></span>

```js
var convenientHunk = convenientPatch.hunks();
```

The hunks in this patch

| Returns |  |
| --- | --- |
| [ConvenientHunk](/api/convenient_hunk/) | an array of ConvenientHunks |

## <a name="isAdded"></a><span>ConvenientPatch#</span>isAdded <span class="tags"><span class="sync">Sync</span></span>

```js
var boolean = convenientPatch.isAdded();
```

Is this an added patch?

| Returns |  |
| --- | --- |
| Boolean |  |

## <a name="isCopied"></a><span>ConvenientPatch#</span>isCopied <span class="tags"><span class="sync">Sync</span></span>

```js
var boolean = convenientPatch.isCopied();
```

Is this a copied patch?

| Returns |  |
| --- | --- |
| Boolean |  |

## <a name="isDeleted"></a><span>ConvenientPatch#</span>isDeleted <span class="tags"><span class="sync">Sync</span></span>

```js
var boolean = convenientPatch.isDeleted();
```

Is this a deleted patch?

| Returns |  |
| --- | --- |
| Boolean |  |

## <a name="isIgnored"></a><span>ConvenientPatch#</span>isIgnored <span class="tags"><span class="sync">Sync</span></span>

```js
var boolean = convenientPatch.isIgnored();
```

Is this an ignored patch?

| Returns |  |
| --- | --- |
| Boolean |  |

## <a name="isModified"></a><span>ConvenientPatch#</span>isModified <span class="tags"><span class="sync">Sync</span></span>

```js
var boolean = convenientPatch.isModified();
```

Is this an modified patch?

| Returns |  |
| --- | --- |
| Boolean |  |

## <a name="isRenamed"></a><span>ConvenientPatch#</span>isRenamed <span class="tags"><span class="sync">Sync</span></span>

```js
var boolean = convenientPatch.isRenamed();
```

Is this a renamed patch?

| Returns |  |
| --- | --- |
| Boolean |  |

## <a name="isTypeChange"></a><span>ConvenientPatch#</span>isTypeChange <span class="tags"><span class="sync">Sync</span></span>

```js
var boolean = convenientPatch.isTypeChange();
```

Is this a type change?

| Returns |  |
| --- | --- |
| Boolean |  |

## <a name="isUnmodified"></a><span>ConvenientPatch#</span>isUnmodified <span class="tags"><span class="sync">Sync</span></span>

```js
var boolean = convenientPatch.isUnmodified();
```

Is this an unmodified patch?

| Returns |  |
| --- | --- |
| Boolean |  |

## <a name="isUntracked"></a><span>ConvenientPatch#</span>isUntracked <span class="tags"><span class="sync">Sync</span></span>

```js
var boolean = convenientPatch.isUntracked();
```

Is this an untracked patch?

| Returns |  |
| --- | --- |
| Boolean |  |

## <a name="newFile"></a><span>ConvenientPatch#</span>newFile <span class="tags"><span class="sync">Sync</span></span>

```js
var string = convenientPatch.newFile();
```

New name of the file

| Returns |  |
| --- | --- |
| String |  |

## <a name="oldFile"></a><span>ConvenientPatch#</span>oldFile <span class="tags"><span class="sync">Sync</span></span>

```js
var string = convenientPatch.oldFile();
```

Old name of the file

| Returns |  |
| --- | --- |
| String |  |

## <a name="size"></a><span>ConvenientPatch#</span>size <span class="tags"><span class="sync">Sync</span></span>

```js
var number = convenientPatch.size();
```

The number of hunks in this patch

| Returns |  |
| --- | --- |
| Number |  |

## <a name="status"></a><span>ConvenientPatch#</span>status <span class="tags"><span class="sync">Sync</span></span>

```js
var number = convenientPatch.status();
```

The status of this patch (unmodified, added, deleted)

| Returns |  |
| --- | --- |
| Number |  |

