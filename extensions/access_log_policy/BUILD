licenses(["notice"])  # Apache 2

load(
    "@envoy//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_package",
)

envoy_package()

envoy_cc_library(
    name = "access_log_policy_lib",
    srcs = [
        "config.cc",
        "plugin.cc",
    ],
    hdrs = [
        "plugin.h",
    ],
    repository = "@envoy",
    visibility = ["//visibility:public"],
    deps = [
        "//extensions/access_log_policy/config/v1alpha1:access_log_policy_config_cc_proto",
        "//extensions/common:context",
        "//extensions/common:istio_dimensions",
        "@envoy//source/common/common:base64_lib",
        "@envoy//source/extensions/common/wasm/null:null_plugin_lib",
    ],
)
