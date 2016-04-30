# ttlcounters
A library to hold monotonic counters concurrently, with a per-counter TTL


``` go
counters := ttlcounters.New(time.Hour)

n, _ := counters.Incr("errors")
if n > 100 {
    fmt.Println("Too many errors")
}
```
