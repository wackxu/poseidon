load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "coco_interference_scores.pb.go",
        "firmament_client.go",
        "firmament_scheduler.pb.go",
        "firmament_scheduler_mock.go",
        "job_desc.pb.go",
        "label.pb.go",
        "label_selector.pb.go",
        "reference_desc.pb.go",
        "resource_desc.pb.go",
        "resource_stats.pb.go",
        "resource_topology_node_desc.pb.go",
        "resource_vector.pb.go",
        "scheduling_delta.pb.go",
        "task_desc.pb.go",
        "task_final_report.pb.go",
        "task_stats.pb.go",
        "whare_map_stats.pb.go",
    ],
    importpath = "github.com/kubernetes-sigs/poseidon/pkg/firmament",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/golang/mock/gomock:go_default_library",
        "//vendor/github.com/golang/protobuf/proto:go_default_library",
        "//vendor/golang.org/x/net/context:go_default_library",
        "//vendor/google.golang.org/grpc:go_default_library",
        "//vendor/google.golang.org/grpc/grpclog:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["firmament_client_test.go"],
    embed = [":go_default_library"],
    deps = ["//vendor/github.com/golang/mock/gomock:go_default_library"],
)
