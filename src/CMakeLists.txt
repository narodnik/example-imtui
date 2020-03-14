set(TARGET example-imtui)

add_executable(${TARGET}
    main.cpp
    )

target_link_libraries(${TARGET} PUBLIC
    imtui-ncurses
    PkgConfig::LIBBITCOIN_SYSTEM
    )

install(TARGETS example-imtui RUNTIME DESTINATION bin)

