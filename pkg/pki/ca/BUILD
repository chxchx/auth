load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "ca.go",
        "generate_cert.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/pki:go_default_library",
        "@com_github_golang_glog//:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "ca_test.go",
        "generate_cert_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "//pkg/pki:go_default_library",
        "//pkg/pki/testutil:go_default_library",
    ],
)
