load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "29b9585e396fb027461c573f6dfbfe2773f9490234a2a9a09dca0f1e0e6ac24b",
    strip_prefix = "rules_go-e56822c37c2f3d4e6aff7937b570e9db9ab753ff",
    url = "https://github.com/bazelbuild/rules_go/archive/e56822c37c2f3d4e6aff7937b570e9db9ab753ff.tar.gz",
)

http_archive(
    name = "bazel_gazelle",
    sha256 = "f490124dd4b97c136cb8565f3aeefc2f2c1736afda7728b9b227b2b8aeadc88c",
    strip_prefix = "bazel-gazelle-44ce230b3399a5d4472198740358fcd825b0c3c9",
    url = "https://github.com/bazelbuild/bazel-gazelle/archive/44ce230b3399a5d4472198740358fcd825b0c3c9.tar.gz",
)

load("@io_bazel_rules_go//go:def.bzl", "go_register_toolchains", "go_rules_dependencies")

go_rules_dependencies()
go_register_toolchains(nogo = "@//:nogo")

load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")

gazelle_dependencies()