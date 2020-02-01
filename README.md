# Setup

1. `go mod init github.com/parthpatel1001/bazel_go_skaffold`
2. Update root/`BUILD` prefix
3. `go mod vendor`
4. `go mod tidy`
5. `bazelisk run //:gazelle -- update-repos -from_file=go.mod`
6. `bazelisk run //:gazelle`

```
$ bazelisk run //cmd/hello:hello
INFO: Analyzed target //cmd/hello:hello (1 packages loaded, 3 targets configured).
INFO: Found 1 target...
Target //cmd/hello:hello up-to-date:
  bazel-bin/cmd/hello/darwin_amd64_stripped/hello
INFO: Elapsed time: 0.595s, Critical Path: 0.33s
INFO: 2 processes: 2 darwin-sandbox.
INFO: Build completed successfully, 5 total actions
INFO: Build completed successfully, 5 total actions
hello world
```