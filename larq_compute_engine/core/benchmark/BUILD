licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

cc_binary(
    name = "benchmark_aarch64",
    srcs = [
        "aarch64/packbits_bench.cc",
    ],
    linkopts = ["-lrt -lm"],
    deps = [
        "//larq_compute_engine/core:packbits",
        "//larq_compute_engine/core:packbits_aarch64",
        "@googlebenchmark//:benchmark",
        "@googlebenchmark//:benchmark_main",
    ],
)

cc_binary(
    name = "benchmark",
    srcs = [
        "bconv2d_bench.cc",
        "bgemm_bench.cc",
        "im2col_bench.cc",
        "padding_bench.cc",
    ],
    linkopts = ["-lrt -lm"],
    deps = [
        "//larq_compute_engine/core:bconv2d_functor",
        "//larq_compute_engine/core:bgemm_functor",
        "//larq_compute_engine/core:fused_bgemm_functor",
        "//larq_compute_engine/core:im2col_functor",
        "//larq_compute_engine/core:padding_functor",
        "@googlebenchmark//:benchmark",
        "@googlebenchmark//:benchmark_main",
    ],
)
