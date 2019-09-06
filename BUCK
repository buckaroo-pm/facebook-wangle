load('//:buckaroo_macros.bzl', 'buckaroo_deps')
load('//:subdir_glob.bzl', 'subdir_glob')

cxx_library(
  name = 'wangle',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('', 'wangle/**/*.h'),
  ], exclude = glob([
    'wangle/**/test/**/*.h',
  ])),
  srcs = glob([
    'wangle/**/*.cpp',
  ], exclude = glob([
    'wangle/example/**/*.cpp',
    'wangle/**/benchmarks/**/*.cpp',
    'wangle/**/exercises/**/*.cpp',
    'wangle/**/experimental/**/*.cpp',
    'wangle/**/examples/**/*.cpp',
    'wangle/**/test/**/*.cpp',
  ])),
  deps = buckaroo_deps(),
  visibility = [
    'PUBLIC',
  ],
)
