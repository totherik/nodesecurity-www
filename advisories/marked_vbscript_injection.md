---
title:  marked VBScript Content Injection
author: Xiao Long
module_name: marked
publish_date: Thur Jan 22 2015 09:33:48 GMT-0800 (PST) 
cves: "[]"
vulnerable_versions: "<=0.3.2"
patched_versions: "<0.0.0"
...

## Overview

Marked 0.3.2 and earlier is vulnerable to content injection even when `sanitize: true` is enabled.

\[xss link](vbscript:alert(1&#41;)

will get a link

&lt;a href="vbscript:alert(1)">xss link</a>

this script does not work in IE 11 edge mode, but works in IE 10 compatibility view.

## Recommendation:

There is a pull request that may address this issue available [here](https://github.com/chjj/marked/pull/537). You may also consider an alternative markdown parser.


## References:
- https://github.com/chjj/marked/issues/492

