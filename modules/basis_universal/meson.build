_module_basis_universal_srcs = files(run_command(GLOB, '*.cpp', check: true).stdout().split('\n'))
if not DEP_BASIS_UNIVERSAL.found()
    error('module basis_universal requires DEP_BASIS_UNIVERSAL')
endif

_lib_module_basis_universal = library('module_basis_universal', _module_basis_universal_srcs,
    dependencies: [godotcore_dep, DEP_BASIS_UNIVERSAL]
)

DEP_MODULE_BASIS_UNIVERSAL = declare_dependency(link_with: _lib_module_basis_universal)

MODULE_DEPENDENCIES += DEP_MODULE_BASIS_UNIVERSAL

MODULES_ENABLED += 'basis_universal'
