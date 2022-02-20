load("@build_bazel_rules_apple//apple:ios.bzl", "ios_app_clip", "ios_application", "ios_extension")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

package(default_visibility = ["//visibility:public"])

ios_application(
    name = "Fruta",
    app_clips = [":FrutaAppClip"],
    app_icons = ["//Shared/Resources:AppIcon"],
    bundle_id = "com.example.apple-samplecode.fruta-extended",
    extensions = [":FrutaWidget"],
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = ["Info.plist"],
    minimum_os_version = "15.0",
    resources = ["//Shared/Resources:Assets"],
    deps = [":FrutaLib"],
)

swift_library(
    name = "FrutaLib",
    srcs = [
        "AppTabNavigation.swift",
        "//Shared:FrutaApp.swift",
        "//Shared:SharedSources",
    ],
    module_name = "FrutaLib",
)

ios_extension(
    name = "FrutaWidget",
    bundle_id = "com.example.apple-samplecode.fruta-extended.ios-widgets",
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = ["Info-Widget.plist"],
    minimum_os_version = "15.0",
    deps = [":FrutaWidgetLib"],
)

swift_library(
    name = "FrutaWidgetLib",
    srcs = [
        "AppTabNavigation.swift",
        "//Shared:SharedSources",
        "//Widgets:FrutaWidgetSources",
    ],
    module_name = "FrutaWidgetLib",
)

ios_app_clip(
    name = "FrutaAppClip",
    bundle_id = "com.example.apple-samplecode.fruta-extended.Clip",
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = ["Info-Clip.plist"],
    minimum_os_version = "15.0",
    deps = [
        ":FrutaAppClipLib",
    ],
)

swift_library(
    name = "FrutaAppClipLib",
    srcs = [
        "AppTabNavigation.swift",
        "FrutaAppClip.swift",
        "//Shared:SharedSources",
    ],
    module_name = "FrutaAppClipLib",
)
