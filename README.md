# modern c++ micro benchmark header

![Demo](https://raw.githubusercontent.com/amosbird/abmb/master/assets/demo.gif)

based on https://github.com/cameron314/microbench

and

powered by https://github.com/joaotavora/yasnippet

```
# -*- mode: snippet -*-
# name: microbench
# key: mb
# --
`(+amos/add-include "abmb.h")`ab::mb<${1:$$(yas/choose-value '("std::chrono::seconds" "std::chrono::milliseconds" "std::chrono::microseconds" "std::chrono::nanoseconds"))}, ${2:1}, ${3:100}>(
    $0
);
```

```
# -*- mode: snippet -*-
# name: microbenchstats
# key: mbs
# --
`(+amos/add-include "abmb.h")`ab::mbs<${1:$$(yas/choose-value '("std::chrono::seconds" "std::chrono::milliseconds" "std::chrono::microseconds" "std::chrono::nanoseconds"))}, ${2:1}, ${3:100}>(
    $0
).${4:$$(yas/choose-value '("min()" "max()" "range()" "avg()" "variance()" "stddev()" "median()" "q1()" "q2()" "q3()"))};
```
