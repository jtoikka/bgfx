src_fcpp = [
  'cpp1.c',
  'cpp2.c',
  'cpp3.c',
  'cpp4.c',
  'cpp5.c',
  'cpp6.c',
]

incl_fcpp = [
  '.'
]

deps = [
  
]

fcpp = static_library('fcpp',
  src_fcpp,
  include_directories : incl_fcpp,
  dependencies: deps,
)

fcpp_dep = declare_dependency(
  link_with           : fcpp,
  include_directories : incl_fcpp,
)