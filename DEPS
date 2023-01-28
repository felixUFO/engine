# The dependencies referenced by the Flutter Engine.
#
# This file is referenced by the .gclient file at the root of the checkout.
# To preview changes to the dependencies, update this file and run
# `gclient sync`.
#
# When adding a new dependency, please update the top-level .gitignore file
# to list the dependency's destination directory.

vars = {
  'chromium_git': 'https://chromium.googlesource.com',
  'swiftshader_git': 'https://swiftshader.googlesource.com',
  'dart_git': 'https://dart.googlesource.com',
  'flutter_git': 'https://flutter.googlesource.com',
  'fuchsia_git': 'https://fuchsia.googlesource.com',
  'github_git': 'https://github.com',
  'skia_git': 'https://skia.googlesource.com',
  'llvm_git': 'https://llvm.googlesource.com',
  # OCMock is for testing only so there is no google clone
  'ocmock_git': 'https://github.com/erikdoe/ocmock.git',
  'skia_revision': '0b75650caf2a445133e67e7952bf8eb1646065ef',

  # WARNING: DO NOT EDIT canvaskit_cipd_instance MANUALLY
  # See `lib/web_ui/README.md` for how to roll CanvasKit to a new version.
  'canvaskit_cipd_instance': '61aeJQ9laGfEFF_Vlc_u0MCkqB6xb2hAYHRBxKH-Uw4C',

  # Do not download the Emscripten SDK by default.
  # This prevents us from downloading the Emscripten toolchain for builds
  # which do not build for the web. This toolchain is needed to build CanvasKit
  # for the web engine.
  'download_emsdk': False,

  # For experimental features some dependencies may only be avaialable in the master/main
  # channels. This variable is being set when CI is checking out the repository.
  'release_candidate': False,


  # As Dart does, we use Fuchsia's GN and Clang toolchain. These revision
  # should be kept up to date with the revisions pulled by Dart.
  # The list of revisions for these tools comes from Fuchsia, here:
  # https://fuchsia.googlesource.com/integration/+/HEAD/toolchain
  # If there are problems with the toolchain, contact fuchsia-toolchain@.
  'clang_version': 'git_revision:20d06c833d833ef6b2d0f519cc4a7998d49a2803',

  # When updating the Dart revision, ensure that all entries that are
  # dependencies of Dart are also updated to match the entries in the
  # Dart SDK's DEPS file for that revision of Dart. The DEPS file for
  # Dart is: https://github.com/dart-lang/sdk/blob/main/DEPS
  # You can use //tools/dart/create_updated_flutter_deps.py to produce
  # updated revision list of existing dependencies.
  'dart_revision': 'f9583e13e2144c31584aa28d76ddc2f388d60b5e',

  # WARNING: DO NOT EDIT MANUALLY
  # The lines between blank lines above and below are generated by a script. See create_updated_flutter_deps.py
  'dart_binaryen_rev': '4471b81a0a0b94c75bad6e81d0413860944ecb1f',
  'dart_boringssl_gen_rev': 'ced85ef0a00bbca77ce5a91261a5f2ae61b1e62f',
  'dart_boringssl_rev': '87f316d7748268eb56f2dc147bd593254ae93198',
  'dart_browser_launcher_rev': 'f2f01e4c7e719c633ca3c35d55c5331d4fe8b54b',
  'dart_clock_rev': '65e8a13ddf26c9d21884ccc8f8532725697d40df',
  'dart_collection_rev': '85e987cf1b8aaba60bdc8b16dd1ee6233436549f',
  'dart_devtools_rev': 'c7a81f64dabb4b9f2cae0cf2c9411ef8bb805191',
  'dart_libprotobuf_rev': '24487dd1045c7f3d64a21f38a3f0c06cc4cf2edb',
  'dart_perfetto_rev': 'b8da07095979310818f0efde2ef3c69ea70d62c5',
  'dart_protobuf_gn_rev': 'b9517855b24624ec4edf4a11c1b7060f4ef237e6',
  'dart_protobuf_rev': 'cc0f287fb6a8680e431eb9210225f1d0ac33c047',
  'dart_pub_rev': '0cbaf7a2fb8c8ca543c6f222bf25d5f5c63abbf3',
  'dart_root_certificates_rev': '692f6d6488af68e0121317a9c2c9eb393eb0ee50',
  'dart_watcher_rev': '3b49c7ea087cc158bdcba19fe8919283fdc1cd86',
  'dart_webdev_rev': 'a347fa038b5174a01a15ff121367cd7c987b4f6d',
  'dart_webkit_inspection_protocol_rev': '15244ffbab9221f1603eb04eaae74ae7c7ca3944',
  'dart_yaml_edit_rev': '299f74594ff9fda412c1da5c0b5d5231d0c6fc42',
  'dart_zlib_rev': '27c2f474b71d0d20764f86f60ef8b00da1a16cda',

  'ocmock_rev': 'c4ec0e3a7a9f56cfdbd0aa01f4f97bb4b75c5ef8', # v3.7.1

  # Download a prebuilt Dart SDK by default
  'download_dart_sdk': True,

  # Checkout Android dependencies only on platforms where we build for Android targets.
  'download_android_deps': 'host_os == "mac" or (host_os == "linux" and host_cpu == "x64")',

  # Checkout Windows dependencies only if we are building on Windows.
  'download_windows_deps' : 'host_os == "win"',

  # Checkout Linux dependencies only when building on Linux.
  'download_linux_deps': 'host_os == "linux"',

  # Downloads the fuchsia SDK as listed in fuchsia_sdk_path var. This variable
  # is currently only used for the Fuchsia LSC process and is not intended for
  # local development.
  'download_fuchsia_sdk': False,
  'fuchsia_sdk_path': '',

  # An LLVM backend needs LLVM binaries and headers. To avoid build time
  # increases we can use prebuilts. We don't want to download this on every
  # CQ/CI bot nor do we want the average Dart developer to incur that cost.
  # So by default we will not download prebuilts. This varible is needed in
  # the flutter engine to ensure that Dart gn has access to it as well.
  "checkout_llvm": False,

  # Setup Git hooks by default.
  "setup_githooks": True,

  # Upstream URLs for third party dependencies, used in
  # determining common ancestor commit for vulnerability scanning
  # prefixed with 'upstream_' in order to be identified by parsing tool.
  # The vulnerabiity database being used in this scan can be browsed
  # using this UI https://osv.dev/list
  # If a new dependency needs to be added, the upstream (non-mirrored)
  # git URL for that dependency should be added to this list 
  # with the key-value pair being:
  # 'upstream_[dep name from last slash and before .git in URL]':'[git URL]'
  # example: 
  "upstream_abseil-cpp": "https://github.com/abseil/abseil-cpp.git",
  "upstream_angle": "https://github.com/google/angle.git",
  "upstream_archive": "https://github.com/brendan-duncan/archive.git",
  "upstream_args": "https://github.com/dart-lang/args.git",
  "upstream_async": "https://github.com/dart-lang/async.git",
  "upstream_bazel_worker": "https://github.com/dart-lang/bazel_worker.git",
  "upstream_benchmark": "https://github.com/google/benchmark.git",
  "upstream_boolean_selector": "https://github.com/dart-lang/boolean_selector.git",
  "upstream_boringssl_gen": "https://github.com/dart-lang/boringssl_gen.git",
  "upstream_boringssl": "https://github.com/openssl/openssl.git",
  "upstream_browser_launcher": "https://github.com/dart-lang/browser_launcher.git",
  "upstream_buildroot": "https://github.com/flutter/buildroot.git",
  "upstream_cli_util": "https://github.com/dart-lang/cli_util.git",
  "upstream_clock": "https://github.com/dart-lang/clock.git",
  "upstream_collection": "https://github.com/dart-lang/collection.git",
  "upstream_colorama": "https://github.com/tartley/colorama.git",
  "upstream_convert": "https://github.com/dart-lang/convert.git",
  "upstream_crypto": "https://github.com/dart-lang/crypto.git",
  "upstream_csslib": "https://github.com/dart-lang/csslib.git",
  "upstream_dart_style": "https://github.com/dart-lang/dart_style.git",
  "upstream_dartdoc": "https://github.com/dart-lang/dartdoc.git",
  "upstream_equatable": "https://github.com/felangel/equatable.git",
  "upstream_ffi": "https://github.com/dart-lang/ffi.git",
  "upstream_file": "https://github.com/google/file.dart.git",
  "upstream_fixnum": "https://github.com/dart-lang/fixnum.git",
  "upstream_flatbuffers": "https://github.com/google/flatbuffers.git",
  "upstream_fontconfig": "https://gitlab.freedesktop.org/fontconfig/fontconfig.git",
  "upstream_freetype2": "https://gitlab.freedesktop.org/freetype/freetype.git",
  "upstream_gcloud": "https://github.com/dart-lang/gcloud.git",
  "upstream_glfw": "https://github.com/glfw/glfw.git",
  "upstream_glob": "https://github.com/dart-lang/glob.git",
  "upstream_googleapis": "https://github.com/google/googleapis.dart.git",
  "upstream_googletest": "https://github.com/google/googletest.git",
  "upstream_gtest-parallel": "https://github.com/google/gtest-parallel.git",
  "upstream_harfbuzz": "https://github.com/harfbuzz/harfbuzz.git",
  "upstream_html": "https://github.com/dart-lang/html.git",
  "upstream_http_multi_server": "https://github.com/dart-lang/http_multi_server.git",
  "upstream_http_parser": "https://github.com/dart-lang/http_parser.git",
  "upstream_http": "https://github.com/dart-lang/http.git",
  "upstream_icu": "https://github.com/unicode-org/icu.git",
  "upstream_intl": "https://github.com/dart-lang/intl.git",
  "upstream_imgui": "https://github.com/ocornut/imgui.git",
  "upstream_inja": "https://github.com/pantor/inja.git",
  "upstream_json": "https://github.com/nlohmann/json.git",
  "upstream_json_rpc_2": "https://github.com/dart-lang/json_rpc_2.git",
  "upstream_libcxx": "https://github.com/llvm-mirror/libcxx.git",
  "upstream_libcxxabi": "https://github.com/llvm-mirror/libcxxabi.git",
  "upstream_libexpat": "https://github.com/libexpat/libexpat.git",
  "upstream_libjpeg-turbo": "https://github.com/libjpeg-turbo/libjpeg-turbo.git",
  "upstream_libpng": "https://github.com/glennrp/libpng.git",
  "upstream_libtess2": "https://github.com/memononen/libtess2.git",
  "upstream_libwebp": "https://chromium.googlesource.com/webm/libwebp.git",
  "upstream_libxml": "https://gitlab.gnome.org/GNOME/libxml2.git",
  "upstream_linter": "https://github.com/dart-lang/linter.git",
  "upstream_logging": "https://github.com/dart-lang/logging.git",
  "upstream_markdown": "https://github.com/dart-lang/markdown.git",
  "upstream_matcher": "https://github.com/dart-lang/matcher.git",
  "upstream_mime": "https://github.com/dart-lang/mime.git",
  "upstream_mockito": "https://github.com/dart-lang/mockito.git",
  "upstream_oauth2": "https://github.com/dart-lang/oauth2.git",
  "upstream_ocmock": "https://github.com/erikdoe/ocmock.git",
  "upstream_package_config": "https://github.com/dart-lang/package_config.git",
  "upstream_packages": "https://github.com/flutter/packages.git",
  "upstream_path": "https://github.com/dart-lang/path.git",
  "upstream_platform": "https://github.com/google/platform.dart.git",
  "upstream_pool": "https://github.com/dart-lang/pool.git",
  "upstream_process_runner": "https://github.com/google/process_runner.git",
  "upstream_process": "https://github.com/google/process.dart.git",
  "upstream_protobuf": "https://github.com/google/protobuf.dart.git",
  "upstream_pub_semver": "https://github.com/dart-lang/pub_semver.git",
  "upstream_pub": "https://github.com/dart-lang/pub.git",
  "upstream_pyyaml": "https://github.com/yaml/pyyaml.git",
  "upstream_quiver-dart": "https://github.com/google/quiver-dart.git",
  "upstream_rapidjson": "https://github.com/Tencent/rapidjson.git",
  "upstream_root_certificates": "https://github.com/dart-lang/root_certificates.git",
  "upstream_sdk": "https://github.com/dart-lang/sdk.git",
  "upstream_shaderc": "https://github.com/google/shaderc.git",
  "upstream_shelf": "https://github.com/dart-lang/shelf.git",
  "upstream_skia": "https://skia.googlesource.com/skia.git",
  "upstream_source_map_stack_trace": "https://github.com/dart-lang/source_map_stack_trace.git",
  "upstream_source_maps": "https://github.com/dart-lang/source_maps.git",
  "upstream_source_span": "https://github.com/dart-lang/source_span.git",
  "upstream_sqlite": "https://github.com/sqlite/sqlite.git",
  "upstream_sse": "https://github.com/dart-lang/sse.git",
  "upstream_stack_trace": "https://github.com/dart-lang/stack_trace.git",
  "upstream_stream_channel": "https://github.com/dart-lang/stream_channel.git",
  "upstream_string_scanner": "https://github.com/dart-lang/string_scanner.git",
  "upstream_SwiftShader": "https://swiftshader.googlesource.com/SwiftShader.git",
  "upstream_term_glyph": "https://github.com/dart-lang/term_glyph.git",
  "upstream_test_reflective_loader": "https://github.com/dart-lang/test_reflective_loader.git",
  "upstream_test": "https://github.com/dart-lang/test.git",
  "upstream_tinygltf": "https://github.com/syoyo/tinygltf.git",
  "upstream_typed_data": "https://github.com/dart-lang/typed_data.git",
  "upstream_usage": "https://github.com/dart-lang/usage.git",
  "upstream_vector_math": "https://github.com/google/vector_math.dart.git",
  "upstream_Vulkan-Headers": "https://github.com/KhronosGroup/Vulkan-Headers.git",
  "upstream_VulkanMemoryAllocator": "https://github.com/GPUOpen-LibrariesAndSDKs/VulkanMemoryAllocator.git",
  "upstream_watcher": "https://github.com/dart-lang/watcher.git",
  "upstream_web_socket_channel": "https://github.com/dart-lang/web_socket_channel.git",
  "upstream_webdev": "https://github.com/dart-lang/webdev.git",
  "upstream_webkit_inspection_protocol": "https://github.com/google/webkit_inspection_protocol.dart.git",
  "upstream_wuffs-mirror-release-c": "https://github.com/google/wuffs-mirror-release-c.git",
  "upstream_yaml_edit": "https://github.com/dart-lang/yaml_edit.git",
  "upstream_yaml": "https://github.com/dart-lang/yaml.git",
  "upstream_yapf": "https://github.com/google/yapf.git",
  "upstream_zlib": "https://github.com/madler/zlib.git",
}

