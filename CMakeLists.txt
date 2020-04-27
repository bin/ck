CMAKE_MINIMUM_REQUIRED(VERSION 3.14)

SET(CMAKE_C_STANDARD 11)

PROJECT(ck)

MESSAGE(STATUS "Building concurrency kit.")

INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/include)

ADD_LIBRARY(ck STATIC
	ck_array.c
	ck_barrier_centralized.c
	ck_barrier_combining.c
	ck_barrier_dissemination.c
	ck_barrier_mcs.c
	ck_barrier_tournament.c
	ck_ec.c
	ck_epoch.c
	ck_hp.c
	ck_hs.c
	ck_ht.c
	ck_rhs.c)
