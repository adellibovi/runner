## Features

- Bump runtime to dotnet 6 (#1471)
- Show service container logs on teardown (#1563)

## Bugs

- Add masks for multiline secrets from ::add-mask:: (#1521)
- fix Log size and retention settings not work (#1507)
- Refactor SelfUpdater adding L0 tests. (#1564)
- Fix test failure: /bin/sleep on Macos 11 (Monterey) does not accept the suffix s. (#1472)


## Misc

- Update dependency check for dotnet 6. (#1551)
- Produce trimmed down runner packages. (#1556)
- Deleted extra background in github-praph.png, which is displayed in README.md (#1432)


## Windows x64
We recommend configuring the runner in a root folder of the Windows drive (e.g. "C:\actions-runner"). This will help avoid issues related to service identity folder permissions and long file path restrictions on Windows.

The following snipped needs to be run on `powershell`:
``` powershell
# Create a folder under the drive root
mkdir \actions-runner ; cd \actions-runner
# Download the latest runner package
Invoke-WebRequest -Uri https://github.com/actions/runner/releases/download/v<RUNNER_VERSION>/actions-runner-win-x64-<RUNNER_VERSION>.zip -OutFile actions-runner-win-x64-<RUNNER_VERSION>.zip
# Extract the installer
Add-Type -AssemblyName System.IO.Compression.FileSystem ;
[System.IO.Compression.ZipFile]::ExtractToDirectory("$PWD\actions-runner-win-x64-<RUNNER_VERSION>.zip", "$PWD")
```

## OSX

``` bash
# Create a folder
mkdir actions-runner && cd actions-runner
# Download the latest runner package
curl -O -L https://github.com/actions/runner/releases/download/v<RUNNER_VERSION>/actions-runner-osx-x64-<RUNNER_VERSION>.tar.gz
# Extract the installer
tar xzf ./actions-runner-osx-x64-<RUNNER_VERSION>.tar.gz
```

## Linux x64

``` bash
# Create a folder
mkdir actions-runner && cd actions-runner
# Download the latest runner package
curl -O -L https://github.com/actions/runner/releases/download/v<RUNNER_VERSION>/actions-runner-linux-x64-<RUNNER_VERSION>.tar.gz
# Extract the installer
tar xzf ./actions-runner-linux-x64-<RUNNER_VERSION>.tar.gz
```

## Linux arm64

``` bash
# Create a folder
mkdir actions-runner && cd actions-runner
# Download the latest runner package
curl -O -L https://github.com/actions/runner/releases/download/v<RUNNER_VERSION>/actions-runner-linux-arm64-<RUNNER_VERSION>.tar.gz
# Extract the installer
tar xzf ./actions-runner-linux-arm64-<RUNNER_VERSION>.tar.gz
```

## Linux arm

``` bash
# Create a folder
mkdir actions-runner && cd actions-runner
# Download the latest runner package
curl -O -L https://github.com/actions/runner/releases/download/v<RUNNER_VERSION>/actions-runner-linux-arm-<RUNNER_VERSION>.tar.gz
# Extract the installer
tar xzf ./actions-runner-linux-arm-<RUNNER_VERSION>.tar.gz
```

## Using your self hosted runner
For additional details about configuring, running, or shutting down the runner please check out our [product docs.](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/adding-self-hosted-runners)

## SHA-256 Checksums

The SHA-256 checksums for the packages included in this build are shown below:

- actions-runner-win-x64-<RUNNER_VERSION>.zip <!-- BEGIN SHA win-x64 --><WIN_X64_SHA><!-- END SHA win-x64 -->
- actions-runner-osx-x64-<RUNNER_VERSION>.tar.gz <!-- BEGIN SHA osx-x64 --><OSX_X64_SHA><!-- END SHA osx-x64 -->
- actions-runner-linux-x64-<RUNNER_VERSION>.tar.gz <!-- BEGIN SHA linux-x64 --><LINUX_X64_SHA><!-- END SHA linux-x64 -->
- actions-runner-linux-arm64-<RUNNER_VERSION>.tar.gz <!-- BEGIN SHA linux-arm64 --><LINUX_ARM64_SHA><!-- END SHA linux-arm64 -->
- actions-runner-linux-arm-<RUNNER_VERSION>.tar.gz <!-- BEGIN SHA linux-arm --><LINUX_ARM_SHA><!-- END SHA linux-arm -->

- actions-runner-win-x64-<RUNNER_VERSION>-noexternals.zip <!-- BEGIN SHA win-x64_noexternals --><WIN_X64_SHA_NOEXTERNALS><!-- END SHA win-x64_noexternals -->
- actions-runner-osx-x64-<RUNNER_VERSION>-noexternals.tar.gz <!-- BEGIN SHA osx-x64_noexternals --><OSX_X64_SHA_NOEXTERNALS><!-- END SHA osx-x64_noexternals -->
- actions-runner-linux-x64-<RUNNER_VERSION>-noexternals.tar.gz <!-- BEGIN SHA linux-x64_noexternals --><LINUX_X64_SHA_NOEXTERNALS><!-- END SHA linux-x64_noexternals -->
- actions-runner-linux-arm64-<RUNNER_VERSION>-noexternals.tar.gz <!-- BEGIN SHA linux-arm64_noexternals --><LINUX_ARM64_SHA_NOEXTERNALS><!-- END SHA linux-arm64_noexternals -->
- actions-runner-linux-arm-<RUNNER_VERSION>-noexternals.tar.gz <!-- BEGIN SHA linux-arm_noexternals --><LINUX_ARM_SHA_NOEXTERNALS><!-- END SHA linux-arm_noexternals -->

- actions-runner-win-x64-<RUNNER_VERSION>-noruntime.zip <!-- BEGIN SHA win-x64_noruntime --><WIN_X64_SHA_NORUNTIME><!-- END SHA win-x64_noruntime -->
- actions-runner-osx-x64-<RUNNER_VERSION>-noruntime.tar.gz <!-- BEGIN SHA osx-x64_noruntime --><OSX_X64_SHA_NORUNTIME><!-- END SHA osx-x64_noruntime -->
- actions-runner-linux-x64-<RUNNER_VERSION>-noruntime.tar.gz <!-- BEGIN SHA linux-x64_noruntime --><LINUX_X64_SHA_NORUNTIME><!-- END SHA linux-x64_noruntime -->
- actions-runner-linux-arm64-<RUNNER_VERSION>-noruntime.tar.gz <!-- BEGIN SHA linux-arm64_noruntime --><LINUX_ARM64_SHA_NORUNTIME><!-- END SHA linux-arm64_noruntime -->
- actions-runner-linux-arm-<RUNNER_VERSION>-noruntime.tar.gz <!-- BEGIN SHA linux-arm_noruntime --><LINUX_ARM_SHA_NORUNTIME><!-- END SHA linux-arm_noruntime -->

- actions-runner-win-x64-<RUNNER_VERSION>-noruntime-noexternals.zip <!-- BEGIN SHA win-x64_noruntime_noexternals --><WIN_X64_SHA_NORUNTIME_NOEXTERNALS><!-- END SHA win-x64_noruntime_noexternals -->
- actions-runner-osx-x64-<RUNNER_VERSION>-noruntime-noexternals.tar.gz <!-- BEGIN SHA osx-x64_noruntime_noexternals --><OSX_X64_SHA_NORUNTIME_NOEXTERNALS><!-- END SHA osx-x64_noruntime_noexternals -->
- actions-runner-linux-x64-<RUNNER_VERSION>-noruntime-noexternals.tar.gz <!-- BEGIN SHA linux-x64_noruntime_noexternals --><LINUX_X64_SHA_NORUNTIME_NOEXTERNALS><!-- END SHA linux-x64_noruntime_noexternals -->
- actions-runner-linux-arm64-<RUNNER_VERSION>-noruntime-noexternals.tar.gz <!-- BEGIN SHA linux-arm64_noruntime_noexternals --><LINUX_ARM64_SHA_NORUNTIME_NOEXTERNALS><!-- END SHA linux-arm64_noruntime_noexternals -->
- actions-runner-linux-arm-<RUNNER_VERSION>-noruntime-noexternals.tar.gz <!-- BEGIN SHA linux-arm_noruntime_noexternals --><LINUX_ARM_SHA_NORUNTIME_NOEXTERNALS><!-- END SHA linux-arm_noruntime_noexternals -->
