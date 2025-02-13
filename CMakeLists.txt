cmake_minimum_required(VERSION 3.9)
project(DiscordRPC)

# install library / headers
option(DISCORDRPC_INSTALL_LIBRARY "Install the Discord RPC library and headers" OFF)
if(DISCORDRPC_INSTALL_LIBRARY)
    include(GNUInstallDirs)
endif()

# format
file(GLOB_RECURSE ALL_SOURCE_FILES
    include/*.h
    src/*.cpp src/*.h
)

# add subdirs
add_subdirectory(src)
