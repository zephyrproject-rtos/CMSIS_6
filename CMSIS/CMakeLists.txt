# SPDX-License-Identifier: Apache-2.0

function(add_subdirectory_ifdef feature_toggle source_dir)
  if(${${feature_toggle}})
    add_subdirectory(${source_dir} ${ARGN})
  endif()
endfunction()

add_subdirectory_ifdef(CONFIG_HAS_CMSIS_CORE_M Core)
