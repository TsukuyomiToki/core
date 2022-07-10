cmake_minimum_required(VERSION 3.14)

project(pisces-clipboard LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt5 COMPONENTS Core Gui Widgets REQUIRED)

add_executable(pisces-clipboard
  main.cpp
  clipboard.cpp
)
target_link_libraries(pisces-clipboard
    Qt5::Core
    Qt5::Gui
    Qt5::Widgets
)

install(TARGETS pisces-clipboard DESTINATION ${CMAKE_INSTALL_BINDIR})