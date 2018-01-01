CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
PROJECT(Base)

#ADD_EXECUTABLE(sourc_dir [binary_dir] [EXCLUDE FROM ALL])
#EXCLUE FROM ALL: exclude at compile stage
ADD_EXECUTABLE(hello main.cpp)

#If we want to changet the output binary file path or output library path, we could use the following two instructions
#In this example, they have the same functionalities as the default setting
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_LIBRARY_DIR}/lib)
INSTALL(TARGETS hello
    RUNTIME DESTINATION bin)
