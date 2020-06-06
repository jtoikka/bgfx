includes = [
  'glslang', 
  'spirv-cross',
  'spirv-tools/include',
  'webgpu/include'
]

src = [
  'glslang/SPIRV/SPVRemapper.cpp',
  'glslang/SPIRV/doc.cpp',
  # 'webgpu/webgpu_cpp.cpp'
]

spirv_lib = static_library(
  'spirv',
  src,
  include_directories: includes
)

spirv_dep = declare_dependency(
  include_directories: includes,
  link_with: spirv_lib
)