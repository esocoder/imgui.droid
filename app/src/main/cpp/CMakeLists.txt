cmake_minimum_required(VERSION 3.4.1)

project(esosand)

# build native_app_glue as a static lib
add_library(native_app_glue STATIC ${ANDROID_NDK}/sources/android/native_app_glue/android_native_app_glue.c)

# now build app's shared lib
add_library(
    native-plasma
    SHARED
    main.cpp
    imgui/imgui.cpp
    imgui/imgui_demo.cpp
    imgui/imgui_draw.cpp
    imgui/imgui_tables.cpp
    imgui/imgui_widgets.cpp
    imgui/backends/imgui_impl_android.cpp
    imgui/backends/imgui_impl_opengl3.cpp
)

target_include_directories(native-plasma PRIVATE
        ${ANDROID_NDK}/sources/android/native_app_glue
        imgui
        imgui/backends)

target_compile_definitions(native-plasma PRIVATE IMGUI_IMPL_OPENGL_ES3)

set(CMAKE_SHARED_LINKER_FLAGS "${CMAKE_SHARED_LINKER_FLAGS} -u ANativeActivity_onCreate")

# add lib dependencies
target_link_libraries(native-plasma
    android
    native_app_glue
    log
    EGL
    GLESv3)
