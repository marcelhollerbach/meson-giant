project('meson-giant', 'c',
  version : '0.1',
  default_options : ['warning_level=3'])

dep_chain = []

lib_dirs = [
      'lib000',
      'lib001',
      'lib002',
      'lib003',
      'lib004',
      'lib005',
      'lib006',
      'lib007',
      'lib008',
      'lib009',
      'lib010',
      'lib011',
      'lib012',
      'lib013',
      'lib014',
      'lib015',
   ]

foreach directory : lib_dirs
   subdir(directory)
   dep_chain += lib
endforeach

foreach directory : lib_dirs
   exe = executable('tester_'+directory,
      'empty.c',
      dependencies: dep_chain,
   )
endforeach
