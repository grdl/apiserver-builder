load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")
load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["index.pb.go"],
    importpath = "github.com/gogo/protobuf/test/indeximport-issue72/index",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/gogo/protobuf/gogoproto:go_default_library",
        "//vendor/github.com/gogo/protobuf/proto:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["indexpb_test.go"],
    importpath = "github.com/gogo/protobuf/test/indeximport-issue72/index",
    library = ":go_default_library",
    deps = [
        "//vendor/github.com/gogo/protobuf/gogoproto:go_default_library",
        "//vendor/github.com/gogo/protobuf/jsonpb:go_default_library",
        "//vendor/github.com/gogo/protobuf/proto:go_default_library",
    ],
)

proto_library(
    name = "index_proto",
    srcs = ["index.proto"],
    visibility = ["//visibility:public"],
    deps = ["//github.com/gogo/protobuf/gogoproto:gogoproto_proto"],
)

go_proto_library(
    name = "index_go_proto",
    importpath = "github.com/gogo/protobuf/test/indeximport-issue72/index",
    proto = ":index_proto",
    visibility = ["//visibility:public"],
    deps = ["//github.com/gogo/protobuf/gogoproto:go_default_library"],
)
