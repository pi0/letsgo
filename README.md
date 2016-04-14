# Let's Learn Go
**(Note: nothing is right here! that's just some notes while i was learning)**

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
    fmt.Printf("hello, دنیا\n")
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
* Good News For Iranians : Google And OpenSource Community blockd iranian users getting go packages, so turn on you فیلتر شکن * ! 
i prefered getting the offline version :   
```sh
go get golang.org/x/tour/gotour
./bin/gotour.exe
```
Bang! Super nice, browser showed off with a offline version on `http://127.0.0.1:3999/welcome/1`

# Go Projects - Get Pro!

Read this pages for more information about go workspace structure and dependancy managers:   
- (How to Write Go Code)[https://golang.org/doc/code.html]
- (PackageManagementTools)[https://github.com/golang/go/wiki/PackageManagementTools]   

Also found a useful command `go env` which prints current go environment configs.

# (Godep)[https://github.com/tools/godep]
godep helps build packages reproducibly by fixing their dependencies.
```go get github.com/tools/godep```
