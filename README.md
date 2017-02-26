# proto_library

NOTE: Bazel 0.4.4 lacks some features the example uses - you'll need to build Bazel from head. The easiest is to install Bazel, download Bazel's source code, build it (`bazel build //src:bazel`) and copy it somewhere (e.g., `cp bazel-bin/src/bazel ~/bazel`)

This Bazel demonstrates how to use Bazel's built-in support for [Protocol Buffers](https://developers.google.com/protocol-buffers/).

```bash
$ ~/bazel build //src:person_java_proto
Target //src:person_java_proto up-to-date:
  bazel-bin/src/libperson_proto-speed.jar
  ...
$ ~/bazel build //src:person_cc_proto
Target //src:person_java_proto up-to-date:
  bazel-bin/src/libperson_proto.so
  ...
$ ~/bazel build //src:person_proto
Target //src:person_java_proto up-to-date:
  bazel-genfiles/src/person_proto-descriptor-set.proto.bin
```
