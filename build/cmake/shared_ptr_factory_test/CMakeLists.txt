# 
# Copyright (c) 2015 Marat Abrarov (abrarov@gmail.com)
#
# Distributed under the Boost Software License, Version 1.0. (See accompanying
# file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt)
#

cmake_minimum_required(VERSION 2.8.11)
project(shared_ptr_factory_test)

find_package(Boost REQUIRED)

set(HEADERS_DIR "${PROJECT_SOURCE_DIR}/../../../include")
set(SOURCES_DIR "${PROJECT_SOURCE_DIR}/../../../src")

set(HEADERS
    "${HEADERS_DIR}/ma/detail/memory.hpp"
    "${HEADERS_DIR}/ma/config.hpp"
    "${HEADERS_DIR}/ma/shared_ptr_factory.hpp")

set(SOURCES
    "${SOURCES_DIR}/shared_ptr_factory_test/main.cpp"
)

include_directories(${Boost_INCLUDE_DIRS})
include_directories(${HEADERS_DIR})
add_executable(shared_ptr_factory_test ${HEADERS} ${SOURCES})
