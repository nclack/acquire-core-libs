aq_require(acquire-core-logger)
aq_require(acquire-core-platform)
aq_require(acquire-device-properties)
aq_require(acquire-device-kit)
aq_require(acquire-device-hal)

set(tgt acquire-core-libs)
add_library(${tgt} INTERFACE)
target_link_libraries(${tgt} INTERFACE
        acquire-core-logger
        acquire-core-platform
        acquire-device-properties
        acquire-device-kit
        acquire-device-hal)
target_include_directories(${tgt} INTERFACE ${CMAKE_CURRENT_LIST_DIR})
