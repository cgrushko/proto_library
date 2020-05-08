# proto_library

This Bazel demonstrates how to use Bazel's built-in support for
[Protocol Buffers](https://developers.google.com/protocol-buffers/).

```bash
$ bazel build //src:person_java_proto_lite
Target //src:person_java_proto up-to-date:
  bazel-bin/src/libperson_proto-lite.jar
  ...
$ bazel build //src:person_java_proto
Target //src:person_java_proto up-to-date:
  bazel-bin/src/libperson_proto-speed.jar
  ...
$ bazel build //src:person_cc_proto
Target //src:person_java_proto up-to-date:
  bazel-bin/src/libperson_proto.so
  ...
$ bazel build //src:person_proto
Target //src:person_java_proto up-to-date:
  bazel-genfiles/src/person_proto-descriptor-set.proto.bin
```

## Supporting Bazel 2.x and earlier

Before Bazel 3.0, `java_lite_proto_library` had an implicit dependency on `@com_google_protobuf_javalite//:javalite_toolchain`. In order to support
Bazel 2.x and earlier, you need to provide this dependency. Because the
java lite toolchain has been included in the main protobuf repo since v3.11,
it is recommended to use v3.11 at a minimum in order to support both Bazel 3.x
and Bazel 2.x. To do this, add this to your WORKSPACE file:

```
# The 'com_google_protobuf_javalite' package is required for Bazel 2.x and below.
http_archive(
    name = "com_google_protobuf_javalite",
    sha256 = "832c476bb442ca98a59c2291b8a504648d1c139b74acc15ef667a0e8f5e984e7",
    strip_prefix = "protobuf-3.11.3",
    urls = ["https://github.com/protocolbuffers/protobuf/archive/v3.11.3.zip"],
)
```
