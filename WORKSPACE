workspace(name = "proto_converter")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "com_google_protobuf",
    sha256 = "55912546338433f465a552e9ef09930c63b9eb697053937416890cff83a8622d",
    strip_prefix = "protobuf-b407e8416e3893036aee5af9a12bd9b6a0e2b2e6",
    urls = ["https://github.com/protocolbuffers/protobuf/archive/b407e8416e3893036aee5af9a12bd9b6a0e2b2e6.tar.gz"],  # v29.3
)

load("@com_google_protobuf//:protobuf_deps.bzl", "protobuf_deps")

protobuf_deps()

load("@rules_python//python:repositories.bzl", "py_repositories")

py_repositories()

load("@rules_python//python/pip_install:repositories.bzl", "pip_install_dependencies")

pip_install_dependencies()

http_archive(
    name = "com_google_googletest",
    sha256 = "7315acb6bf10e99f332c8a43f00d5fbb1ee6ca48c52f6b936991b216c586aaad",
    strip_prefix = "googletest-1.15.0",
    urls = [
        "https://github.com/google/googletest/releases/download/v1.15.0/googletest-1.15.0.tar.gz",  # 2024-07-15
    ],
)

load("@com_google_googletest//:googletest_deps.bzl", "googletest_deps")

googletest_deps()

