cmake_minimum_required(VERSION 3.0)

project(test)

#指定c++版本
set(CMAKE_CXX_STANDARD 11)

#取别名
set(SRC_LIST add.cpp div.cpp main.cpp mult.cpp sub.cpp)

#指定文件输出路径
set(HOME /home/weng/Cmake/5_CmakePractice)
set(EXECUTABLE_OUTPUT_PATH ${HOME}/ofile)
set(LIBRARY_OUTPUT_PATH ${HOME}/oso)


add_executable(app ${SRC_LIST})

