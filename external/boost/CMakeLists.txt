
set(Boost_USE_STATIC_LIBS ON)

find_package(Boost
    1.53.0 EXACT
    REQUIRED
    COMPONENTS
    system
    filesystem
    date_time
    program_options
    serialization
    thread
    regex
    atomic
    )

if (Boost_FOUND)
    message(STATUS "found boost in txt")
    set_target_properties(
        Boost::boost
        Boost::system
        Boost::filesystem
        Boost::date_time
        Boost::program_options
        Boost::serialization
        Boost::thread
        Boost::regex
        Boost::atomic
        PROPERTIES IMPORTED_GLOBAL TRUE
    )
endif ()

