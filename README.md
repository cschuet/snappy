# Bazel Build for [google/snappy](https://github.com/google/leveldb)

[![Build Status](https://travis-ci.org/cschuet/snappy.svg?branch=master)](https://travis-ci.org/cschuet/leveldb)

Add to your WORKSPACE

```
http_archive(
    name = "com_github_cschuet_snappy",
    strip_prefix = "snappy-<SHA-1>",
    urls = [
        "https://github.com/cschuet/snappy/archive/<SHA-1>.tar.gz",
    ],
)

load("@com_github_cschuet_snappy//:bazel/repositories.bzl", "repositories")

repositories()

load("@com_github_cschuet_crc32c//:bazel/repositories.bzl", "repositories")

repositories()
```

Compile with
```
bazel build @com_github_google_snappy//:leveldb
```

Test with
```
bazel test @com_github_google_snappy//...
```

## Limitations
* not using FDATASYNC
* not using Google Snappy
* assumes little endian
