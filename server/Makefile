CC = g++
PWD = $(shell dirname $(realpath $(lastword $(MAKEFILE_LIST))))
LIB = -L ${PWD}
OPENCVLIBS = `pkg-config --cflags --libs opencv`
PCLLIBS =`pkg-config --libs pcl_apps-1.7 pcl_common-1.7 pcl_features-1.7 pcl_filters-1.7 pcl_geometry-1.7 pcl_io-1.7 pcl_kdtree-1.7 pcl_keypoints-1.7 pcl_octree-1.7 pcl_registration-1.7 pcl_sample_consensus-1.7 pcl_search-1.7 pcl_segmentation-1.7 pcl_surface-1.7 pcl_tracking-1.7 pcl_visualization-1.7 flann ` 
INCLUDEPATH = -I/usr/include/vtk-5.8 -I/usr/include/pcl-1.7 -I/usr/include/eigen3
SRC = SocketServer.cpp
FLAG = -pthread -lpthread -Wno-deprecated -std=c++11

all: SocketServer
	
SocketServer: ${SRC}
	${CC} $(FLAG) ${LIB} -g -o SocketServer ${SRC}   

clean:
	$(RM) *.o *.so main
