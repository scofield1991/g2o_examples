CMAKE_MINIMUM_REQUIRED( VERSION 2.8 ) #设定版本
PROJECT( g2o_exampels ) #设定工程名
SET( CMAKE_CXX_COMPILER "g++") #设定编译器
#SET( CMAKE_BUILD_TYPE Debug  )
SET( CMAKE_BUILD_TYPE Release )
#允许C++11标准、O3优化、多线程
set( CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -march=native -O3 -pthread" )	
#设定可执行二进制文件的目录
SET( EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin) 
	
#设定存放编译出来的库文件的目录
SET( LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib) 
#并且把该目录设为连接目录
LINK_DIRECTORIES( ${PROJECT_SOURCE_DIR}/lib)
	
#设定头文件目录
INCLUDE_DIRECTORIES( ${PROJECT_SOURCE_DIR}/include)
	
#增加子文件夹，也就是进入源代码文件夹继续构建
ADD_SUBDIRECTORY( ${PROJECT_SOURCE_DIR}/src)
