set(tgt acquire-device-kit)
add_library(${tgt} INTERFACE
        src/device/kit/driver.h
        src/device/kit/camera.h
        src/device/kit/experimental/signals.h
        src/device/kit/experimental/stage.axis.h
        src/device/kit/storage.h
)
target_link_libraries(${tgt} INTERFACE acquire-device-properties)
target_include_directories(${tgt} INTERFACE src)
