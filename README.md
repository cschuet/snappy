# Bazel Build for [google/snappy](https://github.com/google/snappy)

[![Build Status](https://travis-ci.org/cschuet/snappy.svg?branch=master)](https://travis-ci.org/cschuet/snappy)

Add to your WORKSPACE

```
http_archive(
    name = "com_github_cschuet_snappy",
    strip_prefix = "snappy-7b7f8fc8e162bbf24ad31fa046d995703179a3be",
    sha256 = "a62d0fa46f3efb3cec7779d95bbf3320195d2f106d63db5a029eeebf0e7ec67f",
    urls = [
        "https://github.com/cschuet/snappy/archive/7b7f8fc8e162bbf24ad31fa046d995703179a3be.tar.gz",
    ],
)

load("@com_github_cschuet_snappy//:bazel/repositories.bzl", "repositories")

repositories()
```

Compile with
```
bazel build @com_github_google_snappy//:snappy
```

Test with
```
bazel test @com_github_google_snappy//...
```

## Limitations
* not using FDATASYNC
* not using Google Snappy
* assumes little endian
