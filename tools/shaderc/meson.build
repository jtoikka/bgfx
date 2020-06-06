src = [
  'shaderc_glsl.cpp',
  'shaderc_hlsl.cpp',
  'shaderc_metal.cpp',
  'shaderc_pssl.cpp',
  'shaderc_spirv.cpp',
]

includes = [
  '.'
]

shaderc_lib = static_library(
  'shaderc',
  src,
  include_directories : includes,
  dependencies        : dependencies
)

shaderc_dep = declare_dependency(include_directories : includes, link_with: shaderc_lib, dependencies: dependencies)