+++
date = "2016-12-20T14:06:16+07:00"
description = ""
title = "Go Programming Language"
thumbnail = ""
tags = []
categories = []

+++
# [Golang](golang.org)

## Tools
* [godep](https://github.com/tools/godep) for dependency management. `godep save` and `godep go test`. Alternative is glide, govendor, gvt and gb

## Sample Projects to explore
* [honeypot](github.com/carlmjohnson/heffalump) look at random message generator

## Youtube Video
### Using Go Channels - Natik Shah - Gopherfest
* php/node/etc do concurency with callback on single thread
* in go = sync.Mutex .Waitgroup .Once .Cond, atomic.AddInt64 .Value, chan
* background manager goroutine -> talk to them to access shared resource

### Testing Techniques-Andrew 2014
* `go test -v ./...` and `func TestName(t *testing.t)`
* `var tests = []struct{}` and `for _, test := range tests{}` for table test
* t.Errorf .Fatalf .Logf .Parallel .Skip
* `go test -cover` or `go test -cover=c.out` then `go tool cover -html=c.out`
* this is summary for all test basic in 6 minutes

### Gopher Tricks in Production by Audrey Lim 2016
* hide sensitive data (redact) -> implement func String() String
* env var -> package envvars func CheckSecretToken. func init(). can change it on test
* tests -> var mockUserName = func() string{}. Or use interface in function parameter
* Error handling -> ??? and use error hash

### [Twelve Go Best Practices - Francesc Campoy](https://talks.golang.org/2013/bestpractices.slide)
* simple, readable, maintainable
* happy path on the left
* use interface to avoid dependency
* avoid concurrency in API
* [summary](https://talks.golang.org/2013/bestpractices.slide#34)
