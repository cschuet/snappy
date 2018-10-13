licenses(["notice"])

exports_files(["LICENSE"])

cc_library(
    name = "snappy",
    srcs = glob(
        ["**/*.cc"],
	exclude = ["snappy-test.cc", "snappy_unittest.cc"],
    ),
    hdrs = glob(
        ["**/*.h"],
	exclude = ["snappy-test.h"],
    ),
)

