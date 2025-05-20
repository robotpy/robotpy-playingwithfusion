project('robotpy-playingwithfusion', ['cpp'],
        default_options: ['warning_level=1', 'cpp_std=c++20',
                          'b_colorout=auto', 'optimization=2', 'b_pie=true'])

subdir('semiwrap')

playingwithfusion_sources += files(
    'playingwithfusion/pwf.cpp',
)

#
# Static link
#

cpp = meson.get_compiler('cpp')
libs_path = meson.current_source_dir() + '/lib/lib'

playingwithfusion_deps += [
    cpp.find_library('PlayingWithFusionDriver', dirs: libs_path),
    cpp.find_library('PlayingWithFusion', dirs: libs_path),
]

subdir('semiwrap/modules')
