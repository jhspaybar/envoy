licenses(["notice"])  # Apache 2

load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_package",
)

envoy_package()

envoy_cc_library(
    name = "echo_lib",
    srcs = ["echo.cc"],
    hdrs = ["echo.h"],
    deps = [
        "//include/envoy/buffer:buffer_interface",
        "//include/envoy/network:connection_interface",
        "//include/envoy/network:filter_interface",
        "//source/common/common:assert_lib",
        "//source/common/common:logger_lib",
    ],
)

envoy_cc_library(
    name = "ratelimit_lib",
    srcs = ["ratelimit.cc"],
    hdrs = ["ratelimit.h"],
    deps = [
        "//include/envoy/network:connection_interface",
        "//include/envoy/network:filter_interface",
        "//include/envoy/ratelimit:ratelimit_interface",
        "//include/envoy/runtime:runtime_interface",
        "//include/envoy/stats:stats_macros",
        "//source/common/tracing:http_tracer_lib",
        "@envoy_api//envoy/api/v2/filter/network:rate_limit_cc",
    ],
)

envoy_cc_library(
    name = "tcp_proxy_lib",
    srcs = ["tcp_proxy.cc"],
    hdrs = ["tcp_proxy.h"],
    deps = [
        "//include/envoy/access_log:access_log_interface",
        "//include/envoy/buffer:buffer_interface",
        "//include/envoy/event:dispatcher_interface",
        "//include/envoy/event:timer_interface",
        "//include/envoy/network:connection_interface",
        "//include/envoy/network:filter_interface",
        "//include/envoy/router:router_interface",
        "//include/envoy/server:filter_config_interface",
        "//include/envoy/stats:stats_interface",
        "//include/envoy/stats:stats_macros",
        "//include/envoy/stats:timespan",
        "//include/envoy/upstream:cluster_manager_interface",
        "//include/envoy/upstream:upstream_interface",
        "//source/common/access_log:access_log_lib",
        "//source/common/common:assert_lib",
        "//source/common/common:empty_string",
        "//source/common/common:logger_lib",
        "//source/common/network:cidr_range_lib",
        "//source/common/network:filter_lib",
        "//source/common/network:utility_lib",
        "//source/common/request_info:request_info_lib",
        "@envoy_api//envoy/api/v2/filter/network:tcp_proxy_cc",
    ],
)
