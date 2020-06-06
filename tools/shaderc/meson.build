src = [
  'shaderc_glsl.cpp',
  'shaderc_hlsl.cpp',
  'shaderc_metal.cpp',
  'shaderc_pssl.cpp',
  'shaderc_spirv.cpp',
  'shaderc.cpp',
  '../../src/vertexlayout.cpp',
	'../../src/shader_spirv.cpp',
]

includes = [
  '../../include'
]

dependencies = [ 
  bx_dep,
  bimg_dep, 
  glslang_dep, 
  glsloptimizer_dep, 
  spirvcross_dep, 
  spirvtools_dep,
  webgpu_dep,
  fcpp_dep
]

if host_machine.system() == 'darwin'
	appleframeworks_dep = dependency('appleframeworks', modules : ['Metal', 'QuartzCore', 'Cocoa'])
	dependencies += appleframeworks_dep
endif

shaderc_exe = executable(
  'shaderc',
  src,
  include_directories: includes,
  dependencies: dependencies
)