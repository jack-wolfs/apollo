load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "net_util",
    srcs = [
        "net_util.cc",
    ],
    hdrs = [
        "net_util.h",
    ],
    deps = [
        "//cyber",
        "//modules/prediction/proto:network_model_proto",
        "@eigen",
    ],
)

cc_library(
    name = "net_layer",
    srcs = [
        "net_layer.cc",
    ],
    hdrs = [
        "net_layer.h",
    ],
    deps = [
        "//cyber",
        "//modules/prediction/network:net_util",
        "//modules/prediction/proto:network_model_proto",
        "@eigen",
    ],
)

cc_library(
    name = "net_model",
    srcs = [
        "net_model.cc",
    ],
    hdrs = [
        "net_model.h",
    ],
    deps = [
        "//cyber",
        "//modules/common/util",
        "//modules/prediction/network:net_layer",
        "//modules/prediction/proto:network_model_proto",
        "@eigen",
    ],
)

cc_test(
    name = "net_util_test",
    size = "small",
    srcs = [
        "net_util_test.cc",
    ],
    deps = [
        "//modules/prediction/network:net_util",
        "//modules/prediction/proto:network_model_proto",
        "@eigen",
        "@gtest//:main",
    ],
)

cc_test(
    name = "net_layer_test",
    size = "small",
    srcs = [
        "net_layer_test.cc",
    ],
    deps = [
        "//modules/prediction/network:net_layer",
        "//modules/prediction/network:net_util",
        "//modules/prediction/proto:network_model_proto",
        "@eigen",
        "@gtest//:main",
    ],
)

cpplint()
