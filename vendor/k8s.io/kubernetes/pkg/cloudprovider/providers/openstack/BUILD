package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "metadata.go",
        "openstack.go",
        "openstack_client.go",
        "openstack_instances.go",
        "openstack_loadbalancer.go",
        "openstack_metrics.go",
        "openstack_routes.go",
        "openstack_volumes.go",
    ],
    importpath = "k8s.io/kubernetes/pkg/cloudprovider/providers/openstack",
    deps = [
        "//pkg/util/mount:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/net:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//staging/src/k8s.io/client-go/informers:go_default_library",
        "//staging/src/k8s.io/client-go/listers/core/v1:go_default_library",
        "//staging/src/k8s.io/client-go/util/cert:go_default_library",
        "//staging/src/k8s.io/cloud-provider:go_default_library",
        "//staging/src/k8s.io/cloud-provider/node/helpers:go_default_library",
        "//staging/src/k8s.io/cloud-provider/service/helpers:go_default_library",
        "//staging/src/k8s.io/cloud-provider/volume:go_default_library",
        "//staging/src/k8s.io/cloud-provider/volume/errors:go_default_library",
        "//staging/src/k8s.io/cloud-provider/volume/helpers:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/blockstorage/extensions/volumeactions:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/blockstorage/v1/volumes:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/blockstorage/v2/volumes:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/blockstorage/v3/volumes:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/compute/v2/extensions/attachinterfaces:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/compute/v2/extensions/volumeattach:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/compute/v2/servers:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/identity/v3/extensions/trusts:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/identity/v3/tokens:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/external:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/layer3/floatingips:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/layer3/routers:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/lbaas_v2/listeners:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/lbaas_v2/loadbalancers:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/lbaas_v2/monitors:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/lbaas_v2/pools:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/security/groups:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/security/rules:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/networks:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/ports:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/pagination:go_default_library",
        "//vendor/github.com/mitchellh/mapstructure:go_default_library",
        "//vendor/github.com/prometheus/client_golang/prometheus:go_default_library",
        "//vendor/gopkg.in/gcfg.v1:go_default_library",
        "//vendor/k8s.io/klog:go_default_library",
        "//vendor/k8s.io/utils/exec:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "metadata_test.go",
        "openstack_routes_test.go",
        "openstack_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/rand:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//staging/src/k8s.io/cloud-provider:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/compute/v2/servers:go_default_library",
        "//vendor/github.com/gophercloud/gophercloud/openstack/networking/v2/extensions/layer3/routers:go_default_library",
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
)
