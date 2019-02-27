cmake_minimum_required(VERSION 2.8)
project(chatbot)

include_directories(include include/ros_voice)
link_directories(${PROJECT_SOURCE_DIR}/libs)
add_library(speech src/linuxrec.c src/speech_recognizer.c)
target_link_libraries(speech -lmsc -lpthread -lasound)

add_executable(chatbot src/main.cpp)
target_link_libraries(chatbot  -lmsc -lpthread speech -ljsoncpp -lcurl)


