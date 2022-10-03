load("@npm//:defs.bzl", "npm_link_all_packages")
load("@npm//:sass/package_json.bzl", sass_bin = "bin")

# Link all direct dependencies in package.json to
# bazel-bin/npm_deps/node_modules
npm_link_all_packages(name = "node_modules")

sass_bin.sass(
    name = "css",
    srcs = ["styles.scss"],
    outs = ["styles.css"],
    args = [
        "$(execpath {})".format("styles.scss"),
        "../../../$@",
    ],
    visibility = ["//visibility:private"],
)