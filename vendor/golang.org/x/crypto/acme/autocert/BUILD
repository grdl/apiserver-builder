load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "autocert.go",
        "cache.go",
        "listener.go",
        "renewal.go",
    ],
    importpath = "golang.org/x/crypto/acme/autocert",
    visibility = ["//visibility:public"],
    deps = ["//vendor/golang.org/x/crypto/acme:go_default_library"],
)

go_test(
    name = "go_default_test",
    srcs = [
        "autocert_test.go",
        "cache_test.go",
        "renewal_test.go",
    ],
    importpath = "golang.org/x/crypto/acme/autocert",
    library = ":go_default_library",
    deps = ["//vendor/golang.org/x/crypto/acme:go_default_library"],
)

go_test(
    name = "go_default_xtest",
    srcs = ["example_test.go"],
    importpath = "golang.org/x/crypto/acme/autocert_test",
    deps = [":go_default_library"],
)
