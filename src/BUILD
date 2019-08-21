load("@rules_cc//cc:defs.bzl", "cc_library")
load("@rules_java//java:defs.bzl", "java_library")
load("@rules_proto//proto:defs.bzl", "proto_library")

# Convention:
# A java_proto_library that wraps a proto_library named foo_proto
# should be called foo_java_proto.
#
# Note that you only need a java_proto_library for the protos
# you directly use in your code - a java_proto_library converts
# an entire proto graph.
java_proto_library(
    name = "person_java_proto",
    deps = [":person_proto"],
)

# Convention:
# A java_lite_proto_library that wraps a proto_library named foo_proto
# should be called foo_java_proto_lite.
java_lite_proto_library(
    name = "person_java_proto_lite",
    deps = [":person_proto"],
)

# Convention:
# A cc_proto_library that wraps a proto_library named foo_proto
# should be called foo_cc_proto.
cc_proto_library(
    name = "person_cc_proto",
    deps = [":person_proto"],
)

# Conventions:
# 1. One proto_library rule per .proto file.
# 2. A file named foo.proto will be in a rule named foo_proto.
proto_library(
    name = "person_proto",
    srcs = ["person.proto"],
    deps = [
        ":address_proto",
        # Well known protos should be included as deps in the
        # proto_library rules of the source files importing them.
        # A list of all @com_google_protobuf well known protos can
        # seen with:
        # `bazel query 'kind(proto_library, @com_google_protobuf//:all)'`
        "@com_google_protobuf//:any_proto",
    ],
)

proto_library(
    name = "address_proto",
    srcs = ["address.proto"],
    deps = [":zip_code_proto"],
)

proto_library(
    name = "zip_code_proto",
    srcs = ["zip_code.proto"],
)
