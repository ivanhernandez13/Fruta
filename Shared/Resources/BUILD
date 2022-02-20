package(default_visibility = ["//visibility:public"])

filegroup(
    name = "AppIcon",
    srcs = glob(["Assets.xcassets/AppIcon.appiconset/**"]),
)

filegroup(
    name = "Assets",
    srcs = glob(
        ["**/*"],
        exclude = ["Assets.xcassets/*.appiconset/**"],
    ),
)
