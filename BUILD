load("@my_deps//:requirements.bzl", "requirement")

py_binary(
  name = "test_numpy",
  srcs = ["//:test_numpy.py"],
  deps = select({
    ":mac": ["//thirdparty/numpy_mac:pkg"],
    ":linux": ["//thirdparty/numpy_linux:pkg"],
    "//conditions:default": [],
  }),
)

config_setting(
  name = "mac",
  values = {"define": "platform=mac"},
)

config_setting(
  name = "linux",
  values = {"define": "platform=linux"},
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

