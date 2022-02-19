cmake_minimum_required(VERSION 3.21)
project(playing_mysql)

set(CMAKE_CXX_STANDARD 17)

include_directories(${MYSQL_CONCPP_DIR}/include)
link_directories(${MYSQL_CONCPP_DIR}/lib64)

add_executable(playing_mysql tmp/library_usage_examples.cpp tmp/library.cpp)

target_link_libraries(playing_mysql mysqlcppconn)


