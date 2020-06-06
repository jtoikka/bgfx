glslang_src = files([
  './OGLCompilersDLL/InitializeDll.cpp',
  './SPIRV/GlslangToSpv.cpp',
  './SPIRV/InReadableOrder.cpp',
  './SPIRV/Logger.cpp',
  './SPIRV/SPVRemapper.cpp',
  './SPIRV/SpvBuilder.cpp',
  './SPIRV/SpvPostProcess.cpp',
  './SPIRV/SpvTools.cpp',
  './SPIRV/disassemble.cpp',
  './SPIRV/doc.cpp',
  './glslang/CInterface/glslang_c_interface.cpp',
  './glslang/GenericCodeGen/CodeGen.cpp',
  './glslang/GenericCodeGen/Link.cpp',
  './glslang/MachineIndependent/Constant.cpp',
  './glslang/MachineIndependent/InfoSink.cpp',
  './glslang/MachineIndependent/Initialize.cpp',
  './glslang/MachineIndependent/IntermTraverse.cpp',
  './glslang/MachineIndependent/Intermediate.cpp',
  './glslang/MachineIndependent/ParseContextBase.cpp',
  './glslang/MachineIndependent/ParseHelper.cpp',
  './glslang/MachineIndependent/PoolAlloc.cpp',
  './glslang/MachineIndependent/RemoveTree.cpp',
  './glslang/MachineIndependent/Scan.cpp',
  './glslang/MachineIndependent/ShaderLang.cpp',
  './glslang/MachineIndependent/SymbolTable.cpp',
  './glslang/MachineIndependent/Versions.cpp',
  './glslang/MachineIndependent/attribute.cpp',
  './glslang/MachineIndependent/glslang_tab.cpp',
  './glslang/MachineIndependent/intermOut.cpp',
  './glslang/MachineIndependent/iomapper.cpp',
  './glslang/MachineIndependent/limits.cpp',
  './glslang/MachineIndependent/linkValidate.cpp',
  './glslang/MachineIndependent/parseConst.cpp',
  './glslang/MachineIndependent/pch.cpp',
  './glslang/MachineIndependent/preprocessor/Pp.cpp',
  './glslang/MachineIndependent/preprocessor/PpAtom.cpp',
  './glslang/MachineIndependent/preprocessor/PpContext.cpp',
  './glslang/MachineIndependent/preprocessor/PpScanner.cpp',
  './glslang/MachineIndependent/preprocessor/PpTokens.cpp',
  './glslang/MachineIndependent/propagateNoContraction.cpp',
  './glslang/MachineIndependent/reflection.cpp',
  './glslang/OSDependent/Unix/ossource.cpp',
  './glslang/OSDependent/Web/glslang.js.cpp',
  './hlsl/hlslAttributes.cpp',
  './hlsl/hlslGrammar.cpp',
  './hlsl/hlslOpMap.cpp',
  './hlsl/hlslParseHelper.cpp',
  './hlsl/hlslParseables.cpp',
  './hlsl/hlslScanContext.cpp',
  './hlsl/hlslTokenStream.cpp',
  './hlsl/pch.cpp',
])

glslang_inc = [
  '.',
  './glslang',
  './glslang/Public',
  './glslang/Include',
  '../spirv-tools/include',
  '../spirv-tools/source',
]

glslang_dep_list = [

]

glslang = static_library(
	'glslang',
	glslang_src,
	cpp_args            : ['-DENABLE_OPT=1', '-DENABLE_HLSL=1'],
	include_directories : glslang_inc,
	dependencies        : glslang_dep_list,
)

glslang_dep = declare_dependency(
  link_with           : glslang,
  include_directories : glslang_inc,
)