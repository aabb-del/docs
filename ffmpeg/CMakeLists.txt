cmake_minimum_required(VERSION 3.0)
project(ffmpeg_test)

include_directories(./include)
link_directories(./lib)

set(SRC_LIST
    ./ffmpeg_test.c
)

add_executable(ffmpeg_test ${SRC_LIST})

target_link_libraries(
    ffmpeg_test 
    
    pthread 
    avfilter
    avformat
    avcodec
    avutil
    swresample
    swscale
    m  
    z
)