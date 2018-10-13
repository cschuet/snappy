# Bazel Build for [google/snappy](https://github.com/google/snappy)

[![Build Status](https://travis-ci.org/cschuet/snappy.svg?branch=master)](https://travis-ci.org/cschuet/snappy)

Add to your WORKSPACE

```
http_archive(
    name = "com_github_cschuet_snappy",
    strip_prefix = "snappy-5f2dda2e502d904120eb3715f47ee8c8338efc90",
    urls = [
        "https://github.com/cschuet/snappy/archive/5f2dda2e502d904120eb3715f47ee8c8338efc90.tar.gz",
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
