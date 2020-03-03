# proto_library

This Bazel demonstrates how to use Bazel's built-in support for
[Protocol Buffers](https://developers.google.com/protocol-buffers/).

> :bangbang: Before Bazel 3.0, `java_lite_proto_library` had an implicit
  dependency on `@com_google_protobuf_javalite//:javalite_toolchain`. Check
  [here](https://github.com/cgrushko/proto_library/blob/08e5522a99c41a188046e1f5af305d5c5d39c2d9/WORKSPACE#L38)
  for an example how to use `java_lite_proto_library` with Bazel 2.2 (or earlier).

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

_Tested with Bazel 3.0._
