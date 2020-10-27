cmake_minimum_required(VERSION 3.17)
project(wx_template)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS -s)

set(wxWidgets_ROOT_DIR "D:\\msys64\\mingw64")
set(wxWidgets_LIB_DIR "D:\\msys64\\mingw64\\lib\\gcc_dll")
#set(wxWidgets_LIB_DIR "D:\\msys64\\mingw64\\lib\\gcc_lib")

set(wxWidgets_CONFIGURATION mswu)
find_package(wxWidgets COMPONENTS mono REQUIRED)
include(${wxWidgets_USE_FILE})

add_executable(
        wx_template WIN32
        mainwinodw.cpp res.rc)

target_link_libraries(wx_template ${wxWidgets_LIBRARIES})