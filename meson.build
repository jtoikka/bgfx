project('bgfx', 'cpp', version : '1.0.0', license: 'BSD 2-Clause', default_options : ['cpp_std=c++14'])

includes = [
	'include',
	'3rdparty',
	'3rdparty/khronos',
	'3rdparty/fcpp',
	'3rdparty/glslang/glslang/Public',
	'3rdparty/glslang/glslang/Include',
	'3rdparty/glsl-optimizer/include',
	'3rdparty/glsl-optimizer/src/glsl',
]

src = ['src/amalgamated.cpp']

bx_dep = dependency('bx', fallback: ['bx', 'bx_dep'])
bimg_dep = dependency('bimg', fallback: ['bimg', 'bimg_dep'])

cpp_args = []
if host_machine.system() == 'darwin'
	appleframeworks_dep = dependency('appleframeworks', modules : ['Metal', 'QuartzCore', 'Cocoa'])
	cpp_args = ['-ObjC++']
else
endif

lib = static_library(
  'libbgfx',
  src,
  include_directories : includes,
  dependencies        : [bx_dep, bimg_dep],
	cpp_args     			  : cpp_args
	
)

bgfx_dep = declare_dependency(include_directories : includes, link_with: lib)