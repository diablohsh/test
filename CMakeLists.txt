project(test)

set(sccache SCCACHE_ERROR_LOG=/tmp/sccache_log.txt SCCACHE_LOG=debug SCCACHE_REDIS="redis://:testRedis@9.134.45.129:6380" ${CMAKE_CURRENT_LIST_DIR}/sccache)
set(CMAKE_C_COMPILER_LAUNCHER ${sccache})
set(CMAKE_CXX_COMPILER_LAUNCHER ${sccache})

add_executable(test test.cc)
