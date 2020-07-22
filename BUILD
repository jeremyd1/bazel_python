load("@my_deps//:requirements.bzl", "requirement")

py_binary(
  name = "test_numpy",
  srcs = ["//:test_numpy.py"],
  deps = [
      "//thirdparty/numpy_mac:pkg"
      ],
)

py_binary(
  name = "test_pandas",
  srcs = ["//:test_pandas.py"],
  deps = [
      requirement("pandas"),
      ],
)

py_binary(
 name = "empty",
 srcs = ["//:empty.py"], 
)


platform(
    name = "k8s",
    constraint_values = [
        "@platforms//os:linux",
        "@platforms//cpu:x86_64",
    ],
)

