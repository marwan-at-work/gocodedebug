Debugging https://github.com/mdempsky/gocode/issues/79

```
2018/10/30 17:11:43 Cursor at: 136
2018/10/30 17:11:43 -------------------------------------------------------
package main

import (
        "fmt"

        "github.com/marwan-at-work/gocodebug/sub"
)

func main() {
        fmt.Println("calling hello")
        sub.Hello()
        s#ub.
}
2018/10/30 17:11:43 -------------------------------------------------------
2018/10/30 17:11:43 Error parsing input file (outer block):
2018/10/30 17:11:43  /Users/me/go/src/github.com/marwan-at-work/gocodebug/main.go:13:1: expected selector or type assertion, found '}'
2018/10/30 17:11:43  /Users/me/go/src/github.com/marwan-at-work/gocodebug/main.go:13:3: expected ';', found 'EOF'
2018/10/30 17:11:43  /Users/me/go/src/github.com/marwan-at-work/gocodebug/main.go:13:3: expected '}', found 'EOF'
2018/10/30 17:11:43 Elapsed duration: 1.96989ms
2018/10/30 17:11:43 Offset: 0
2018/10/30 17:11:43 Number of candidates found: 2
2018/10/30 17:11:43 Candidates are:
2018/10/30 17:11:43   package sub
2018/10/30 17:11:43   type string string
2018/10/30 17:11:43 =======================================================
2018/10/30 17:11:43 Got autocompletion request for '/Users/me/go/src/github.com/marwan-at-work/gocodebug/main.go'
2018/10/30 17:11:43 Cursor at: 139
2018/10/30 17:11:43 -------------------------------------------------------
package main

import (
        "fmt"

        "github.com/marwan-at-work/gocodebug/sub"
)

func main() {
        fmt.Println("calling hello")
        sub.Hello()
        sub.#
}
2018/10/30 17:11:43 -------------------------------------------------------
2018/10/30 17:11:43 Error parsing input file (outer block):
2018/10/30 17:11:43  /Users/me/go/src/github.com/marwan-at-work/gocodebug/main.go:12:6: expected selector or type assertion, found ';'
2018/10/30 17:11:43 Elapsed duration: 617.381µs
2018/10/30 17:11:43 Offset: 0
2018/10/30 17:11:43 Number of candidates found: 0
2018/10/30 17:11:43 Candidates are:
2018/10/30 17:11:43 =======================================================
```