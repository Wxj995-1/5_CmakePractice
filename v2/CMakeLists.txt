cmake_minimum_required(VERSION 3.5)

project(test)

#指定c++版本
set(CMAKE_CXX_STANDARD 11)

#取别名 aux_source_directory() 或者 file()
#set(SRC add.cpp div.cpp main.cpp mult.cpp sub.cpp)


#搜索指定路径下面的文件 aux_source_directory() 或者 file()
#1
aux_source_directory(${PROJECT_SOURCE_DIR}/src SRC)
#2
#file(GLOB SRC ${PROJECT_SOURCE_DIR}/src/*.cpp)


#指定文件输出路径
#set(HOME /home/weng/Cmake/5_CmakePractice)
set(HOME ${PROJECT_SOURCE_DIR})

include_directories(${PROJECT_SOURCE_DIR}/include)

#指定生成目标文件的地址
set(EXECUTABLE_OUTPUT_PATH ${HOME}/ofile)
set(LIBRARY_OUTPUT_PATH ${HOME}/oso)

#生成执行文件
#add_executable(app ${SRC})

#生成动态链接库
#add_library(calc SHARED ${SRC})

#生成动态链接库
add_library(calc SHARED ${SRC})