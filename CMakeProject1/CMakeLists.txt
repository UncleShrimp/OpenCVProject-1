# CMakeList.txt : CMake project for CMakeProject1, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)
# Add source to this project's executable.
add_executable (CMakeProject1 "CMakeProject1.cpp" "CMakeProject1.h")

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET CMakeProject1 PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed. #
include_directories(${OpenCV_INCLUDE_DIRS})
SET("OpenCV_DIR" "C:/libs/opencv/build")
find_package(OpenCV REQUIRED)
find_library(PATH ${OpenCV_DIR}) # C:\libs\opencv\build\x64\vc16\lib
SET("OpenCV_LIB" "C:/libs/opencv/build/x64/vc16/lib")
find_library(PATH ${OpenCV_LIB})
target_link_libraries(CMakeProject1 ${OpenCV_LIBS})



#Severity	Code	Description	Project	File	Line	Suppression State
#Error		CMake Error: Error: generator : Ninja
#Does not match the generator used previously: MinGW Makefiles
#Either remove the CMakeCache.txt file and CMakeFiles directory or choose a different binary directory.
#'C:\Windows\system32\cmd.exe' '/c "%SYSTEMROOT%\System32\chcp.com 65001 >NUL && "C:\PROGRAM FILES\MICROSOFT VISUAL STUDIO\2022\COMMUNITY\COMMON7\IDE\COMMONEXTENSIONS\MICROSOFT\CMAKE\CMake\bin\cmake.exe"  -G "Ninja"  -DCMAKE_C_COMPILER:STRING="cl.exe" -DCMAKE_CXX_COMPILER:STRING="cl.exe" -DCMAKE_BUILD_TYPE:STRING="Debug" -DCMAKE_INSTALL_PREFIX:PATH="C:/Users/danaa/Downloads/CMakeOpenCVProject1/out/install/x64-debug"  -DCMAKE_MAKE_PROGRAM="C:\PROGRAM FILES\MICROSOFT VISUAL STUDIO\2022\COMMUNITY\COMMON7\IDE\COMMONEXTENSIONS\MICROSOFT\CMAKE\Ninja\ninja.exe" "C:\Users\danaa\Downloads\CMakeOpenCVProject1" 2>&1"' execution failed with error: ''C:\Windows\system32\cmd.exe' '/c "%SYSTEMROOT%\System32\chcp.com 65001 >NUL && "C:\PROGRAM FILES\MICROSOFT VISUAL STUDIO\2022\COMMUNITY\COMMON7\IDE\COMMONEXTENSIONS\MICROSOFT\CMAKE\CMake\bin\cmake.exe"  -G "Ninja"  -DCMAKE_C_COMPILER:STRING="cl.exe" -DCMAKE_CXX_COMPILER:STRING="cl.exe" -DCMAKE_BUILD_TYPE:STRING="Debug" -DCMAKE_INSTALL_PREFIX:PATH="C:/Users/danaa/Downloads/CMakeOpenCVProject1/out/install/x64-debug"  -DCMAKE_MAKE_PROGRAM="C:\PROGRAM FILES\MICROSOFT VISUAL STUDIO\2022\COMMUNITY\COMMON7\IDE\COMMONEXTENSIONS\MICROSOFT\CMAKE\Ninja\ninja.exe" "C:\Users\danaa\Downloads\CMakeOpenCVProject1" 2>&1"' returned with exit code: 1'.		C:\Users\danaa\Downloads\CMakeOpenCVProject1\'C		
