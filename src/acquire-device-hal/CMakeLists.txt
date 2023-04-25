set(tgt acquire-device-hal)
add_library(${tgt} STATIC
        src/device/hal/camera.h
        src/device/hal/camera.c
        src/device/hal/driver.h
        src/device/hal/driver.c
        src/device/hal/device.manager.h
        src/device/hal/device.manager.cpp
        src/device/hal/loader.h
        src/device/hal/loader.c
        src/device/hal/experimental/stage.axis.h
        src/device/hal/experimental/stage.axis.c
        src/device/hal/storage.h
        src/device/hal/storage.c
        )
target_sources(${tgt} PUBLIC FILE_SET HEADERS
        BASE_DIRS ${CMAKE_CURRENT_LIST_DIRS}
        FILES
        src/device/hal/device.manager.h
        )
target_link_libraries(${tgt} PRIVATE
        acquire-device-kit
        acquire-core-logger
        acquire-core-platform
        )
target_include_directories(${tgt} PUBLIC ${CMAKE_CURRENT_LIST_DIR}/src)
set_target_properties(${tgt} PROPERTIES
        MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>"
        )

install(TARGETS ${tgt} FILE_SET HEADERS)