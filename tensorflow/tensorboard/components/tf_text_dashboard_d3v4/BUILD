package(default_visibility = ["//tensorflow:internal"])

load("@io_bazel_rules_closure//closure:defs.bzl", "web_library")

licenses(["notice"])  # Apache 2.0

web_library(
    name = "tf_text_dashboard_d3v4",
    srcs = [
        "tf-text-dashboard.html",
        "tf-text-loader.html",
    ],
    path = "/tf-text-dashboard",
    deps = [
        "//tensorflow/tensorboard/components/tf_backend_d3v4",
        "//tensorflow/tensorboard/components/tf_color_scale_d3v4",
        "//tensorflow/tensorboard/components/tf_dashboard_common_d3v4",
        "//tensorflow/tensorboard/components/tf_imports_d3v4:d3",
        "//tensorflow/tensorboard/components/tf_imports_d3v4:lodash",
        "@org_polymer",
        "@org_polymer_paper_dialog",
        "@org_polymer_paper_icon_button",
        "@org_polymer_paper_material",
        "@org_polymer_paper_slider",
        "@org_polymer_paper_spinner",
    ],
)

web_library(
    name = "demo",
    srcs = ["index.html"] + glob(["data/**"]),
    path = "/tf-text-dashboard",
    deps = [
        ":tf_text_dashboard_d3v4",
        "@org_polymer_iron_demo_helpers",
        "@org_polymer_paper_styles",
        "@org_polymer_webcomponentsjs",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(["**"]),
    tags = ["notsan"],
)
