set(tgt acquire-core-logger)
add_library(${tgt} STATIC src/logger.h src/logger.c)
target_include_directories(${tgt} PUBLIC ../acquire-core-logger/src)
set_target_properties(${tgt} PROPERTIES
    MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>"
)
install(TARGETS ${tgt})