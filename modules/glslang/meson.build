_modules_glslang_srcs = files(run_command(GLOB, '*.cpp', check: true).stdout().split('\n'))
_lib_modules_glslang = library('modules_glslang',
                     _modules_glslang_srcs,
                     dependencies: [godotcore_dep, DEP_GLSLANG],
                     build_by_default:true)

DEP_MODULE_GLSLANG = declare_dependency(link_with: _lib_modules_glslang)

MODULE_DEPENDENCIES += [DEP_MODULE_GLSLANG]
MODULES_ENABLED += 'glslang'
