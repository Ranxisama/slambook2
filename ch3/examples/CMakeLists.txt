include_directories("/usr/include/eigen3")
add_executable(coordinateTransform coordinateTransform.cpp)

find_package(Pangolin REQUIRED)

## 1. 设置 Pangolin 的头文件路径
#set(Pangolin_INCLUDE_DIRS "/usr/local/include/pangolin")
#
## 设置 Pangolin 的库文件路径
#set(Pangolin_LIBRARIES "/usr/local/lib/libpangolin.so")

## 2. 设置Pangolin的路径
#set(PANGOLIN_INCLUDE_DIR ~/Documents/GitHub/slambook2/3rdparty/Pangolin/include)
#set(PANGOLIN_LIB_DIR ~/Documents/GitHub/slambook2/3rdparty/Pangolin/lib)
#
## 包含Pangolin的头文件
#include_directories(${PANGOLIN_INCLUDE_DIR})
#
## 链接Pangolin的库
#target_link_directories(${PANGOLIN_LIB_DIR})

include_directories(${Pangolin_INCLUDE_DIRS})
add_executable(plotTrajectory plotTrajectory.cpp)
target_link_libraries(plotTrajectory ${Pangolin_LIBRARIES})



