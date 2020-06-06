compile_args = []

spirvcross_src = files([
    'spirv_cfg.cpp',
    'spirv_cpp.cpp',
    'spirv_cross.cpp',
    'spirv_cross_c.cpp',
    'spirv_cross_parsed_ir.cpp',
    'spirv_cross_util.cpp',
    'spirv_glsl.cpp',
    'spirv_hlsl.cpp',
    'spirv_msl.cpp',
    'spirv_parser.cpp',
    'spirv_reflect.cpp',
])

spirvcross_inc = [
  './',
  './include',
]

spirvcross_dep_list = [

]

spirvcross = static_library(
	'spirvcross',
	spirvcross_src,
	cpp_args            : compile_args,
	include_directories : spirvcross_inc,
	dependencies        : spirvcross_dep_list,
)

spirvcross_dep = declare_dependency(
  link_with           : spirvcross,
  include_directories : spirvcross_inc,
)