load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["logs.go"],
    importpath = "k8s.io/kubernetes/pkg/kubelet/kuberuntime/logs",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/kubelet/apis/cri:go_default_library",
        "//pkg/kubelet/apis/cri/runtime/v1alpha2:go_default_library",
        "//pkg/util/tail:go_default_library",
        "//vendor/github.com/docker/docker/pkg/jsonlog:go_default_library",
        "//vendor/github.com/fsnotify/fsnotify:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["logs_test.go"],
    embed = [":go_default_library"],
    importpath = "k8s.io/kubernetes/pkg/kubelet/kuberuntime/logs",
    deps = [
        "//pkg/kubelet/apis/cri/runtime/v1alpha2:go_default_library",
        "//vendor/github.com/stretchr/testify/assert:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
