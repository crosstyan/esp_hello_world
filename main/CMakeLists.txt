file(GLOB SRC_FILES
    "src/*.c"
    "src/*.cpp"
)

idf_component_register(SRCS ${SRC_FILES}
                    INCLUDE_DIRS "include")