gclient_gn_args_file = 'src/third_party/dart/build/config/gclient_args.gni'
gclient_gn_args = [
  'checkout_llvm'
]

# Only these hosts are allowed for dependencies in this DEPS file.
# If you need to add a new host, contact chrome infrastructure team.
allowed_hosts = [
  'boringssl.googlesource.com',
  'chrome-infra-packages.appspot.com',
  'chromium.googlesource.com',
  'dart.googlesource.com',
  'flutter.googlesource.com',
  'fuchsia.googlesource.com',
  'llvm.googlesource.com',
  'skia.googlesource.com',
  'swiftshader.googlesource.com',
]

deps = {
  'src': 'https://github.com/flutter/buildroot.git' + '@' + 'c77cac9502fb108be6a1ed4e0e4e1c65649b3a35',

   # Fuchsia compatibility
   #
   # The dependencies in this section should match the layout in the Fuchsia gn
   # build. Eventually, we'll manage these dependencies together with Fuchsia
   # and not have to specific hashes.

  'src/third_party/rapidjson':
   Var('fuchsia_git') + '/third_party/rapidjson' + '@' + 'ef3564c5c8824989393b87df25355baf35ff544b',

  'src/third_party/harfbuzz':
   Var('flutter_git') + '/third_party/harfbuzz' + '@' + 'd40d15e994ed60d32bcfc9ab87004dfb028dfbd6',

  'src/third_party/libcxx':
   Var('llvm_git') + '/llvm-project/libcxx' + '@' + '44079a4cc04cdeffb9cfe8067bfb3c276fb2bab0',

  'src/third_party/libcxxabi':
   Var('llvm_git') + '/llvm-project/libcxxabi' + '@' + '2ce528fb5e0f92e57c97ec3ff53b75359d33af12',

  'src/third_party/glfw':
   Var('fuchsia_git') + '/third_party/glfw' + '@' + 'dd8a678a66f1967372e5a5e3deac41ebf65ee127',

  'src/third_party/shaderc':
   Var('github_git') + '/google/shaderc.git' + '@' + '7ea834ecc59258a5c13c3d3e6fa0582bdde7c543',

  'src/third_party/vulkan-deps':
   Var('chromium_git') + '/vulkan-deps' + '@' + 'a56166d59ebdb0208a7301d267460773df1a1adc',

  'src/third_party/flatbuffers':
   Var('github_git') + '/google/flatbuffers.git' + '@' + '0a80646371179f8a7a5c1f42c31ee1d44dcf6709',

  'src/third_party/icu':
   Var('chromium_git') + '/chromium/deps/icu.git' + '@' + '2cce76fd67afce170560afaaac1872efefe64fdb',

  'src/third_party/khronos':
   Var('chromium_git') + '/chromium/src/third_party/khronos.git' + '@' + '676d544d2b8f48903b7da9fceffaa534a5613978',

   'src/third_party/gtest-parallel':
   Var('chromium_git') + '/external/github.com/google/gtest-parallel' + '@' + '38191e2733d7cbaeaef6a3f1a942ddeb38a2ad14',

  'src/third_party/benchmark':
   Var('github_git') + '/google/benchmark' + '@' + '431abd149fd76a072f821913c0340137cc755f36',

  'src/third_party/googletest':
   Var('github_git') + '/google/googletest' + '@' + '054a986a8513149e8374fc669a5fe40117ca6b41',

  'src/third_party/boringssl':
   Var('github_git') + '/dart-lang/boringssl_gen.git' + '@' + Var('dart_boringssl_gen_rev'),

  'src/third_party/yapf':
  Var('github_git') + '/google/yapf' + '@' + '212c5b5ad8e172d2d914ae454c121c89cccbcb35',

  'src/third_party/boringssl/src':
   'https://boringssl.googlesource.com/boringssl.git' + '@' + Var('dart_boringssl_rev'),

  'src/third_party/perfetto':
   Var('fuchsia_git') + "/third_party/android.googlesource.com/platform/external/perfetto"
   + '@' + Var('dart_perfetto_rev'),

  'src/third_party/protobuf':
   Var('fuchsia_git') + '/third_party/protobuf' + '@' + Var('dart_libprotobuf_rev'),

  'src/build/secondary/third_party/protobuf':
   Var('fuchsia_git') + '/protobuf-gn' + '@' + Var('dart_protobuf_gn_rev'),

  'src/third_party/dart':
   Var('dart_git') + '/sdk.git' + '@' + Var('dart_revision'),

  # WARNING: Unused Dart dependencies in the list below till "WARNING:" marker are removed automatically - see create_updated_flutter_deps.py.

  'src/third_party/dart/third_party/binaryen/src':
   Var('chromium_git') + '/external/github.com/WebAssembly/binaryen.git@4471b81a0a0b94c75bad6e81d0413860944ecb1f',

  'src/third_party/dart/third_party/devtools':
   {'packages': [{'version': 'git_revision:c7a81f64dabb4b9f2cae0cf2c9411ef8bb805191', 'package': 'dart/third_party/flutter/devtools'}], 'dep_type': 'cipd'},

  'src/third_party/dart/third_party/pkg/args':
   Var('dart_git') + '/args.git@a23ea85cfd5c467c8671aef2ef9dfe45759ff974',

  'src/third_party/dart/third_party/pkg/async':
   Var('dart_git') + '/async.git@c9cc576e1f4d477047f737cace79ed6b72c70350',

  'src/third_party/dart/third_party/pkg/bazel_worker':
   Var('dart_git') + '/bazel_worker.git@b35c25e6cecced319b80c6686b9d025e462c7053',

  'src/third_party/dart/third_party/pkg/boolean_selector':
   Var('dart_git') + '/boolean_selector.git@ba7d86b66382aa808576cd55840d4c34f0225066',

  'src/third_party/dart/third_party/pkg/browser_launcher':
   Var('dart_git') + '/browser_launcher.git' + '@' + Var('dart_browser_launcher_rev'),

  'src/third_party/dart/third_party/pkg/cli_util':
   Var('dart_git') + '/cli_util.git@32bc0779a604c1bde1bb0782789c99cac222e651',

  'src/third_party/dart/third_party/pkg/clock':
   Var('dart_git') + '/clock.git' + '@' + Var('dart_clock_rev'),

  'src/third_party/dart/third_party/pkg/collection':
   Var('dart_git') + '/collection.git' + '@' + Var('dart_collection_rev'),

  'src/third_party/dart/third_party/pkg/convert':
   Var('dart_git') + '/convert.git@20d136c2fa4edc229fc3d7684bbeb8df5105580b',

  'src/third_party/dart/third_party/pkg/crypto':
   Var('dart_git') + '/crypto.git@f854f2fa730acb107aa41ebe431403081f7161e4',

  'src/third_party/dart/third_party/pkg/csslib':
   Var('dart_git') + '/csslib.git@7054945b62bd83c4c7a0fab693fa73c3f137c202',

  'src/third_party/dart/third_party/pkg/dart_style':
   Var('dart_git') + '/dart_style.git@d0c6b1da52c9f80679a7aaa05e5935ef5c6bb52f',

  'src/third_party/dart/third_party/pkg/dartdoc':
   Var('dart_git') + '/dartdoc.git@99df16a0d08c6a6323ebf66d1cada63c7a4de0ba',

  'src/third_party/dart/third_party/pkg/ffi':
   Var('dart_git') + '/ffi.git@2a56c2a9a87122c057168874bde384debbb806b0',

  'src/third_party/dart/third_party/pkg/file':
   Var('dart_git') + '/external/github.com/google/file.dart@b768f79dcd104a5feabafab47101c4355b71cd8f',

  'src/third_party/dart/third_party/pkg/fixnum':
   Var('dart_git') + '/fixnum.git@71f0d4d16054e6be7d8e22bdb3b082b9f82061be',

  'src/third_party/dart/third_party/pkg/glob':
   Var('dart_git') + '/glob.git@4579281741e59e2e4ad02a197e0b1f4d6558dede',

  'src/third_party/dart/third_party/pkg/html':
   Var('dart_git') + '/html.git@3dd00b0ca99e222697e6b6dc653774dc877da420',

  'src/third_party/dart/third_party/pkg/http':
   Var('dart_git') + '/http.git@092bb2d5ed1d522c55ef6781a469ba1e53cee2a8',

  'src/third_party/dart/third_party/pkg/http_multi_server':
   Var('dart_git') + '/http_multi_server.git@cce50802b66d33f703f82b3189988aa8e51976ac',

  'src/third_party/dart/third_party/pkg/http_parser':
   Var('dart_git') + '/http_parser.git@6f73e4a399df013ded8f4c81f151d122b36d361b',

  'src/third_party/dart/third_party/pkg/intl':
   Var('dart_git') + '/intl.git@946c34c155073c0c7dbbc6ce06f5d0c35570019d',

  'src/third_party/dart/third_party/pkg/json_rpc_2':
   Var('dart_git') + '/json_rpc_2.git@bd9f8d90ec9ce9d0da5c11f3e71b87af3aaca3b4',

  'src/third_party/dart/third_party/pkg/linter':
   Var('dart_git') + '/linter.git@8f7b75f8a3501ca2c4d5bbc1f003d90d66447544',

  'src/third_party/dart/third_party/pkg/logging':
   Var('dart_git') + '/logging.git@34ed68fe23291c82bb685984e4e2ffc06860a4a8',

  'src/third_party/dart/third_party/pkg/markdown':
   Var('dart_git') + '/markdown.git@ee3f4e976efcfed87c6ec78364bc2dd3c6e717b9',

  'src/third_party/dart/third_party/pkg/matcher':
   Var('dart_git') + '/matcher.git@deedda179c33b00b3e06aa107ebfc3dd2f8a5f49',

  'src/third_party/dart/third_party/pkg/mime':
   Var('dart_git') + '/mime.git@034471a60d5603a6988de6d9811bee1cb0657f70',

  'src/third_party/dart/third_party/pkg/mockito':
   Var('dart_git') + '/mockito.git@76965577aac7c82307a82cb5a12e78cfcc3f1f9d',

  'src/third_party/dart/third_party/pkg/package_config':
   Var('dart_git') + '/package_config.git@2e1a8eca1ebeac01f45003642c25e24e63d45b50',

  'src/third_party/dart/third_party/pkg/path':
   Var('dart_git') + '/path.git@9768908ef81cf92fc77cb259c2cf01ca8725de88',

  'src/third_party/dart/third_party/pkg/pool':
   Var('dart_git') + '/pool.git@ad4e2a7fde6a2937b2f7f59af271b437376d8e3d',

  'src/third_party/dart/third_party/pkg/protobuf':
   Var('dart_git') + '/protobuf.git' + '@' + Var('dart_protobuf_rev'),

  'src/third_party/dart/third_party/pkg/pub':
   Var('dart_git') + '/pub.git' + '@' + Var('dart_pub_rev'),

  'src/third_party/dart/third_party/pkg/pub_semver':
   Var('dart_git') + '/pub_semver.git@3946e33446365aa6af84abc0b1f47ad3a6f3b490',

  'src/third_party/dart/third_party/pkg/shelf':
   Var('dart_git') + '/shelf.git@a44e95e00324b6051bbee5ea235355f843795d1c',

  'src/third_party/dart/third_party/pkg/source_map_stack_trace':
   Var('dart_git') + '/source_map_stack_trace.git@adea3e51269f355514b59b66a4fcecabd1fa6e95',

  'src/third_party/dart/third_party/pkg/source_maps':
   Var('dart_git') + '/source_maps.git@d995912983f4f4c33a040c629952fb4632aeea70',

  'src/third_party/dart/third_party/pkg/source_span':
   Var('dart_git') + '/source_span.git@72d5c55e455c3940c37fe768730f5922e7a1f309',

  'src/third_party/dart/third_party/pkg/sse':
   Var('dart_git') + '/sse.git@4e63b08cbe4974c834e43e30c52af632ad147cea',

  'src/third_party/dart/third_party/pkg/stack_trace':
   Var('dart_git') + '/stack_trace.git@c08ee90b83380381a893d1e77a9a533d632f40e0',

  'src/third_party/dart/third_party/pkg/stream_channel':
   Var('dart_git') + '/stream_channel.git@3b9926876dc06970b583c34d0cb359ef976c4350',

  'src/third_party/dart/third_party/pkg/string_scanner':
   Var('dart_git') + '/string_scanner.git@045498024df8f0a1cd0f717f12d60aec77d3d8ae',

  'src/third_party/dart/third_party/pkg/term_glyph':
   Var('dart_git') + '/term_glyph.git@8cd931827bc3bfc1c62fd7ea44cbbc99b8a94f4d',

  'src/third_party/dart/third_party/pkg/test':
   Var('dart_git') + '/test.git@53df5270dbf0c35543f83035300d10d9fcc2f4cf',

  'src/third_party/dart/third_party/pkg/test_reflective_loader':
   Var('dart_git') + '/test_reflective_loader.git@cf58259b91c4d3cccc90abd4c0b44273e6421646',

  'src/third_party/dart/third_party/pkg/typed_data':
   Var('dart_git') + '/typed_data.git@9c209b9c99ca7528a45c23d5d09579788b3ea81b',

  'src/third_party/dart/third_party/pkg/usage':
   Var('dart_git') + '/usage.git@2773c7d334db9a902582feb8c5f38899c83d7b54',

  'src/third_party/dart/third_party/pkg/watcher':
   Var('dart_git') + '/watcher.git' + '@' + Var('dart_watcher_rev'),

  'src/third_party/dart/third_party/pkg/web_socket_channel':
   Var('dart_git') + '/web_socket_channel.git@28d7b82986cf931e6d977d973a7849cfc7c0bab9',

  'src/third_party/dart/third_party/pkg/webdev':
   Var('dart_git') + '/webdev.git' + '@' + Var('dart_webdev_rev'),

  'src/third_party/dart/third_party/pkg/webkit_inspection_protocol':
   Var('dart_git') + '/external/github.com/google/webkit_inspection_protocol.dart.git' + '@' + Var('dart_webkit_inspection_protocol_rev'),

  'src/third_party/dart/third_party/pkg/yaml':
   Var('dart_git') + '/yaml.git@b2fce6cb8f07f091967b849d5434ed495cbb305f',

  'src/third_party/dart/third_party/pkg/yaml_edit':
   Var('dart_git') + '/yaml_edit.git' + '@' + Var('dart_yaml_edit_rev'),

  'src/third_party/dart/tools/sdks':
   {'packages': [{'version': 'version:2.19.0', 'package': 'dart/dart-sdk/${{platform}}'}], 'dep_type': 'cipd'},

  # WARNING: end of dart dependencies list that is cleaned up automatically - see create_updated_flutter_deps.py.

  # Prebuilt Dart SDK of the same revision as the Dart SDK source checkout
  'src/flutter/prebuilts/linux-x64/dart-sdk': {
    'packages': [
      {
        'package': 'flutter/dart-sdk/linux-amd64',
        'version': 'git_revision:'+Var('dart_revision')
      }
    ],
    'dep_type': 'cipd',
    'condition': 'host_os == "linux" and download_dart_sdk'
  },
  'src/flutter/prebuilts/linux-arm64/dart-sdk': {
    'packages': [
      {
        'package': 'flutter/dart-sdk/linux-arm64',
        'version': 'git_revision:'+Var('dart_revision')
      }
    ],
    'dep_type': 'cipd',
    'condition': 'host_os == "linux" and download_dart_sdk'
  },
  'src/flutter/prebuilts/macos-x64/dart-sdk': {
    'packages': [
      {
        'package': 'flutter/dart-sdk/mac-amd64',
        'version': 'git_revision:'+Var('dart_revision')
      }
    ],
    'dep_type': 'cipd',
    'condition': 'host_os == "mac" and download_dart_sdk'
  },
  'src/flutter/prebuilts/macos-arm64/dart-sdk': {
    'packages': [
      {
        'package': 'flutter/dart-sdk/mac-arm64',
        'version': 'git_revision:'+Var('dart_revision')
      }
    ],
    'dep_type': 'cipd',
    'condition': 'host_os == "mac" and download_dart_sdk'
  },
  'src/flutter/prebuilts/windows-x64/dart-sdk': {
    'packages': [
      {
        'package': 'flutter/dart-sdk/windows-amd64',
        'version': 'git_revision:'+Var('dart_revision')
      }
    ],
    'dep_type': 'cipd',
    'condition': 'host_os == "win" and download_dart_sdk'
  },
  'src/flutter/prebuilts/windows-arm64/dart-sdk': {
    'packages': [
      {
        'package': 'flutter/dart-sdk/windows-arm64',
        'version': 'git_revision:'+Var('dart_revision')
      }
    ],
    'dep_type': 'cipd',
    'condition': 'host_os == "win" and download_dart_sdk and not release_candidate'
  },

  'src/third_party/colorama/src':
   Var('chromium_git') + '/external/colorama.git' + '@' + '799604a1041e9b3bc5d2789ecbd7e8db2e18e6b8',

  'src/third_party/expat':
   Var('chromium_git') + '/external/github.com/libexpat/libexpat.git' + '@' + '654d2de0da85662fcc7644a7acd7c2dd2cfb21f0',

  'src/third_party/freetype2':
   Var('flutter_git') + '/third_party/freetype2' + '@' + '3bea2761290a1cbe7d8f75c1c5a7ad727f826a66',

  'src/third_party/root_certificates':
   Var('dart_git') + '/root_certificates.git' + '@' + Var('dart_root_certificates_rev'),

  'src/third_party/skia':
   Var('skia_git') + '/skia.git' + '@' +  Var('skia_revision'),

  'src/third_party/ocmock':
   Var('ocmock_git') + '@' +  Var('ocmock_rev'),

  'src/third_party/libjpeg-turbo':
   Var('fuchsia_git') + '/third_party/libjpeg-turbo' + '@' + '0fb821f3b2e570b2783a94ccd9a2fb1f4916ae9f',

  'src/third_party/libpng':
   Var('flutter_git') + '/third_party/libpng' + '@' + '9187b6e12756317f6d44fc669ac11dfc262bd192',

  'src/third_party/libwebp':
   Var('chromium_git') + '/webm/libwebp.git' + '@' + '7dfde712a477e420968732161539011e0fd446cf', # 1.2.0

  'src/third_party/wuffs':
   Var('skia_git') + '/external/github.com/google/wuffs-mirror-release-c.git' + '@' + '600cd96cf47788ee3a74b40a6028b035c9fd6a61',

  'src/third_party/fontconfig/src':
   Var('chromium_git') + '/external/fontconfig.git' + '@' + 'c336b8471877371f0190ba06f7547c54e2b890ba',

  'src/third_party/fontconfig':
   Var('flutter_git') + '/third_party/fontconfig' + '@' + '81c83d510ae3aa75589435ce32a5de05139aacb0',

  'src/third_party/libxml':
   Var('flutter_git') + '/third_party/libxml' + '@' + 'a143e452b5fc7d872813eeadc8db421694058098',

  'src/third_party/zlib':
   Var('chromium_git') + '/chromium/src/third_party/zlib.git' + '@' + Var('dart_zlib_rev'),

  'src/third_party/inja':
   Var('flutter_git') + '/third_party/inja' + '@' + '88bd6112575a80d004e551c98cf956f88ff4d445',

  'src/third_party/libtess2':
   Var('flutter_git') + '/third_party/libtess2' + '@' + '725e5e08ec8751477565f1d603fd7eb9058c277c',

  'src/third_party/sqlite':
   Var('flutter_git') + '/third_party/sqlite' + '@' + '0f61bd2023ba94423b4e4c8cfb1a23de1fe6a21c',

  'src/third_party/pyyaml':
   Var('fuchsia_git') + '/third_party/pyyaml.git' + '@' + '25e97546488eee166b1abb229a27856cecd8b7ac',

   # Upstream Khronos Vulkan Headers are part of vulkan-deps
   # Downstream Fuchsia Vulkan Headers (v1.2.198)
  'src/third_party/fuchsia-vulkan':
   Var('fuchsia_git') + '/third_party/Vulkan-Headers.git' + '@' + '32640ad82ef648768c706c9bf828b77123a09bc2',

   'src/third_party/swiftshader':
   Var('swiftshader_git') + '/SwiftShader.git' + '@' + '5f9ed9b16931c7155171d31f75004f73f0a3abc8',

   'src/third_party/angle':
   Var('chromium_git') + '/angle/angle.git' + '@' + '32175d8a6dc185dd850e5c9988f208085c9c0d80',

   'src/third_party/vulkan_memory_allocator':
   Var('chromium_git') + '/external/github.com/GPUOpen-LibrariesAndSDKs/VulkanMemoryAllocator' + '@' + '7de5cc00de50e71a3aab22dea52fbb7ff4efceb6',

   'src/third_party/abseil-cpp':
   Var('flutter_git') + '/third_party/abseil-cpp.git' + '@' + '61833f2c057a2b1993d871e8c51156aed1dd4354',

   # Dart packages
  'src/third_party/pkg/archive':
  Var('github_git') + '/brendan-duncan/archive.git' + '@' + '9de7a0544457c6aba755ccb65abb41b0dc1db70d', # 3.1.2

  'src/third_party/pkg/equatable':
  Var('github_git') + '/felangel/equatable.git' + '@' + '0ba67c72db8bed75877fc1caafa74112ee0bd921', # 2.0.2

  'src/third_party/pkg/file':
  Var('dart_git') + '/external/github.com/google/file.dart.git' + '@' + 'b2e31cb6ef40b223701dbfa0b907fe58468484d7', # 6.1.4

  'src/third_party/pkg/flutter_packages':
  Var('github_git') + '/flutter/packages.git' + '@' + '25454e63851fe7933f04d025606e68c1eac4fe0f', # various

  'src/third_party/pkg/gcloud':
  Var('github_git') + '/dart-lang/gcloud.git' + '@' + 'a5276b85c4714378e84b1fb478b8feeeb686ac26', # 0.8.6-dev

  'src/third_party/pkg/googleapis':
  Var('github_git') + '/google/googleapis.dart.git' + '@' + '526011f56d98eab183cc6075ee1392e8303e43e2', # various

  'src/third_party/pkg/platform':
  Var('github_git') + '/google/platform.dart.git' + '@' + '1ffad63428bbd1b3ecaa15926bacfb724023648c', # 3.1.0

  'src/third_party/pkg/process':
  Var('github_git') + '/google/process.dart.git' + '@' + '0c9aeac86dcc4e3a6cf760b76fed507107e244d5', # 4.2.1

  'src/third_party/pkg/process_runner':
  Var('github_git') + '/google/process_runner.git' + '@' + 'd632ea0bfd814d779fcc53a361ed33eaf3620a0b', # 4.0.1

  'src/third_party/pkg/quiver':
  Var('github_git') + '/google/quiver-dart.git' + '@' + '90b92bee895e507d435012356a8b5c5f17eafa52', # 3.2.1

  'src/third_party/pkg/vector_math':
  Var('dart_git') + '/external/github.com/google/vector_math.dart.git' + '@' + '0a5fd95449083d404df9768bc1b321b88a7d2eef', # 2.1.0

  'src/third_party/imgui':
  Var('github_git') + '/ocornut/imgui.git' + '@' + '3ea0fad204e994d669f79ed29dcaf61cd5cb571d',

  'src/third_party/tinygltf':
  Var('github_git') + '/syoyo/tinygltf.git' + '@' + '9bb5806df4055ac973b970ba5b3e27ce27d98148',

  'src/third_party/json':
  Var('github_git') + '/nlohmann/json.git' + '@' + '17d9eacd248f58b73f4d1be518ef649fe2295642',

  'src/third_party/gradle': {
    'packages': [
      {
        'version': 'version:7.0.2',
        'package': 'flutter/gradle'
      }
    ],
    'condition': 'download_android_deps',
    'dep_type': 'cipd'
  },

  'src/third_party/android_tools/trace_to_text': {
    'packages': [
      {
        # 25.0 downloads for both mac-amd64 and mac-arm64
        # 26.1 is not found with either platform
        # 27.1 is the latest release of perfetto
        'version': 'git_tag:v25.0',
        'package': 'perfetto/trace_to_text/${{platform}}'
      }
    ],
    'condition': 'download_android_deps',
    'dep_type': 'cipd'
  },

   'src/third_party/android_tools/google-java-format': {
     'packages': [
       {
        'package': 'flutter/android/google-java-format',
        'version': 'version:1.7-1'
       }
     ],
     # We want to be able to format these as part of CI, and the CI step that
     # checks formatting runs without downloading the rest of the Android build
     # tooling. Therefore unlike all the other Android-related tools, we want to
     # download this every time.
     'dep_type': 'cipd',
   },

  'src/third_party/android_tools': {
     'packages': [
       {
        'package': 'flutter/android/sdk/all/${{platform}}',
        'version': 'version:33v6'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/android_embedding_dependencies': {
     'packages': [
       {
        'package': 'flutter/android/embedding_bundle',
        'version': 'last_updated:2021-11-23T12:31:07-0800'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/third_party/web_dependencies': {
     'packages': [
       {
         'package': 'flutter/web/canvaskit_bundle',
         'version': Var('canvaskit_cipd_instance')
       }
     ],
     'dep_type': 'cipd',
   },

  'src/third_party/java/openjdk': {
     'packages': [
       {
        'package': 'flutter/java/openjdk/${{platform}}',
        'version': 'version:11'
       }
     ],
     'condition': 'download_android_deps',
     'dep_type': 'cipd',
   },

  'src/flutter/third_party/gn': {
    'packages': [
      {
        'package': 'gn/gn/${{platform}}',
        'version': 'git_revision:b79031308cc878488202beb99883ec1f2efd9a6d'
      },
    ],
    'dep_type': 'cipd',
  },
  'src/flutter/third_party/ninja': {
    'packages': [
      {
        'package': 'infra/3pp/tools/ninja/${{platform}}',
        'version': 'version:2@1.8.2.chromium.3',
      }
    ],
    'dep_type': 'cipd',
  },

  'src/buildtools/emsdk': {
   'url': Var('skia_git') + '/external/github.com/emscripten-core/emsdk.git' + '@' + 'fc645b7626ebf86530dbd82fbece74d457e7ae07',
   'condition': 'download_emsdk',
  },

  # Clang on mac and linux are expected to typically be the same revision.
  # They are separated out so that the autoroller can more easily manage them.
  'src/buildtools/mac-x64/clang': {
    'packages': [
      {
        'package': 'fuchsia/third_party/clang/mac-amd64',
        'version': Var('clang_version'),
      }
    ],
    'condition': 'host_os == "mac"', # On ARM64 Macs too because Goma doesn't support the host-arm64 toolchain.
    'dep_type': 'cipd',
  },

  'src/buildtools/mac-arm64/clang': {
    'packages': [
      {
        'package': 'fuchsia/third_party/clang/mac-arm64',
        'version': Var('clang_version'),
      }
    ],
    'condition': 'host_os == "mac" and host_cpu == "arm64"',
    'dep_type': 'cipd',
  },

  'src/buildtools/linux-x64/clang': {
    'packages': [
      {
        'package': 'fuchsia/third_party/clang/linux-amd64',
        'version': Var('clang_version'),
      }
    ],
    'condition': 'host_os == "linux" and host_cpu == "x64"',
    'dep_type': 'cipd',
  },

  'src/buildtools/linux-arm64/clang': {
    'packages': [
      {
        'package': 'fuchsia/third_party/clang/linux-arm64',
        'version': Var('clang_version'),
      }
    ],
    'condition': 'host_os == "linux" and host_cpu == "arm64"',
    'dep_type': 'cipd',
  },

  'src/buildtools/windows-x64/clang': {
    'packages': [
      {
        'package': 'fuchsia/third_party/clang/windows-amd64',
        'version': Var('clang_version'),
      }
    ],
    'condition': 'download_windows_deps',
    'dep_type': 'cipd',
  },

   # Get the SDK from https://chrome-infra-packages.appspot.com/p/fuchsia/sdk/core at the 'latest' tag
   # Get the toolchain from https://chrome-infra-packages.appspot.com/p/fuchsia/clang at the 'goma' tag

   'src/fuchsia/sdk/mac': {
     'packages': [
       {
        'package': 'fuchsia/sdk/core/mac-amd64',
        'version': '11wOrGFBXTHgxQVOiDlM2QZI8AFL0idY8lOPNYDs7wMC'
       }
     ],
     'condition': 'host_os == "mac" and not download_fuchsia_sdk',
     'dep_type': 'cipd',
   },
   'src/fuchsia/sdk/linux': {
     'packages': [
       {
        'package': 'fuchsia/sdk/core/linux-amd64',
        'version': '6c2H32X3EXOGlWIgb8HSZpQ-bcF7Msec3q2uC-WUB7UC'
       }
     ],
     'condition': 'host_os == "linux" and not download_fuchsia_sdk',
     'dep_type': 'cipd',
   },
}

recursedeps = [
  'src/third_party/vulkan-deps',
]

hooks = [
  {
    # Generate the Dart SDK's .dart_tool/package_confg.json file.
    'name': 'Generate .dart_tool/package_confg.json',
    'pattern': '.',
    'action': ['python3', 'src/third_party/dart/tools/generate_package_config.py'],
  },
  {
    # Generate the sdk/version file.
    'name': 'Generate sdk/version',
    'pattern': '.',
    'action': ['python3', 'src/third_party/dart/tools/generate_sdk_version_file.py'],
  },
  {
    # Update the Windows toolchain if necessary.
    'name': 'win_toolchain',
    'condition': 'download_windows_deps',
    'pattern': '.',
    'action': ['python3', 'src/build/vs_toolchain.py', 'update'],
  },
  {
    # Ensure that we don't accidentally reference any .pyc files whose
    # corresponding .py files have already been deleted.
    'name': 'remove_stale_pyc_files',
    'pattern': 'src/tools/.*\\.py',
    'action': [
        'python3',
        'src/tools/remove_stale_pyc_files.py',
        'src/tools',
    ],
  },
  {
    'name': 'dia_dll',
    'pattern': '.',
    'condition': 'download_windows_deps',
    'action': [
      'python3',
      'src/flutter/tools/dia_dll.py',
    ],
  },
  {
    'name': 'linux_sysroot_x64',
    'pattern': '.',
    'condition': 'download_linux_deps',
    'action': [
      'python3',
      'src/build/linux/sysroot_scripts/install-sysroot.py',
      '--arch=x64'],
  },
  {
    'name': 'linux_sysroot_arm64',
    'pattern': '.',
    'condition': 'download_linux_deps',
    'action': [
      'python3',
      'src/build/linux/sysroot_scripts/install-sysroot.py',
      '--arch=arm64'],
  },
  {
    'name': 'pub get --offline',
    'pattern': '.',
    'action': [
      'python3',
      'src/flutter/tools/pub_get_offline.py',
    ]
  },
  {
    'name': 'Download Fuchsia SDK',
    'pattern': '.',
    'condition': 'download_fuchsia_sdk',
    'action': [
      'python3',
      'src/flutter/tools/download_fuchsia_sdk.py',
      '--fail-loudly',
      '--verbose',
      '--host-os',
      Var('host_os'),
      '--fuchsia-sdk-path',
      Var('fuchsia_sdk_path'),
    ]
  },
  {
    'name': 'Activate Emscripten SDK',
    'pattern': '.',
    'condition': 'download_emsdk',
    'action': [
      'python3',
      'src/flutter/tools/activate_emsdk.py',
    ]
  },
  {
    'name': 'Setup githooks',
    'pattern': '.',
    'condition': 'setup_githooks',
    'action': [
      'python3',
      'src/flutter/tools/githooks/setup.py',
    ]
  }
]
