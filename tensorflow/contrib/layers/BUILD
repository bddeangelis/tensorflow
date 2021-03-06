# Description:
#   contains parts of TensorFlow that are experimental or unstable and which are not supported.

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])

package(default_visibility = ["//tensorflow:__subpackages__"])

py_library(
    name = "layers_py",
    srcs = [
        "__init__.py",
        "python/framework/tensor_util.py",
        "python/layers/__init__.py",
        "python/layers/initializers.py",
        "python/layers/layers.py",
        "python/layers/regularizers.py",
        "python/layers/summaries.py",
        "python/ops/__init__.py",
        "python/ops/loss_ops.py",
    ],
    srcs_version = "PY2AND3",
)

py_test(
    name = "layers_test",
    srcs = glob(["python/layers/layers_test.py"]),
    srcs_version = "PY2AND3",
    deps = [
        ":layers_py",
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

py_test(
    name = "regularizers_test",
    srcs = glob(["python/layers/regularizers_test.py"]),
    srcs_version = "PY2AND3",
    deps = [
        ":layers_py",
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

py_test(
    name = "initializers_test",
    srcs = glob(["python/layers/initializers_test.py"]),
    srcs_version = "PY2AND3",
    deps = [
        ":layers_py",
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

py_test(
    name = "loss_ops_test",
    srcs = glob(["python/ops/loss_ops_test.py"]),
    srcs_version = "PY2AND3",
    deps = [
        ":layers_py",
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

py_test(
    name = "summaries_test",
    srcs = glob(["python/layers/summaries_test.py"]),
    srcs_version = "PY2AND3",
    deps = [
        ":layers_py",
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

py_test(
    name = "tensor_util_test",
    srcs = glob(["python/framework/tensor_util_test.py"]),
    srcs_version = "PY2AND3",
    deps = [
        ":layers_py",
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(
        ["**/*"],
        exclude = [
            "**/METADATA",
            "**/OWNERS",
        ],
    ),
    visibility = ["//tensorflow:__subpackages__"],
)
