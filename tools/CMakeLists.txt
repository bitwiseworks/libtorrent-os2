add_executable(dht dht_put.cpp)
target_link_libraries(dht PRIVATE torrent-rasterbar)
if (OS2)
    set_target_properties(dht PROPERTIES
        OS2_DEF_VENDOR "$ENV{VENDOR}"
        OS2_DEF_PATCH "${VER_TINY}"
        OS2_DEF_VERSION "${PROJECT_VERSION}")
endif()

add_executable(dht_sample dht_sample.cpp)
target_link_libraries(dht_sample PRIVATE torrent-rasterbar)
if (OS2)
    set_target_properties(dht_sample PROPERTIES
        OS2_DEF_VENDOR "$ENV{VENDOR}"
        OS2_DEF_PATCH "${VER_TINY}"
        OS2_DEF_VERSION "${PROJECT_VERSION}")
endif()

add_executable(session_log_alerts session_log_alerts.cpp)
target_link_libraries(session_log_alerts PRIVATE torrent-rasterbar)
if (OS2)
    set_target_properties(session_log_alerts PROPERTIES
        OS2_DEF_VENDOR "$ENV{VENDOR}"
        OS2_DEF_PATCH "${VER_TINY}"
        OS2_DEF_VERSION "${PROJECT_VERSION}")
endif()
