include_directories(
	${WLR_INCLUDE_DIRS}
	${XKBCOMMON_INCLUDE_DIRS}
)

add_library(sway-common STATIC
	ipc-client.c
	log.c
	util.c
	readline.c
	stringop.c
)

target_link_libraries(
    sway-common m
    ${WLR_LIBRARIES}
)
