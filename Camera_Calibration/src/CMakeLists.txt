# 增加一个可执行的二进制
FIND_PACKAGE( OpenCV REQUIRED )
ADD_EXECUTABLE(calibration calibration.cpp )
# 增加opencv的依赖
INCLUDE_DIRECTORIES( ${OpenCV_INCLUDE_DIRS} )
TARGET_LINK_LIBRARIES( calibration ${OpenCV_LIBS})
# ————————————————

#                             版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
# 原文链接：https://blog.csdn.net/weixin_40107913/article/details/106606114