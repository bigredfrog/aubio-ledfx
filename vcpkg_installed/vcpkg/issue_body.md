Package: ffmpeg[avcodec,avformat,core,swresample]:x64-linux@7.1.2#2

**Host Environment**

- Host: x64-linux
- Compiler: GNU 13.3.0
- CMake Version: 3.31.6
-    vcpkg-tool version: 2025-10-16-71538f2694db93da4668782d094768ba74c45991
    vcpkg-scripts version: e3ed41868d 2025-10-31 (10 days ago)

**To Reproduce**

`vcpkg install `

**Failure logs**

```
Downloading https://github.com/ffmpeg/ffmpeg/archive/n7.1.2.tar.gz -> ffmpeg-ffmpeg-n7.1.2.tar.gz
Successfully downloaded ffmpeg-ffmpeg-n7.1.2.tar.gz
-- Extracting source /usr/local/share/vcpkg/downloads/ffmpeg-ffmpeg-n7.1.2.tar.gz
-- Applying patch 0001-create-lib-libraries.patch
-- Applying patch 0002-fix-msvc-link.patch
-- Applying patch 0003-fix-windowsinclude.patch
-- Applying patch 0004-dependencies.patch
-- Applying patch 0005-fix-nasm.patch
-- Applying patch 0007-fix-lib-naming.patch
-- Applying patch 0013-define-WINVER.patch
-- Applying patch 0020-fix-aarch64-libswscale.patch
-- Applying patch 0024-fix-osx-host-c11.patch
-- Applying patch 0040-ffmpeg-add-av_stream_get_first_dts-for-chromium.patch
-- Applying patch 0041-add-const-for-opengl-definition.patch
-- Applying patch 0043-fix-miss-head.patch
-- Applying patch 0044-fix-vulkan-debug-callback-abi.patch
-- Using source at /usr/local/share/vcpkg/buildtrees/ffmpeg/src/n7.1.2-a0bd95c46c.clean
CMake Error at scripts/cmake/vcpkg_find_acquire_program.cmake:166 (message):
  Could not find nasm.  Please install it via your package manager:

      sudo apt-get install nasm
Call Stack (most recent call first):
  ports/ffmpeg/portfile.cmake:28 (vcpkg_find_acquire_program)
  scripts/ports.cmake:206 (include)



```

**Additional context**

<details><summary>vcpkg.json</summary>

```
{
  "$schema": "https://raw.githubusercontent.com/microsoft/vcpkg-tool/main/docs/vcpkg.schema.json",
  "name": "aubio-ledfx",
  "version-string": "0.5.0-alpha",
  "description": "aubio is a library for audio and music analysis, synthesis, and effects",
  "dependencies": [
    "pkgconf",
    {
      "name": "libsndfile",
      "default-features": false,
      "features": [
        "external-libs"
      ]
    },
    "libsamplerate",
    "fftw3",
    "rubberband",
    {
      "name": "ffmpeg",
      "default-features": false,
      "features": [
        "avcodec",
        "avformat",
        "swresample"
      ]
    }
  ]
}

```
</details>
