# letsgo
Lets Learn Go ..  So tonight i decided to start learning golang.  
Get started from here https://golang.org/doc/install  

The first crazy thing, i'm using cygwin on holy windows(R) . when you are setting $GOPATH it detects absolute unix paths as relative path and ``` export GOPATH=`pwd` ``` seems not working. so workaround is ``` GOPATH=`cygpath -aw .` ``` (maybe i will make a helper script for thi GOPATH thing)
    
So lets compile and test my hello-go 

```
mkdir -p src/github.com/pi0/letsgo
vi src/github.com/pi0/letsgo/hello.go
```

```go
package main

import "fmt"

func main() {
    fmt.Printf("hello, world\n")
}
```

```
> go install github.com/pi0/letsgo
[Silent!]
> ./bin/letsgo.exe
hello, world
> du -h ./bin/letsgo.exe
2.4M    ./bin/letsgo.exe
```
