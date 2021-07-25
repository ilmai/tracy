project('tracy')

deps = []

if host_machine.system() != 'windows'
  deps += meson.get_compiler('cpp').find_library('dl')
endif

tracy_dep = declare_dependency(
    include_directories : include_directories('.'),
    sources : 'TracyClient.cpp',
    dependencies : deps
)

meson.override_dependency('tracy', tracy_dep)
