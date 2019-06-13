package(default_visibility = ["//visibility:public"])

load("@protobuf_py_deps//:requirements.bzl", protobuf_requirements = "all_requirements")
load("@grpc_py_deps//:requirements.bzl", grpc_requirements = "all_requirements")
load("@ptf_deps//:requirements.bzl", ptf_requirements = "all_requirements")

py_binary(
    name = "test",
    srcs = ["test.py"],
    deps = ["@com_github_p4lang_p4runtime//:p4runtime_py_grpc"] +
    depset(ptf_requirements + protobuf_requirements + grpc_requirements).to_list(),
)

