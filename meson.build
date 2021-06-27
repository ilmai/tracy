project('tracy')

dl_dep = meson.get_compiler('cpp').find_library('dl')

tracy_dep = declare_dependency(
    include_directories : include_directories('.'),
    sources : 'TracyClient.cpp',
    dependencies : dl_dep
)

meson.override_dependency('tracy', tracy_dep)
