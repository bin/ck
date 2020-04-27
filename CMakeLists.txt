CMAKE_MINIMUM_REQUIRED(VERSION 3.14)

SET(CMAKE_C_STANDARD 11)

PROJECT(ck)

MESSAGE(STATUS "Building concurrency kit.")

# Configure ck_md.h
SET(VERSION "0.7.0")
ADD_SUBDIRECTORY(${CMAKE_CURRENT_SOURCE_DIR}/include)

INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/include)

ADD_LIBRARY(ck STATIC
	src/ck_array.c
	src/ck_barrier_centralized.c
	src/ck_barrier_combining.c
	src/ck_barrier_dissemination.c
	src/ck_barrier_mcs.c
	src/ck_barrier_tournament.c
	src/ck_ec.c
	src/ck_epoch.c
	src/ck_hp.c
	src/ck_hs.c
	src/ck_ht.c
	src/ck_rhs.c)
