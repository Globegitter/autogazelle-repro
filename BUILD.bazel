load("@bazel_gazelle//:def.bzl", "gazelle")
load("@io_bazel_rules_go//go:def.bzl", "nogo")

nogo(
    name = "nogo",
    vet = True,
    visibility = ["//visibility:public"],  # must have public visibility
)

gazelle(
    name = "gazelle",
    prefix = "github.com/ecosia/core",
)
