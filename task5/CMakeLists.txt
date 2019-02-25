cmake_minimum_required (VERSION 2.0)
project(Problem5_cmakeproject)

include_directories(${CMAKE_SOURCE_DIR}/include)
link_directories(${CMAKE_SOURCE_DIR}/lib)

add_executable(myexe ${PROJECT_SOURCE_DIR}/src/driver.c)
target_link_libraries(myexe libc.so libmyfunctions.a)

install(TARGETS myexe DESTINATION /usr/bin)
install(FILES man/prog1.3 man/prog2.3 man/prog3.3 man/prog4.3 DESTINATION /usr/share/man/man3)

include(InstallRequiredSystemLibraries)
set(CPACK_GENERATOR "DEB")
set(CPACK_DEBIAN_PACKAGE_MAINTAINER "Ailia")
include(CPack)
