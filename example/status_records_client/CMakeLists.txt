project(status_records_client)

add_executable(status_records_client)

target_sources(status_records_client PRIVATE
    main.cpp)

target_link_libraries(status_records_client
    PRIVATE
    EcflowClient::ecflow_grpc
    CLI11::CLI11
    spdlog::spdlog_header_only
    )