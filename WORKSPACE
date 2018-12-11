load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
git_repository(
    name = "rules_idris",
    remote = "https://github.com/BryghtWords/rules_idris.git",
    tag = "v0.3"
)

load("@rules_idris//idris:idris_repos.bzl", "loadIdrisPackagerRepositories")

loadIdrisPackagerRepositories()

load("@rules_idris//idris:local_idris_loader.bzl", "loadIdris")

loadIdris("/nix/store/iz7jahxg47hzhwapiwlc2xr2nqsixdkq-idris-1.3.1")

git_repository(
    name = "smoke-hill",
    remote = "https://github.com/shmish111/smoke-hill.git",
    commit = "73addb298b9b4d3cb7188c03627ff36ed16cd932",
)
load("@smoke-hill//:packages.bzl", "loadIdrisPackages")
loadIdrisPackages()
