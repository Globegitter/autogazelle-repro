load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "ac3f9989ae4032d9d90c3c10216cf3a645cf4fb1b235fe6e196f97b62d39a95d",
    strip_prefix = "rules_go-f9fac1f422e7e805085aed95631c28319354bf7b",
    url = "https://github.com/bazelbuild/rules_go/archive/f9fac1f422e7e805085aed95631c28319354bf7b.tar.gz",
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

go_repository(
    name = "com_github_rs_zerolog",
    commit = "9cd6f6eef2d7e9041629e2dd853778a9b2abddbd",
    importpath = "github.com/rs/zerolog",
)
