load("@build_bazel_rules_apple//apple:macos.bzl", "macos_application", "macos_extension")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

package(default_visibility = ["//visibility:public"])

macos_application(
    name = "Fruta",
    app_icons = ["//Shared/Resources:AppIcon"],
    bundle_id = "com.example.apple-samplecode.fruta",
    extensions = [":FrutaWidget"],
    infoplists = ["Info.plist"],
    minimum_os_version = "12.0",
    resources = ["//Shared/Resources:Assets"],
    deps = [":FrutaLib"],
)

swift_library(
    name = "FrutaLib",
    srcs = [
        "//Shared:FrutaApp.swift",
        "//Shared:SharedSources",
    ],
    module_name = "FrutaLib",
)

macos_extension(
    name = "FrutaWidget",
    bundle_id = "com.example.apple-samplecode.fruta.macos-widgets",
    infoplists = ["Info-Widget.plist"],
    minimum_os_version = "12.0",
    deps = [
        ":FrutaWidgetLib",
    ],
)

swift_library(
    name = "FrutaWidgetLib",
    srcs = [
        "//Shared:SharedSources",
        "//Widgets:FrutaWidgetSources",
    ],
    module_name = "FrutaWidgetLib",
)
