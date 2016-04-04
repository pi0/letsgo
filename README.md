# letsgo
Lets Learn Go ..  So tonight i decided to start learning golang.  
Get started from here https://golang.org/doc/install  

The first crazy thing, i'm using cygwin on holy windows(R) . when you are setting **$GOPATH** it detects absolute unix paths as relative path and ``` export GOPATH=`pwd` ``` seems not working. so workaround is ``` GOPATH=`cygpath -aw .` ``` (maybe i will make a helper script for this `GOPATH` thing)
    
So lets compile and test my hello-go 

```sh
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

```sh
> go install github.com/pi0/letsgo
[Silent!]
> ./bin/letsgo.exe
hello, world
> du -h ./bin/letsgo.exe
2.4M    ./bin/letsgo.exe
```

# A Tour of Go
** Good news for iranians Goolgle and Open-Source Community blockd iranian users getting go packages, so turn on you `فیلتر شکن` **  ! 
I prefered getting the offline version :   
```sh
go get golang.org/x/tour/gotour
cd $GOPATH/bin
./gotour
```
