---
layout: default
menu_item: api
title: Patch
description: Version 0.4.0
menu_item: api
return_to:
  "API Documentation Index": /api/
sections:
  "fromBlobAndBuffer": "#fromBlobAndBuffer"
  "fromBlobs": "#fromBlobs"
  "fromDiff": "#fromDiff"
  "#getDelta": "#getDelta"
  "#getHunk": "#getHunk"
  "#getLineInHunk": "#getLineInHunk"
  "#numHunks": "#numHunks"
  "#numLinesInHunk": "#numLinesInHunk"
  "#size": "#size"
---

## <a name="fromBlobAndBuffer"></a><span>Patch.</span>fromBlobAndBuffer <span class="tags"><span class="async">Async</span><span class="experimental">Experimental</span></span>

```js
Patch.fromBlobAndBuffer(old_blob, old_as_path, buffer, buffer_len, buffer_as_path, opts).then(function(patch) {
  // Use patch
});
```

| Parameters | Type |   |
| --- | --- | --- |
| old_blob | [Blob](/api/blob/) | Blob for old side of diff, or NULL for empty blob |
| old_as_path | String | Treat old blob as if it had this filename; can be NULL |
| buffer | String | Raw data for new side of diff, or NULL for empty |
| buffer_len | Number | Length of raw data for new side of diff |
| buffer_as_path | String | Treat buffer as if it had this filename; can be NULL |
| opts | [DiffOptions](/api/diff_options/) | Options for diff, or NULL for default options |

| Returns |  |
| --- | --- |
| [Patch](/api/patch/) | The generated patch; NULL on error |

## <a name="fromBlobs"></a><span>Patch.</span>fromBlobs <span class="tags"><span class="async">Async</span><span class="experimental">Experimental</span></span>

```js
Patch.fromBlobs(old_blob, old_as_path, new_blob, new_as_path, opts).then(function(patch) {
  // Use patch
});
```

| Parameters | Type |   |
| --- | --- | --- |
| old_blob | [Blob](/api/blob/) | Blob for old side of diff, or NULL for empty blob |
| old_as_path | String | Treat old blob as if it had this filename; can be NULL |
| new_blob | [Blob](/api/blob/) | Blob for new side of diff, or NULL for empty blob |
| new_as_path | String | Treat new blob as if it had this filename; can be NULL |
| opts | [DiffOptions](/api/diff_options/) | Options for diff, or NULL for default options |

| Returns |  |
| --- | --- |
| [Patch](/api/patch/) | The generated patch; NULL on error |

## <a name="fromDiff"></a><span>Patch.</span>fromDiff <span class="tags"><span class="sync">Sync</span><span class="experimental">Experimental</span></span>

```js
var patch = Patch.fromDiff(diff, idx);
```

| Parameters | Type |   |
| --- | --- | --- |
| diff | [Diff](/api/diff/) | Diff list object |
| idx | Number | Index into diff list |

| Returns |  |
| --- | --- |
| [Patch](/api/patch/) | Output parameter for the delta patch object |

## <a name="getDelta"></a><span>Patch#</span>getDelta <span class="tags"><span class="sync">Sync</span><span class="experimental">Experimental</span></span>

```js
var diffDelta = patch.getDelta();
```

| Returns |  |
| --- | --- |
| [DiffDelta](/api/diff_delta/) |  |

## <a name="getHunk"></a><span>Patch#</span>getHunk <span class="tags"><span class="sync">Sync</span><span class="experimental">Experimental</span></span>

```js
var result = patch.getHunk(hunk_idx);
```

| Parameters | Type |
| --- | --- | --- |
| hunk_idx | Number | Input index of hunk to get information about |

| Returns |  |
| --- | --- |
| Number | Output count of total lines in this hunk |

## <a name="getLineInHunk"></a><span>Patch#</span>getLineInHunk <span class="tags"><span class="sync">Sync</span><span class="experimental">Experimental</span></span>

```js
var diffLine = patch.getLineInHunk(hunk_idx, line_of_hunk);
```

| Parameters | Type |
| --- | --- | --- |
| hunk_idx | Number | The index of the hunk |
| line_of_hunk | Number | The index of the line in the hunk |

| Returns |  |
| --- | --- |
| [DiffLine](/api/diff_line/) | The git_diff_line data for this line |

## <a name="numHunks"></a><span>Patch#</span>numHunks <span class="tags"><span class="sync">Sync</span><span class="experimental">Experimental</span></span>

```js
var result = patch.numHunks();
```

| Returns |  |
| --- | --- |
| Number |  |

## <a name="numLinesInHunk"></a><span>Patch#</span>numLinesInHunk <span class="tags"><span class="sync">Sync</span><span class="experimental">Experimental</span></span>

```js
var result = patch.numLinesInHunk(hunk_idx);
```

| Parameters | Type |
| --- | --- | --- |
| hunk_idx | Number | Index of the hunk |

| Returns |  |
| --- | --- |
| Number |  Number of lines in hunk or -1 if invalid hunk index |

## <a name="size"></a><span>Patch#</span>size <span class="tags"><span class="sync">Sync</span><span class="experimental">Experimental</span></span>

```js
var result = patch.size(include_context, include_hunk_headers, include_file_headers);
```

| Parameters | Type |
| --- | --- | --- |
| include_context | Number | Include context lines in size if non-zero |
| include_hunk_headers | Number | Include hunk header lines if non-zero |
| include_file_headers | Number | Include file header lines if non-zero |

| Returns |  |
| --- | --- |
| Number |  The number of bytes of data |

