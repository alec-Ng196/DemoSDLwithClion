cmake_minimum_required(VERSION 3.28)
project(Clion_SDL2)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake_modules/")


set(SDL2_PATH "D:/Duc codes again/SDL2-2.28.5/x86_64-w64-mingw32")
set(SDL2_IMAGE_PATH "D:/Duc codes again/SDL2_image-2.8.2/x86_64-w64-mingw32")
find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)
include_directories(${SDL2_INCLUDE_DIRS})
include_directories(${SDL2_IMAGE_INCLUDE_DIRS})

add_executable(Clion_SDL2 main.cpp)

target_link_libraries(${PROJECT_NAME} ${SDL2_LIBRARIES} ${SDL2_IMAGE_LIBRARIES} )