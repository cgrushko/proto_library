# proto_library rules implicitly depend on @com_google_protobuf//:protoc,
# which is the proto-compiler.
# This statement defines the @com_google_protobuf repo.
git_repository(
    name = "com_google_protobuf",
    remote = "https://github.com/google/protobuf.git",
    commit = "b4b0e304be5a68de3d0ee1af9b286f958750f5e4",
)

# cc_proto_library rules implicitly depend on @com_google_protobuf_cc//:cc_toolchain,
# which is the C++ proto runtime (base classes and common utilities).
git_repository(
    name = "com_google_protobuf_cc",
    remote = "https://github.com/google/protobuf.git",
    commit = "b4b0e304be5a68de3d0ee1af9b286f958750f5e4",
)

# java_proto_library rules implicitly depend on @com_google_protobuf_java//:java_toolchain,
# which is the Java proto runtime (base classes and common utilities).
git_repository(
    name = "com_google_protobuf_java",
    remote = "https://github.com/google/protobuf.git",
    commit = "b4b0e304be5a68de3d0ee1af9b286f958750f5e4",
)

# java_lite_proto_library rules implicitly depend on @com_google_protobuf_javalite//:javalite_toolchain,
# which is the JavaLite proto runtime (base classes and common utilities).
git_repository(
    name = "com_google_protobuf_javalite",
    remote = "https://github.com/google/protobuf.git",
    commit = "82809aaebf24fca3c2d5611149c78a3625bd3b70",
)
