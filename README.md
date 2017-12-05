# proto_library

This Bazel demonstrates how to use Bazel's built-in support for [Protocol Buffers](https://developers.google.com/protocol-buffers/).

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

_Tested with Bazel 0.8.0._
