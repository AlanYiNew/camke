CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

#This instruction define XXX_BINARY_DIR and XXX_SOURCE_DIR where XXX coresponds to Base
#It also define PROJECT_BINARY_DIR and PROJECT_SOURCE_DIR which have the same value as the two mentioned above
#It is recommended to use the bottom two so that we don't need to change this file due to change of project name
PROJECT(Base)

SET(SRC_LIST main.c)
ADD_SUBDIRECTORY(src bin)

INSTALL(FILES COPYRIGHT README DESTINATION share/doc/cmake)
INSTALL(PROGRAMS run.sh DESTINATION bin)
INSTALL(DIRECTORY doc/ DESTINATION share/doc/cmake)



