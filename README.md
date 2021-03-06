# hivecmp
diff and patch for folder hives.
This is a fork of filecmp python standard library.

Functions added: report_patch, report_full_closure_patch, dump_hive_diff and demolocal

## Features
* Compare two folder hives (hive1, hive2)
* Create a config file (hivepatch.ini) showing the changes in old and new
* Dump a diff of hives to a different folder (hive2-hive1).

## Todo
* Track file differences
* Patch hive1 with the hive diff.
* hivecmp as a subclass of filecmp
* and more

### hivepatch.ini

* This file has 3 sections Root, New, Old
* Root: shows old (hive1) and new (hive2) folder names
* New: shows files and folders ONLY IN new folder (hive2)
* Old: shows files and folders ONLY IN old folder (hive1)


```
[Root]
old = hive1
new = hive2

[New]
hive2 = ['f3']
hive2/f1/f1a = ['fladoc.txt']
hive2/f2 = ['d1', 'file5.py']

[Old]
hive1/f1 = ['file2.txt']
```

## How to use
```
clone repo
open python interpreter.
cd to hivecmp
import hivecmp
hivecmp.demolocal()
```