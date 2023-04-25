include(cmake/wsl.cmake)

if(WIN32)
    add_subdirectory(src/win32)
elseif(APPLE)
    add_subdirectory(src/osx)
elseif(LINUX)
    add_subdirectory(src/linux)
endif()

install(TARGETS acquire-core-platform)
