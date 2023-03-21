project(test)

set(ENV{SCCACHE_REDIS} redis://:testRedis@9.134.45.129:6380)
set(CMAKE_CXX_COMPILER_LAUNCHER ${CMAKE_CURRENT_LIST_DIR}/sccache)

add_executable(test test.cc)
