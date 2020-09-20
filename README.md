# PathRedux
Better path handling for deno. This lib handles paths in a more dynamic and practical fashion

examples:
```ts
import {Path, WINDOWS_SEPS} from "https://deno.land/x/path/mod.ts";

// Can handle mixed separators on windows
const winPath = new Path("C:\\Users\\Test\\Documents/myFile.v1.txt", WINDOWS_SEPS);
console.log(winPath.elements);
console.log(winPath.toString());
console.log(winPath.ext);
console.log(winPath.exists);

const nixPath = new Path("/etc/passwd");
console.log(nixPath.elements);
console.log(nixPath.toString());
console.log(nixPath.ext);
console.log(nixPath.exists);
```

# Features
* Handles windows acceptance of `\` or `/` as separators
* On linux `\` is treated as escaped characters correctly
* Easily manipulate paths by pushing/poping like an array
* Get file extensions with ease and correctly
* Make assertions about a path

# Thanks
this lib incorporates work from the hashids lib found on src/_hashids.ts
Copyright (c) 2012-2020 Bazyli Brzóska & Ivan Akimov
