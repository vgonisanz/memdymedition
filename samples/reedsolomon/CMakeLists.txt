file(GLOB ALL_FILES_CURRENT_PATH ${CMAKE_CURRENT_SOURCE_DIR}/* )

foreach(CURRENT_FILE ${ALL_FILES_CURRENT_PATH})
  if(IS_DIRECTORY ${CURRENT_FILE})
    message("Adding RS sample: ${CURRENT_FILE}")
    add_subdirectory( ${CURRENT_FILE} )
  endif()
endforeach()
