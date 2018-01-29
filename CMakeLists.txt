cmake_minimum_required(VERSION 3.1)
project(patch LANGUAGES C)

set(SOURCES
	backupfile.c
	inp.c
	mkpath.c
	patch.c
	pch.c
	util.c
)
add_executable(patch ${SOURCES})
target_include_directories(patch PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
install(TARGETS patch RUNTIME DESTINATION bin)
